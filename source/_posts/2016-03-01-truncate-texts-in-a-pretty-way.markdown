---
layout: post
title:  "Truncate texts in a pretty way"
date:   2016-03-01 11:21:32 +0200
categories: Development
tags: frontend
permalink: /truncate-texts-in-a-pretty-way/
image: https://lh3.googleusercontent.com/YVkzcnY82n_MvxFGG9BMynWQ7EnoKsSEiTpfTyDdcrJyiDkY6NRvKaHlGtJB-1VgBB9g6PiXYyB45lzPrETEA90yCWyfHZOKGaQ0XiTG6dPS9oET5vq8ojDxbUYESYdtIAc5fLq42A
---

Text-overflow: ellipsis truncates the overflowing text, and adds '...' at the end. And it is responsive, so it will always look nice:

{% highlight css %}
p {
   text-overflow: ellipsis;
}
{% endhighlight t%}

<a href="https://jsfiddle.net/6yrw244h/" target="_blank">Try it in JSFiddle</a>

<script src="//jsfiddle.net/6yrw244h/embed/html,css,result/dark/" async=""></script>