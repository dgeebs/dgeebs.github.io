---
layout: post
title:  "Hello Github Pages!"
date:   2024-04-23 09:22:00 -0700
categories: general
---
One doesn't simply start developing something new without a good old `hello world` project, right?

`Insert Clever One Does Not Simply... Meme Here`

Well this post is that `hello world` and goes to show that in the expansive world that is technology, there's always something new to learn!

So, here we begin!

Since setting up this site with Github Pages is a new one for me, I think it appropriate that my first post covers what I've learned from getting my personal github pages up and running.

## Why am I starting this project?
I've long been considering starting some sort of blog to share some of my experiences to help me process and retain what I've learned as well as help others who may be just getting started on a particular topic. With this blog on Github Pages, I hope to finally start doing something about that. Not only because, "Sharing is Caring", but also since I know the power and value of reteaching what you have learned. Reteaching and recording what you've learned helps you to not only "get by" with what you've learned, but to think critically, drill further into it, expand it, and organize that knowledge in a way that it can be understood by others. Doing so also really cements your own understanding in a topic as well.

And I wanted to learn how to use github pages and this was a great excuse!

## Getting Started with GitHub Pages
I find that often times when I read blogs or online recipes, I feel like the authors spend a lot of time providing backstory and background before getting into the meat and potatoes of the topic. In order to keep myself from doing the same to you, I'd like to preload you with some of the links to the resources that I found most helpful getting myself started first.

- <a href="https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll?platform=linux">GitHub Docs: Create site with Jekyll</a>
- <a href="https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll">GitHub Docs: Test site locally with Jekyll</a>
- <a href="https://programmerah.com/solved-jekyll-install-error-cannot-load-such-file-webrick-loaderror-39104/">ProgrammerAH: [Solved] Jekyll Install Error: cannot load such file — webrick (LoadError)</a>

I encourage you to read-on to see where each of these come into play, but to each their own! I understand that everyone learns differently and the path to success isn't always a linear one.

### What will we be building with this project
In this project we'll be building my basic personal GitHub Pages site with Jekyll using a GitHub Free account.

Jekyll is a static site generator which takes text written in a variety of markup languages and uses layouts to create a site. It allows for 

### What you'll need to before starting this project

- WSL or Linux recommended (I used a debian WSL on Windows 11)
- A GitHub Account
- GitHub CLI

### 1. Create a public repo
Create a new repository in your personal account and name the repository `<username>.github.io`. We'll also tell github to add a README.md.

This repository is where all the source and site contents will be stored. Later we'll adjust the repository settings so that GitHub will automatically publish changes made to a specific branch.

### 2. Clone the repo

Now open a terminal and clone your newly created repo (personally like to use VS code for my development), the command you run should look something like this:

`gh clone repo <username>.github.io`

If you've never run your github CLI before, you may not be logged in, to log in to git, use the following and then follow the prompts:

`gh auth login`

### 3. Install tools and dependencies

Now that you've got a repo, we've got to install some dependencies before we can start building our site. For my site, I'm going to use a static site generator supported by GitHub Pages called Jekyll.

I have a debian WSL, so to install the dependencies for Jekyll, I need to run the following commands:

`sudo apt-get install ruby-full build-essential zlib1g-dev`

Let's make sure ruby and gem installed correctly, the following command should return a version:

`gem -v`

Success! Finally, let's install Jekyll and bundler:

```
echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
gem install jekyll bundler
```

That should be it for our dependencies for now, let's go ahead and initialize out Jekyll site!

### 4. Create new Jekyll site and modify defaults

To start a new site, we can use jek

### 5. Test your site locally

### 6. Create a branch to push your changes to before they are published

### 7. Push your changes

### 8. Configure your GitHub Pages source

### 9. Publish your changes to your site

