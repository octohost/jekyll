Jekyll
====

Basic [Jekyll](http://jekyllrb.com/) container for octohost.

Clone this repo and use Jekyll to develop your website.

Push this repo to your octohost:

```
git clone https://github.com/octohost/jekyll.git
cd jekyll
git remote add octohost git@ip.address.here:jekyll.git
git push octohost master
```

This repo uses the [jekyll-nginx](https://github.com/octohost/jekyll-nginx) container to serve static files.

Example site \(usually\) at [http://jekyll.octohost.io](http://jekyll.octohost.io)
