---
layout: post
title: How to run Jekyll
subtitle: Steps and problems
categories: Programming
tags: [Jekyll]
---

## Installing Jekyll

### Install Ruby

Use Ruby --version to check

### Install Bundler

gem install bundler

### Install Jekyll

Write the following in Gemfile

source 'https://rubygems.org'
gem 'github-pages'

Then use the command to run jekyll in the local server.

bundle exec jekyll serve

http://localhost:4000

Problem 1: Please add the following to your Gemfile to avoid polling for changes:
    gem 'wdm', '>= 0.1.0' if Gem.win_platform?


gem install wdm

Problem 2: Cannot load such file -- webrick (LoadError)

Add webrick as a dependency: bundle add webrick