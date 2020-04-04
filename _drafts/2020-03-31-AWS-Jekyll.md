---
layout: post
title:  "AWS Jekyll"
date:   2020-03-31 4:37:00 -0600
categories: [tutorial]
tags: [AWS]
---

# Overview

This is a tutorial on how to deploy a Jekyll site to AWS. There are a lot of sites out there describing bits and pieces of this but I thought that I would try to bring together my notes, references and steps all in one place.

The tutorial assumes that you've already figured out how to build your Jekyll site. This tutorial describes:

1. Configuring your S3 Bucket for static content
2. Configuring AWS Route 53
    * Redirect
* CloudFront
    * HTTPS
* Deploy through Github

# Github Deploy

[jekyll AWS deploy](https://github.com/ethanfahy/jekyll-aws)

[jekyll & Drone](https://dev.to/adelowo/building-and-deploying-a-jekyll-site-with-drone-ci-2eib)