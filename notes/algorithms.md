---
layout: page
title: "Algorithms"
date:  2015-04-18 19:14:33
---

### Big O notation

In computer science, big O notation is used to classify algorithms by how they respond to changes in input size, such as how the processing time of an algorithm changes as the problem size becomes extremely large.

The big thing that Big-O notation means to your code is how it will scale when you double the amount of "things" it operates on. Here's a concrete example:

{% highlight bash %}
Big-O       |  computations for 10 things |  computations for 100 things
----------------------------------------------------------------------
O(1)        |   1                         |     1
O(log(n))   |   3                         |     7
O(n)        |  10                         |   100
O(n log(n)) |  30                         |   700
O(n^2)      | 100                         | 10000

{% endhighlight %}
So take quicksort which is O(n log(n)) vs bubble sort which is O(n^2). When sorting 10 things, quicksort is 3 times faster than bubble sort. But when sorting 100 things, it's 14 times faster! Clearly picking the fastest algorithm is important then. When you get to databases with million rows, it can mean the difference between your query executing in 0.2 seconds, versus taking hours.

Another thing to consider is that a bad algorithm is one thing that Moore's law cannot help. For example, if you've got some scientific calculation that's O(n^3) and it can compute 100 things a day, doubling the processor speed only gets you 125 things in a day. However, knock that calculation to O(n^2) and you're doing 1000 things a day.

* [Assignments - Problem Solving with Algorithms and Data Structures](http://interactivepython.org/runestone/static/pythonds/index.html)
