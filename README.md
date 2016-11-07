# Git Portable for Dummies

A guide by H00G3

### Note

This tutorial is purely for personal use only. I wrote this so I could understand it, but you're free to use it too. If you have any questions, google your problem.

## Contents

- [Connect Git Portable to your Github account](#connect-git-portable-to-your-github-account)
- [Clone a repository](#clone-a-repository)
- [Commit changes to a repository](#commit-changes-to-a-repository)

## Connect Git Portable to your Github account

### Prerequisites

- [Git Portable](https://github.com/sheabunge/GitPortable) installed somewhere (This guide is based on v2.9.2 dev test 1)
- A logged in [Github account](https://github.com/)

### Tell Git who you are

`$ git config --global user.name "<first and last name>"`

`$ git config --global user.email <your email address>` (Must be the same email connected to your Github account)

### Generate a new SSH key

`$ ssh-keygen -t rsa -b 4096 -C "<your email address>"` (Must be the same email connected to your Github account)

Select a directory to place the key in

type a secure passphrase

### Add your newly created SSH Key to your Github account

Copy the SSH key to your clipboard (key can be found at Data/home/.ssh/id_rsa.pub)

Open [Github](https://github.com/)

[Go to the SSH and GPG tab in Settings.](https://github.com/settings/keys)

Click the New SSH key button

Paste the SSH key and title it

Add the key

### Test SSH connection

`$ ssh -T git@github.com`

## Clone a repository

### Prerequisites

- The repository has already been created on Github
- [Connect Git Portable to your Github account](#connect-git-portable-to-your-github-account) completed

### Copy the SSH remote url

Open the website of the repository you want to clone

Click the Clone or download button

copy the SSH remote url to your clipboard

### Clone the repository in Git

`$ git clone <paste SSH remote url here>`

The cloned repository can be found in the Git Portable files (search for it if you can't find it!)

## Commit changes to a repository

### Prerequisites

- [Clone a repository](#clone-a-repository) completed

### Git commands

`cd <repository name>`

`git add .`

`git commit -m "<write a commit message>"`

`git push`

## Resources

https://help.github.com/articles/generating-an-ssh-key/

https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/

https://help.github.com/articles/testing-your-ssh-connection/
