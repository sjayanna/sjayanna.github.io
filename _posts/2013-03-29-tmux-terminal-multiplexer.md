---
layout: post
title: "Tmux   terminal multiplexer"
description: ""
category: tmux
tags: []
---

I have used [gnu screen](http://www.gnu.org/software/screen/) before but for the last month I have been using [tmux terminal multiplexer](http://tmux.sourceforge.net/). Using vim and Tmux on iTerm2 on OSX is really becoming a big part of my workflow while trying to get stuff done.

Few commands to get started with Tmux (prefix is the keyboard shortcut defined in ~/.tmux.conf)

{% highlight text %}
#creates a new tmux session named session_name
tmux new -s session_name

#attaches to an existing tmux session named session_name
tmux attach -t session_name

#switches to an existing session named session_name
tmux switch -t session_name

#lists existing tmux sessions
tmux list-sessions

#detach the currently attached session
tmux detach (prefix + d)

#splits the window into two vertical panes
tmux split-window (prefix + ")

#splits the window into two horizontal panes
tmux split-window -h (prefix + %)
{% endhighlight %}


### Further reading
* This [link](http://robots.thoughtbot.com/post/2641409235/a-tmux-crash-course) helped me get started with Tmux and has more helpful commands.
