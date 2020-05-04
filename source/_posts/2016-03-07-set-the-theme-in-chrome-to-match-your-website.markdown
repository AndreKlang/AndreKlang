---
layout: post
title:  "Set the theme in Chrome to match your website"
date:   2016-03-07 12:54:32 +0200
categories: Development
tags: frontend
permalink: /set-the-theme-in-chrome-to-match-your-website/
image: https://lh3.googleusercontent.com/YVkzcnY82n_MvxFGG9BMynWQ7EnoKsSEiTpfTyDdcrJyiDkY6NRvKaHlGtJB-1VgBB9g6PiXYyB45lzPrETEA90yCWyfHZOKGaQ0XiTG6dPS9oET5vq8ojDxbUYESYdtIAc5fLq42A
---

For quite some time it's been possible to set the color theme in Chrome for Android to match your sites main color. However, it's not been widely adopted until a month or two ago, when I stared to see matching theme in my chrome, and kind of liked it.

So I hit my friend Google with the question,, and it wasn't that easy to find actually, a lot of nonsense results. Until I found the source: <a href="https://developers.google.com/web/updates/2014/11/Support-for-theme-color-in-Chrome-39-for-Android" target="_blank">Original post from Google</a>

So it turns out it's very easy to set the theme, just include a meta-tag with the HEX of your color, like this:

{% highlight html %}
<meta name="theme-color" content="#db5945">
{% endhighlight %}

(I'll add a pretty screenshot later..)

<strong>Update:</strong>

I found additional info as well regarding <a href="https://developers.google.com/web/fundamentals/design-and-ui/browser-customization/theme-color" target="_blank">the similar thing in Apples Safari</a>