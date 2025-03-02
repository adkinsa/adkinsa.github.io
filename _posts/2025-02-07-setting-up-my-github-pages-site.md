---
title: Setting up my GitHub Pages site
date: 2025-02-07 11:34 PM
categories: [GitHub Pages]
tags: [github pages, jekyll, chirpy]
---

In this post I'm going to go over how I set up my website with Jekyll and GitHub Pages. I've always been curious about GitHub, so I figured this project would be a fun way to create my site and learn more about GitHub in the process. Since this is the first website I have created, I knew it was going to be a learning process, but I was up for the challenge.

## Prerequisites
To set up a local testing environment I installed the following tools:
* <a href="https://git-scm.com/downloads" target="_blank">Git</a>
* <a href="https://rubyinstaller.org/downloads/" target="_blank">Ruby</a>
* Jekyll
* <a href="https://code.visualstudio.com/download" target="_blank">VS Code</a>

## Step 1: Install prerequisites
* **Install Git** - First, I installed <a href="https://git-scm.com/downloads" target="_blank">Git</a>.
* **Install Ruby** - Next, I installed <a href="https://rubyinstaller.org/downloads/" target="_blank">Ruby</a>. Once the Ruby installation setup was complete, I chose **"Run ridk install"** and clicked finish. Then, this command prompt window opened:
![Ruby installer 2 for Windows command prompt](https://res.cloudinary.com/do8uy1fxa/image/upload/v1738935315/ridk-install-command-prompt_pwhghq.png)
In the command prompt window, I installed all 3 components one at a time by entering the number and pressing enter.
* **Install Jekyll** - To install **Jekyll**, I opened a command prompt and ran the command `gem install jekyll`.
* **Install VS Code** - Lastly, I installed <a href="https://code.visualstudio.com/download" target="_blank">VS Code</a>.

## Step 2: Create a GitHub account
The next thing I did was create a GitHub account.

## Step 3: Create a new repository
Next, I created a new repository using the <a href="https://github.com/cotes2020/jekyll-theme-chirpy" target="_blank">Chirpy</a> Jekyll theme by going to the <a href="https://github.com/cotes2020/chirpy-starter" target="_blank">chirpy-starter</a> repository and clicking "use this template" and "create a new repository". You can find other themes by visiting one of the many Jekyll theme sites listed <a href="https://jekyllrb.com/docs/themes/" target="_blank">here</a>.
![chirpy-starter repository page](https://res.cloudinary.com/do8uy1fxa/image/upload/v1738935201/chirpy-starter-repo_z4sxnz.png)

On the "create a new repository from chirpy-starter" page, I named the repository `adkinsa.github.io`.

## Step 4: Make initial configuration changes
Now that the repository was created, I needed to make some initial configuration changes.
* **Add url to _config.yml** - First, I added my github pages url to the `_config.yml` file.
* **Change build and deployment source** - Lastly, I went to settings, pages, and changed the build and deployment source to **GitHub Actions**.

## Step 5: Clone repository
The next thing I did was clone the repository to my local machine. First, I created a folder for the repository, then right clicked the folder and selected "Git Bash Here". Next, I copied the local clone https link and ran the command `git clone https://github.com/adkinsa/adkinsa.github.io.git` in the bash terminal. Once the repository was cloned I opened it in VS Code.

## Step 6: Install dependencies
To install the necessary dependencies, I opened a terminal in VS Code and ran the command `bundle`.
![Repository open in VS Code running bundle command in terminal](https://res.cloudinary.com/do8uy1fxa/image/upload/v1738935300/local-repo-opened-in-vscode_o7cbte.png)

## Step 7: Test site locally
To preview the site, I ran the command `bundle exec jekyll s` in the VS Code terminal and went to the local server address `http://127.0.0.1:4000/`.

## Step 8: Push changes to GitHub
Finally, I pushed the changes I made to the site by running the following code:
```shell
git add .
git commit -m 'commit message'
git push origin main
```