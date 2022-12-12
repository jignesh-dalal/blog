---
date: 2022-12-10
title: How I Made This Blog? 
description: A guide on my journey towards learning Eleventy and GitHub Pages.
tags:
  - git
  - tech
---

## Requirement
I simply loved the idea of GitHub Pages which when combined with Jekyll, a static site generator, can help generate a lightweight blogging site. Unfortunately, Jekyll is not officially supported for Windows and the requirement of Ruby adds to the learning curve if one wishes to tread the unofficial route.

Being somewhat a lazy (read laid-back) person and not a professional writer, I need to keep the whole blogging experience simple enough to help me continue with the journey. And for someone who is already familiar with GitHub being a developer, here is the 1-2-3 requirement:
1. Create a new Markdown file for the blog post.
2. Add the blog contents.
3. Push it to git repository with GitHub Actions performing the heavy lifting of updating the blog hosted under GitHub Pages.

## Implementation
Without further ado, I ended up using following for my blog:

### [Eleventy](https://www.11ty.dev/docs/)
Eleventy is NodeJS based tool as it uses JavaScript in NodeJS to transform templates into content. It is not a JavaScript framework as it does not recommend nor force your HTML to include any Eleventy-specific client-side JavaScript.

Bootstrapped my [blog](https://github.com/jignesh-dalal/blog) repo with [eleventy-base-blog](https://github.com/11ty/eleventy-base-blog).

#### Getting started with Eleventy
* https://keepinguptodate.com/pages/2019/06/creating-blog-with-eleventy/
* https://www.filamentgroup.com/lab/build-a-blog/
* https://24ways.org/2018/turn-jekyll-up-to-eleventy/
* https://www.aleksandrhovhannisyan.com/blog/useful-11ty-filters/


### [Slate theme](https://github.com/pages-themes/slate)
Slate is a **Jekyll** theme for GitHub Pages.

Being a **Jekyll** theme for GitHub Pages, this required to be ported for use in Eleventy which was done as follows:
* Copied over .sass files for the Slate theme.
* Configured my [blog](https://github.com/jignesh-dalal/blog) repo to perform sass to css transformation using the `sass` npm package.


## Deploy to GitHub Pages with GitHub Actions
* https://stedman.dev/2020/04/29/make-the-jump-from-jekyll-to-javascript/
* https://www.rockyourcode.com/how-to-deploy-eleventy-to-github-pages-with-github-actions/
* https://maarten.be/blog/20220730/how-to-deploy-your-eleventy-website-to-github-pages-with-github-actions/


## References
* https://eleventy-chirpy-blog-template.netlify.app/
* https://rachelcarmena.github.io/