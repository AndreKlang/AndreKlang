---
layout: post
title:  "Set the theme in Chrome to match your website"
date:   2016-03-07 12:54:32 +0200
categories: Development
tags: frontend
permalink: /set-the-theme-in-chrome-to-match-your-website/
background: https://lh3.googleusercontent.com/u3XJZ6rRFIUcr34Ueyvx5hrF5bTXlxE5eAeYFN-LxlPEGJNb-b6cBJsExU_hrwk6x6s2BxHGxduSWVWubJxoI57pPKHU4XJbc7hWqEw2eA5jUwEeml8Q16yMGBF9NLQPja5FvXqI6kkekbbZr4UYUxMy_t2ZWiY1qpoJup13oOWCB1cBWsM2ZD4eP_qiXwA1blWZ7KLpi3JXhOU2qir-1hBy9ArzELPrDq7S2qip4cGNVocRndYsRFuO-INAipACm77Pe5Ni4NiP6j7qK3PBdLCvyQ5ZH7h5O5wQIP8j7kTkreJDg_8Nt_iJGNbd93TYnFO5DupAU8uOuDedkysfPRJBL_GarwWrbaEu1rqrdlkTSe23fIjkCkIaf3F8OFt780k_mtzXKxn-GxBGJYqrUdqtSZopayyvWHfd6lExzXoLWqeZbCx5Lz3uLe9H7o4wyTJsO__dVSxD7DD3-_KsmM_YVWlWe3aGoZJWm_Bfg4fsWuzQqNDKkcwZiCeb_EPEkWdxI9f7CEBufhKAyMCI57ygAiEJTI7KC_GakkeQMhVcxS4ZT0X0MyzPXUe4oveF0AKAevcamaY6v1w12vJoknyhgyASVO3E4G_sQhq0IE1xPr2ZSzZdCdDVyIFV_qbrRBIRpQNzRGIvNJ4AM_ln3TExDhUpGdBszlBx2q9KNaFB7_L-r5GHVE3WS58hZFhGMTo1ztW_SzSp7OxgIQ-zCJWCzPwjqtX7_34zAUTFikSiTt3E9Zi5hF0
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