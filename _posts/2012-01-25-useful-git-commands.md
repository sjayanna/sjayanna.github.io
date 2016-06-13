---
layout: post
title: "Useful git commands"
categories: git
---
Quick git tutorial for those who join my group.

### Git configuration
{% highlight text %}
git config --global user.name "username"
git config --global user.email "email address"
git config --global core.editor vim
git log --pretty-oneline
{% endhighlight %}

### Basic Git workflow

{% highlight text %}
git init (for a new project)
git clone remote_repo (for an existing project)
git co -b new_branch name
git add .
git commit -m "meaningful commit message"
git co master_branch
git merge new_branch
git push origin branch_name
{% endhighlight %}


### Sync with a github upstream repo after a fork

{% highlight text %}
git remote add upstream git@github.com:remote_parent_repo
git checkout master
git fetch upstream
git rebase upstream/master
#push commit to fork after rebase
git push origin master
{% endhighlight %}

### Few useful commands

{% highlight text %}
git remote add origin ../app.git
git clean -f -d ( d to remove directories) - Remove untracked files
git remote prune origin ( to remove orphan remote branches)
git remote | xargs -L 1 git push - to push to all repos
git checkout branch_name path_to_file - to bring a file from another branch
git commit --amend -m "new commit message" - change last commit message
{% endhighlight %}

### Further reading
* [Git Book](https://git-scm.com/book/en/v2)
* [Quick tutorial](http://rogerdudler.github.io/git-guide/)
* [Sync with github upstream](https://2buntu.com/articles/1459/keeping-your-forked-repo-synced-with-the-upstream-source/)
