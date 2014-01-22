---
layout: post
title: "'setting up octopress'"
date: 2014-01-21 20:21:26 -0800
comments: true
categories:
---

``` bash
git clone git://github.com/imathis/octopress.git octopress-foo
cd octopress-foo

bundle install --path .bundle --binstubs

rake install
rake setup_github_pages
rake generate
rake deploy

echo 'foo.philmonroe.com' >> source/CNAME
# dns
## foo.philmonroe.com => phil-monroe.github.io

rake generate
rake deploy

git cm "getting things setup"
git remote add origin git@github.com:phil-monroe/foo.git
git config branch.master.remote origin
git push origin master

rake new_post["setting up octopress"]
```