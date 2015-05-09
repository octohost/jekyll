Jekyll
====

Basic [Jekyll](http://jekyllrb.com/) container for octohost.

The base Jekyll image was built like this:

```
FROM octohost/node-ruby

RUN export LANGUAGE=en_US.UTF-8 && export LANG=en_US.UTF-8 && export LC_ALL=en_US.UTF-8 && locale-gen en_US.UTF-8 && dpkg-reconfigure locales
RUN apt-get update && apt-get -y install python2.7 make && apt-get clean && rm -rf /var/lib/apt/lists/* && ln -s /usr/bin/python2.7 /usr/bin/python
RUN gem install pygments.rb jekyll --no-rdoc --no-ri
```

Clone this repo and use Jekyll to develop your website.

Push this repo to your octohost:

```
git clone https://github.com/octohost/jekyll.git
cd jekyll
git remote add octohost git@ip.address.here:jekyll.git
git push octohost master
```

This repo uses the [jekyll-nginx](https://github.com/octohost/jekyll-nginx) container to serve static files.
