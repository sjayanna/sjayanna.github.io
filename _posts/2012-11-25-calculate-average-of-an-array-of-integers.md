---
layout: post
title: "Calculate average of an array of integers in Ruby"
description: ""
category:
tags: []
---


I was teaching the concept of average to my elementary grade school daughter and figured the output of the below code would help her better understand.

{% highlight text %}
1.9.2p290 :094 > array = [*1..10]
 => [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
1.9.2p290 :095 > average = array.inject(0) { |memo, n| memo + n } / array.size.to_f
 => 5.5
1.9.2p290 :096 > puts "Average of array #{array} is #{average}"
Average of array [1, 2, 3, 4, 5, 6, 7, 8, 9, 10] is 5.5
 => nil
1.9.2p290 :097 >
{% endhighlight %}


The gist is available [here](https://gist.github.com/sjayanna/5028070)
<script src="https://gist.github.com/sjayanna/5028070.js"></script>
