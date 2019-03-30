
```
 _____ _     _     ___                                     
/  ___(_)   | |   |_  |                                    
\ `--. _  __| |     | | __ _ _   _  __ _ _ __  _ __   __ _
 `--. \ |/ _` |     | |/ _` | | | |/ _` | '_ \| '_ \ / _` |
/\__/ / | (_| | /\__/ / (_| | |_| | (_| | | | | | | | (_| |
\____/|_|\__,_| \____/ \__,_|\__, |\__,_|_| |_|_| |_|\__,_|
                              __/ |                        
                             |___/                         

```
# sjayanna.github.io

This repository contains the Jekyll theme and content of my blog.

### Want to use this theme?

* Remove the existing content

```
$ rm -rf about notes slides _posts keybase.txt CNAME
```

* Create new posts directory

```
$ mkdir _posts
```

* To run the site locally

```
$ bundle exec jekyll serve
```

* Edit the details from `_config.yml`. Make sure you leave the Disqus and
  Google Analytics configs blank if you don't use them.
* Change title in `index.html`

### Rake tasks

There are two rake tasks - `rake post` and `rake page` which prompt for
metadata and generate the markdown files.

### Jekyll guide

https://help.github.com/en/articles/using-jekyll-as-a-static-site-generator-with-github-pages

https://help.github.com/en/articles/setting-up-your-github-pages-site-locally-with-jekyll#step-4-build-your-local-jekyll-site
