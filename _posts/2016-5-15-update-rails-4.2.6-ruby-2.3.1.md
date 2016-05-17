---
layout: post
title: "Update Rails App to 4.2.6 and Ruby to 2.3.1"
description: ""
category:
tags: []
---

We had to update a heavily used application which was running Rails 4.2.0 to the latest release of Rails (4.2.6 as of this writing) and also wanted to get the performance benefits of the latest Ruby update to 2.3.1.

It was as simple as changing the versions in the Gemfile as shown below and then deploy the application via [Ansible](https://www.ansible.com/) and [Capistrano](http://capistranorb.com/documentation/overview/what-is-capistrano/#) to the staging and production server. The [application](http://supportGFC.org) is running smoothly with all the security and bug fixes applied!!

{% highlight ruby %}
# Gemfile
source 'https://rubygems.org'
ruby '2.3.1'

gem 'rails', '4.2.6'
gem 'pg', '0.18.4'

gem 'devise'
gem 'omniauth-facebook'
.
.
.
{% endhighlight %}

### Further reading

* [Rails 4.2.6 and 4.1.15 have been released!](http://weblog.rubyonrails.org/2016/3/11/Rails-4-2-6-and-4-1-15-have-been-released/)
* [Ruby 2.3.1 Released](https://www.ruby-lang.org/en/news/2016/04/26/ruby-2-3-1-released/)
* [Ruby 2.3.1 Changelog](http://svn.ruby-lang.org/repos/ruby/tags/v2_3_1/ChangeLog)
