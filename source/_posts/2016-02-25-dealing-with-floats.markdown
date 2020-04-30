---
layout: post
title:  "Dealing with floats in PHP"
date:   2016-02-25 11:29:02 +0200
categories: Development
tags: php
permalink: /dealing-with-floats-in-php/
image: https://lh3.googleusercontent.com/YVkzcnY82n_MvxFGG9BMynWQ7EnoKsSEiTpfTyDdcrJyiDkY6NRvKaHlGtJB-1VgBB9g6PiXYyB45lzPrETEA90yCWyfHZOKGaQ0XiTG6dPS9oET5vq8ojDxbUYESYdtIAc5fLq42A
---

As we all know, php does not have a good data type for decimals, so we're stuck with floats. And let's face it, they are not always so easy to deal with and to get the expected results.

I recently needed to take a sum of money in a payment module, and convert it from dollars to cents, and send it as an integer to a webservice. Easy enough, but something came up..

## So why are floats difficult?
Well, it has to do with how they are stored in memory, I won't get into it too deep (because I frankly don't really know). But the short description, all values can't be stored in an accurate representation. So it is stored "good enough", or "as good as possible".

And what does that mean? For example the value from the tests below: "143.2" can't be stored. So it is stored like this "143.19999999999998863", and then whenever it is used it is rounded back to 143.2.
> It's rounded back? Then whats the issue?

Glad you asked! The issue? Start doing calculations with it, you'll start to see some funny problems.

Study the example below, it's fairly simple. We start with the value 143.2 and multiply that with 100. Result is quite simple 14320. This is not the interesting part, as I said, I needed to send it as an integer. So I did a simple typecast and I was done! To production the payment module went!

Don't you hate it when someone reports "wierd" bugs on your stuff..
> The order total is one cent wrong! What the f?

Lets try that out..

{% highlight php %}  
var_dump((int) 143.2 * 100);
// int(14319)
{% endhighlight W%}  

14319!?! WHAT!?!

Well,, simple answer.. As I said, do some calculations with a float:
<pre>143.19999999999998863 * 100 = 14319.999999999998863</pre>

## Now to another aspect. What happens when we cast to int?
Well, anything that is not valid integer, is cut of.

So take our example from above, remove anything that is no integer, and what do you get? 14319! Not the expected 14320..

## So how do we cast that to an int?
Well, I think I tried all possible solutions.. Rounding, intval, bc_math, and anything else I could think of. Until I started to think about why var_dump says the correct value when it is a float.

Floats have some kind of "toString"-method, that fixes the rounding. But NOT a "toInteger"-method..

So what if... We cast to string first, making use of "toString", then cast that to integer. SUCCESS!

See line 18 below.

<script src="https://gist.github.com/AndreKlang/f20c55abbc22e2bc7c2c.js"></script>

result:

<pre>
Raw: --------------
float(143.2)
float(14320)

Cast: --------------
int(143)
int(14319)

Test: --------------
float(14320)
int(14319)
int(14319)
int(14320) <-- LINE 18: SUCCESS

Real values: -------
float(143.19999999999998863)
float(14319.999999999998181)

</pre>
