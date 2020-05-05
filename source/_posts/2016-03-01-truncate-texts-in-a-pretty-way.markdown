---
layout: post
title:  "Truncate texts in a pretty way"
date:   2016-03-01 11:21:32 +0200
categories: Development
tags: frontend
permalink: /truncate-texts-in-a-pretty-way/
background: https://lh3.googleusercontent.com/u3XJZ6rRFIUcr34Ueyvx5hrF5bTXlxE5eAeYFN-LxlPEGJNb-b6cBJsExU_hrwk6x6s2BxHGxduSWVWubJxoI57pPKHU4XJbc7hWqEw2eA5jUwEeml8Q16yMGBF9NLQPja5FvXqI6kkekbbZr4UYUxMy_t2ZWiY1qpoJup13oOWCB1cBWsM2ZD4eP_qiXwA1blWZ7KLpi3JXhOU2qir-1hBy9ArzELPrDq7S2qip4cGNVocRndYsRFuO-INAipACm77Pe5Ni4NiP6j7qK3PBdLCvyQ5ZH7h5O5wQIP8j7kTkreJDg_8Nt_iJGNbd93TYnFO5DupAU8uOuDedkysfPRJBL_GarwWrbaEu1rqrdlkTSe23fIjkCkIaf3F8OFt780k_mtzXKxn-GxBGJYqrUdqtSZopayyvWHfd6lExzXoLWqeZbCx5Lz3uLe9H7o4wyTJsO__dVSxD7DD3-_KsmM_YVWlWe3aGoZJWm_Bfg4fsWuzQqNDKkcwZiCeb_EPEkWdxI9f7CEBufhKAyMCI57ygAiEJTI7KC_GakkeQMhVcxS4ZT0X0MyzPXUe4oveF0AKAevcamaY6v1w12vJoknyhgyASVO3E4G_sQhq0IE1xPr2ZSzZdCdDVyIFV_qbrRBIRpQNzRGIvNJ4AM_ln3TExDhUpGdBszlBx2q9KNaFB7_L-r5GHVE3WS58hZFhGMTo1ztW_SzSp7OxgIQ-zCJWCzPwjqtX7_34zAUTFikSiTt3E9Zi5hF0
---

Text-overflow: ellipsis truncates the overflowing text, and adds '...' at the end. And it is responsive, so it will always look nice:

{% highlight css %}
p {
   text-overflow: ellipsis;
}
{% endhighlight t%}

<a href="https://jsfiddle.net/6yrw244h/" target="_blank">Try it in JSFiddle</a>

<script src="//jsfiddle.net/6yrw244h/embed/html,css,result/dark/" async=""></script>