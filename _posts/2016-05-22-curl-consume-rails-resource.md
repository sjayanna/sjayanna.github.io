---
layout: post
title: "Using cURL to interact with Rails resource/api"
date:  2016-05-22  0:53:38
categories: rails
---

[cURL](https://en.wikipedia.org/wiki/CURL) is a command line tool for doing all sorts of URL manipulations and transfers

HTTP is the protocol used to fetch data from web servers. It is a very simple protocol that is built upon TCP/IP. The protocol also allows information to get sent to the server from the client using a few different methods, as will be shown here.

HTTP is plain ASCII text lines being sent by the client to a server to request a particular action, and then the server replies a few text lines before the actual requested content is sent to the client.

The client, curl, sends a HTTP request. The request contains a method (like GET, POST, HEAD etc), a number of request headers and sometimes a request body. The HTTP server responds with a status line (indicating if things went well), response headers and most often also a response body. The "body" part is the plain data you requested, like the actual HTML or the image etc.

I have a Rails application running at localhost:3000 which has a simple resource running on it. With the Rails authenticity token enabled it is a bit tricky to POST via cURL and so go ahead and disable the authenticy token verification by disabling `protect_from_forgery with: :exception` line in application_controller.rb file to keep it simple. Then follow below code.

{% highlight bash %}
#get HEAD
→ curl --head http://localhost:3000

#to delete a resource
→ curl -X DELETE http://localhost:3000/high_scores/2

#to post form data
→ curl -X POST -d "high_score[game]=Jordan" -d "high_score[score]=99" \
  http://localhost:3000/high_scores

#to get data
→ curl http://localhost:3000/high_scores

#to update data using HTTP PUT Method
→ curl -X PUT -d "high_score[score]=11" http://localhost:3000/high_scores/8

#to update data using HTTP PATCH Method
→ curl -X PATCH -d "high_score[score]=21" http://localhost:3000/high_scores/8

#follow redirects
→ curl -L google.com
{% endhighlight %}

### References
* [HTTP Basics](https://robots.thoughtbot.com/back-to-basics-http-requests)
* [cURL with token](https://robots.thoughtbot.com/curling-with-rails-authenticity-token)
* [curl reference](https://curl.haxx.se/docs/httpscripting.html)
* [thoughtbot http blogs](https://robots.thoughtbot.com/tags/http)
* [curl with rails](http://commandercoriander.net/blog/2014/01/11/curling-with-rails/)
* [Rails Securiy](http://guides.rubyonrails.org/security.html)
* [Undertanding rails authenticy token](http://stackoverflow.com/questions/941594/understanding-the-rails-authenticity-token)
