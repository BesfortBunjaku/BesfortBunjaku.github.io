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

## Local Version Control System
## Centralized Version Control System

![Smithsonian Image]({{ site.url }}{{ site.baseurl }}/assets/images/cvcs.png)
{: .image-left}

A centralized version control system has a single server that contains all the file versions. This enables multiple clients to simultaneously access files on the server, pull them to their local computer or push them onto the server from their local computer. This way, everyone usually knows what everyone else on the project is doing. Administrators have control over who can do what.

This allows for easy collaboration with other developers or a team.

The biggest issue with this structure is that everything is stored on the centralized server. If something were to happen to that server, nobody can save their versioned changes, pull files or collaborate at all. Similar to Local Version Control, if the central database became corrupted, and backups haven't been kept, you lose the entire history of the project.

The most well-known examples of centralized version control systems are Microsoft Team Foundation Server (TFS) and SVN.
## Distributed Version Control System

![Smithsonian Image]({{ site.url }}{{ site.baseurl }}/assets/images/dvcs.png)
{: .image-right}

With distributed version control systems, clients don’t just check out the latest snapshot of the files from the server, they fully mirror the repository, including its full history. Thus, everyone collaborating on a project owns a local copy of the whole project, i.e. owns their own local database with their own complete history. With this model, if the server becomes unavailable or dies, any of the client repositories can send a copy of the project's version to any other client or back onto the server when it becomes available. It is enough that one client contains a correct copy which can then easily be further distributed.

Example of distributed version control systems are:
  * Git
  * Mercurial
  * Monotone

## What is Git?

Git is a Version Control System. Version Control System is basically software designed to record changes within one or more files over time. It allows us to undo or to cancel all made or pending changes within one or more files. If we're working on a project with many files, VCS enables us to control the whole project. If necessary, this allows us to revert one or more files any of their previous versions or the whole project to a previous version. We can also compare changes to one file between two versions in order to see exactly what was changed in each file, when it was changed and who made the change. We can also see why the change was made.

Why am I mentioning files instead of code? Because Git is a universal system that can be used for version control of all types of files, be it Microsoft Word files, pictures, AutoCAD files, Visual Studio Project, etc.
## Git Install?

You can download Git for free, and install it in computer.To check if installation was sucesfull, we can type the followin command in console.

```console
git --version
```
## Tell git who you are
After we install git, we need to tell git who we are, since every Git commit will use this information to identify you as the author.There are thre different configuration levels in the Git. 
  * Local(default)
  * Global
  * System
Git has a command called `config` which can accept arguments, those arguments are listed above.

Local will apply only for that repository.
```console
git config --local
```
Global will apply to all repositorys.
```console
git config --global # foll all repos
```
System will apply to all system user, for all users that are using this machine.
```console
git config --system # for all system users
```
## Basic Configuration
The following git command allowe us to make basic git configuration

```console
git config --global user.name "Your full name"
```
Example:
```console
git config --global user.name "Besfort Bunjaku"
```

```console
git config --global user.email "your email address"
```
Example:
```console
git config --global user.email "bessffort@gmail.com"
```
It is worthe to know that we can make other configuration, for example: setting up color to show in git console, or editor that will open when we wont to comapre tow files...
For now we stay with basic config.
## Git Workflow
There are four phases in the Git Workflow.
* Working directory
* Staging area (index)
* Local repository (Head)
* Remote repository (Master)

## Initialize a git repository
## Notices

**Watch out!** You can also add notices by appending `{: .notice}` to a paragraph.
{: .notice}