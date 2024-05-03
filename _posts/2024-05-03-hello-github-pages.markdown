---
layout: post
title:  "Hello Github Pages!"
date:   2024-05-03 07:56:00 -0700
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
source ~/.bashrc
gem install jekyll bundler
```

That should be it for our dependencies for now, let's go ahead and initialize out Jekyll site!

### 4. Create new Jekyll site and modify defaults

To start a new site, we can use the jekyll CLI to create the basic structure of a new Jekyll site:

`jekyll new --skip-bundle .`

After we have the basic structure down, we're going to modify some default dependencies for our site to make it compatible with GitHub pages.

In _config.yml

1. Update the title of our site
2. Update the description of our site
3. Update the domain, url, and baseurl of our site

In Gemfile

1. Remove or comment out the following line:

`gem "jekyll"`

2. Replace the line starting with `# gem "github-pages"` with the following:

`gem "github-pages", "~> 231", group: :jekyll_plugins`

### 5. Test your site locally

To test our site locally, we first need to install our updated dependencies that we added to the Gemfile file. We can do so by using bundle install command installed with ruby earlier:

`bundle install`

Finally to run our site locally so we can preview it, we can run jekyll serve with bundle:

`bundle exec jekyll serve`

<strong>NOTE:</strong> If you run into an issue where there is an issue using webrick and the server can't start, you can fix the issue by running:

`bundle add webrick`

And then retry starting your local development server:

`bundle exec jekyll serve`

If all has gone correctly, this will start a development server locally at http://127.0.0.1:4000 where we can preview our site as we modify our files and develop our site!

### 6. Create a branch to push your changes to before they are published (optional)

Finally, if you'd like to follow some sort of software development lifecycle paradigm like <a href="https://www.gitkraken.com/learn/git/git-flow">git flow</a>, <a href="https://www.atlassian.com/continuous-delivery/continuous-integration/trunk-based-development">trunk based development</a>, or your own method, I'd recommend making a new branch to which you can commit your ongoing changes as you build out posts or part of your site.

To follow a git flow like process we'll start a develop branch to commit our work to so far:

`git checkout -b 'develop`

Then we'll add all our changes, commit, and then push them to load our changes into GitHub.

```
git add -A
git commit -m "Initial Commit"
git push origin develop
```

In order to follow our flow process, we could also then optionally change our branch again as we work on setting up our first customizations and first post.

`git checkout -b 'feature/post-1'`

### 7. Configure your GitHub Pages source

So far we have made a new repo, setup a blank Jekyll site, setup our development environment, setup new branches, and pushed some code. Next, we'll configure the settings on the GitHub repository so that GitHub knows how and where to publish our pages from.

Navigate to your repository on GitHub and go to the <strong>Settings</strong> tab.

On the left hand navigation, there should be a <strong>Pages</strong> section, select it.

On this page, we will set the following options:

<strong>Source:</strong> Deploy from a branch

<strong>Branch:</strong> main, /(root)

### 8. Publish your changes to your site

Finally, in order to bring your changes live, open a pull request and merge your changes from the develop branch to the main branch. Once the merge is complete, your new site should be live!

Navigate to <username>.github.io and see how it looks!

## Conclusion
That's it for this post, I hope it's useful in helping you get your Jekyll GitHub page up and running!

Keep an eye out for a follow up posts where we'll talk about adding posts, themes, and customizing the home page.

As I complete them, I'll add links here:

Dgeebs out!