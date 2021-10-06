---
layout: mypost
title: How to write the article and publish to blog
categories: [Blog]
---

## local write the article,

1.copy the template
2.then edit it in the local

## then review it locally,

```
bundle exec jekyll serve --watch --host=127.0.0.1 --port=8080
```

## and publish to the github

```
cd to the destination file
git add file
git commit -m 'file'
git push -u origina main
```

[Add a file using the command line](https://docs.gitlab.com/ee/gitlab-basics/add-file.html)

## Auto process it

Travis
