---
title: "Git: Git Tutorial"
header:
  image: assets/images/git.png
  caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
tags:
  - table of contents
toc: true
toc_label: "Git Tutorial"
toc_icon: "heart"
---
## Types of version controlle systems?
The types of VCS are:
  * Local Version Control System
  * Centralized Version Control System
  * Distributed Version Control System

## Local Version Control System?
## Centralized Version Control System?

![Smithsonian Image]({{ site.url }}{{ site.baseurl }}/assets/images/cvcs.png)
{: .image-left}

A centralized version control system has a single server that contains all the file versions. This enables multiple clients to simultaneously access files on the server, pull them to their local computer or push them onto the server from their local computer. This way, everyone usually knows what everyone else on the project is doing. Administrators have control over who can do what.

This allows for easy collaboration with other developers or a team.

The biggest issue with this structure is that everything is stored on the centralized server. If something were to happen to that server, nobody can save their versioned changes, pull files or collaborate at all. Similar to Local Version Control, if the central database became corrupted, and backups haven't been kept, you lose the entire history of the project.

The most well-known examples of centralized version control systems are Microsoft Team Foundation Server (TFS) and SVN.
## Distributed Version Control System?

![Smithsonian Image]({{ site.url }}{{ site.baseurl }}/assets/images/dvcs.png)
{: .image-right}

With distributed version control systems, clients don’t just check out the latest snapshot of the files from the server, they fully mirror the repository, including its full history. Thus, everyone collaborating on a project owns a local copy of the whole project, i.e. owns their own local database with their own complete history. With this model, if the server becomes unavailable or dies, any of the client repositories can send a copy of the project's version to any other client or back onto the server when it becomes available. It is enough that one client contains a correct copy which can then easily be further distributed.

Example of distributed version control systems are:
  * Git
  * Mercurial
  * Monotone

## Who created Git?
Git was created by Linus Torvalds in 2005 on the road to develop Linux Kernel.

## Which language is used in Git?
C language. C language makes Git fast

## What is the use of git clone command?
The git clone command creates a copy of the existing central Git repository into your local machine.

## What is Git?
Git is a Version Control System. Version Control System is basically software designed to record changes within one or more files over time. It allows us to undo or to cancel all made or pending changes within one or more files. If we're working on a project with many files, VCS enables us to control the whole project. If necessary, this allows us to revert one or more files any of their previous versions or the whole project to a previous version. We can also compare changes to one file between two versions in order to see exactly what was changed in each file, when it was changed and who made the change. We can also see why the change was made.

Why am I mentioning files instead of code? Because Git is a universal system that can be used for version control of all types of files, be it Microsoft Word files, pictures, AutoCAD files, Visual Studio Project, etc.

## Mention some Git Repository Hosting Services.
* Github
* Gitlab
* BitBucket

## Name some Basic Operations in Git.
* Init
* Add
* Commit
* Push
* Pull

## How to check git Installation version?
```console
git --version
```
## Git config levels?
There are thre different configuration levels in the Git. 
  * Local(default)
  * Global
  * System

Git has a command called `config` which can accept arguments, those arguments are listed above.

`--local` will apply only for that repository.
```console
git config --local
```
`--global` will apply to all repositorys.
```console
git config --global # foll all repos
```
`--system` will apply to all system user, for all users that are using this machine.
```console
git config --system # for all system users
```

## Basic Configuration
After we install git, we need to tell git who we are, since every Git commit will use this information to identify you as the author.The following git commands allow us to make basic git configuration.

User name
```console
git config --global user.name "Your full name"
```
Example:
```console
git config --global user.name "Besfort Bunjaku"
```
Email address
```console
git config --global user.email "your email address"
```
Example:
```console
git config --global user.email "bessffort@gmail.com"
```
It is worth to know that we can make other configuration, for example: setting up color to show in git console, or editor that will open when we wont to compare tow files...
For now we stay with basic config.

## Initialize a git repository?
After we create a project folder,we need to tell git to watch this folder. We can do this by using` git init`,after that git is aware of our project, and it will create a `.git` hidden folder inside it.

```console
git init
```

## Git Workflow
There are four phases in the Git Workflow.
* Working directory
* Staging area (index)
* Local repository (Head)
* Remote repository (Master)

`Working directory` is the directory that contains all our project files.
![Smithsonian Image]({{ site.url }}{{ site.baseurl }}/assets/images/git1.png)
{: .image-right}

## What does git add command do?
This command adds files and changes to the index or staging area.
```console
git add .     # add everything to staging area "." dot refers to current working directory.
```
```console
git add --all     # add everything to staging area, same commend as above.
```
```console
git add foo.py     # add one file to staging area.
```
```console
git add foo.py,bar.py    # add list files to staging area.
```
## Notices

**Watch out!** You can also add notices by appending `{: .notice}` to a paragraph.
{: .notice}