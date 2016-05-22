---
layout: page
title: "Http"
date:  2016-05-21 23:54:42
---

### Using curl to interact with a Rails resource via HTTP Methods

With the authenticity token enabled it is a bic tricky to POST via cURL and so go ahead and disable the authenticy token verification by disabling `protect_from_forgery with: :exception` line in application_controller.rb file. Then follow below code.

{% highlight bash %}
#to delete a resource
→ curl -X DELETE http://localhost:3000/high_scores/2

#to post form data
→ curl -X POST -d "high_score[game]=Jordan" -d "high_score[score]=99" http://localhost:3000/high_scores

#to get data
→ curl http://localhost:3000/high_scores

#to update data using HTTP PUT Method
→ curl -X PUT -d "high_score[score]=11" http://localhost:3000/high_scores/8

#to update data using HTTP PATCH Method
→ curl -X PATCH -d "high_score[score]=21" http://localhost:3000/high_scores/8
{% endhighlight %}

### References
* [curling with token](https://robots.thoughtbot.com/curling-with-rails-authenticity-token)
* [curl with rails](http://commandercoriander.net/blog/2014/01/11/curling-with-rails/)
* [Rails Securiy](http://guides.rubyonrails.org/security.html)
* [Undertanding rails authenticy token](http://stackoverflow.com/questions/941594/understanding-the-rails-authenticity-token)

###References
* [HTTP Basics](https://robots.thoughtbot.com/back-to-basics-http-requests)
* [cURL with token](https://robots.thoughtbot.com/curling-with-rails-authenticity-token)
* [curl reference](https://curl.haxx.se/docs/httpscripting.html)
