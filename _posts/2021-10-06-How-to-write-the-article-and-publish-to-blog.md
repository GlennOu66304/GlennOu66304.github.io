---
layout: mypost
title: How to write the article and publish to blog
categories: [Blog]
---
## set up the writing enviroment in the local:
```
git clone https://github.com/GlennOu66304/Blog.git
cd Blog
gem install bundler
sudo gem install bundler
bundle install
```

## local write the article,

1.copy the template
2.then edit it in the local
3.you can use the editor like the typora or sublime

## then review it locally,

```
bundle exec jekyll serve --watch --host=127.0.0.1 --port=8080
```

## and publish to the github

```
cd to the destination folder
git add file
// (you can cd to file path, then process below )
git commit -m 'file'
git push -u origina main
```

[Add a file using the command line](https://docs.gitlab.com/ee/gitlab-basics/add-file.html)

## Auto process it

Travis
