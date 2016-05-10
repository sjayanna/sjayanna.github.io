---
layout: post
title: "Useful git commands"
description: ""
category:
tags: []
---
Quick git tutorial for those who join my group at Miami University.

Git configuration

	git config --global user.name "username"
	git config --global user.email "email address"
	git config --global core.editor vim
	git log --pretty-oneline

Basic Git workflow

	git init (for a new project)
	git clone remote_repo (for an existing project)
	git co -b new_branch name
	git add .
	git commit -m "meaningful commit message"
	git co master_branch
	git merge new_branch
	git push origin branch_name

Few useful commands, this list will be updated as needed.

	git remote add origin ../app.git
	git clean -f -d ( d to remove directories) - Remove untracked files from the working tree
	git remote prune origin ( to remove orphan remote branches)
	git remote | xargs -L 1 git push - to push to all repos
	git checkout branch_name path_to_file - to bring a file from another branch
	git commit --amend -m "new commit message" - change last commit message
