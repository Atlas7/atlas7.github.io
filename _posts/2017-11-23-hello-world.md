---
layout: post
title:  "My first Jekyll blog on Github pages"
date:   2017-11-23 18:00:00
desc: "Documentation of how I created my first Jekyll blog hosted on Github pages"
keywords: "Jalpc,Jekyll,gh-pages,website,blog,easy"
categories: [HTML]
tags: [Jalpc,Jekyll,blog,ruby,gh-pages]
icon: icon-html
---

I just spent one day building this blog with Jekyll and github page and it's now up. Many thanks to
[Jalpc Jekyll Blog](https://jarrekk.github.io/Jalpc/) which I blatantly git cloned and tweaked to avoid building from
scratch. It's actually pretty great looking!

How I created this blog:

- Pre-requisites:
  - have a GitHub account
  - have a read of [these GitHub pages intros](https://pages.github.com/)
  - have some basic knowledge of writing documents in [Markdown format](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).
  - have these tools installed on the macbook:
    - [rbenv](https://github.com/rbenv/rbenv): a tool that creates isolated Ruby environments
    - Install the latest Ruby within an isolated rbenv environment (so it does not mess with the local system)
    - Install `jekyll` and `bundler` - as per the [jekyll official website](https://jekyllrb.com/)
- Build the site locally:
  - git clone the repository [Jalpc Jekyll Blog](https://jarrekk.github.io/Jalpc/) to the local macbook
  - rename the repository to `<github-user>.github.io`. (In my case, `atlas7.github.io`. This is to make it mine)
  - tweak the related files as instructed in the `README.md` document.
  - use `jekyll serve`, or `bundle exec jekyll serve` to preview blog at [http://127.0.0.1:4000/](http://127.0.0.1:4000/)
  - iterate a bit to make the blog looks good.
  - when satisfied, commit the change. i.e. `git add .`, `git commit -m "make it mine"`.
- Deploy the site to GitHub Pages:
  - on GitHub, create a new repository called `<github-user>.github.io`. In my case, `atlas7.github.io`.
  - going back to the repository locally, change the remote path of `origin` to our one. i.e. `git remote set-url https://github.com/<github-user>/<github-user>.github.io`
  - make sure our remote `origin` now points to our own GitHub repository. i.e. `git remote -v`
  - push the local repository to GitHub. i.e. `git push origin master`
  - Done!
  
# Testing 123

This blog is written in Markdown format. Let's try something out!

Here is a bash snippet:

```bash
cd ENV
source ./bin/activate
```

Here is a raw text snippet:

```
hello 123
hello testing 123
```

Here is a JavaScript code snippet:

```javascript
const add = (a, b) => a + b
const c = add (10, 20)
console.log(c)  //=> print 30
```

Here is a Python code snippet:

```python
def add(a, b):
  return a + b

c = add(10, 20)
print(c)  # print 30
```

Looking good!

---

Some previously mentioned now fixed:

- Problem: for some reason when I click on the code snippet it disappears???
[Fixed - see this GitHub Issue Log](https://github.com/jarrekk/Jalpc/issues/97)

---