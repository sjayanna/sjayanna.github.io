---
layout: post
title: "Ruby reverse string"
date:  2016-05-1 14:10:03
categories: ruby
---

I got a request from someone on a [Slack channel](https://slack.com/) to write a method in ruby which reverses a string without using the in-built 'reverse' method in the standard String library. I understand there are several other solutions, below is my quick solution.

{% highlight ruby %}
#reverse.rb
def reverse_string(input)
  b = []
  input.split('').map { |elm| b.unshift(elm) }
  return b.join()
end

print "Enter the string to be reversed: "
input = gets
puts "the reverse is: #{reverse_string(input)}"
{% endhighlight %}


### Further reading
* [Ruby String Library](http://ruby-doc.org/core-2.3.0/String.html#method-i-reverse)
