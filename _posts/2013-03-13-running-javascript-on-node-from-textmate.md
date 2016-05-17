---
layout: post
title: "Running javascript on node from textmate"
description: ""
category:
tags: []
---

I had issues running javascript on node from textmate using the [Javascript node textmate bundle](https://github.com/drnic/javascript-node.tmbundle).

I created my own command based off the run command from coffee-script textmate bundle. Hope this saves you some time searching.

{% highlight bash %}
#!/bin/bash
function pre {
	echo -n '<pre style="word-wrap: break-word; font-size:15px;">'
	perl -pe '$| = 1; s/&/&amp;/g; s/</&lt;/g; s/>/&gt;/g; s/$\\n/<br>/'
	echo '</pre>'
}
${TM_Node:=node} | pre
{% endhighlight %}

My configuration screenshot is below:

![Alt Javascript node textmate configuration](/images/js-node-textmate.jpg "Javascript node textmate configuration")
