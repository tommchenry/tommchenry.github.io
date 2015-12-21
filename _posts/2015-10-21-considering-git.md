---
layout: post
title: Considering Git
---

#Considering Git

##Week 1 Technical Blog

####October 21, 2015

**What are the benefits of version control?**

Version control is a more robust way of saving your work over time. Where traditional saving overwrites the same file over and over, wiping away what the file used to say with what it says now, version control keeps a library of all the committed file states that have existed since the version control was first initialized. What's more it's not doing this for just one file in a project, but all the files specified for a given project, giving you access to the entire project as a timeline of changes, any one of which can be referenced again later.

Version control also makes it easier for large teams to collaborate on projects, since anyone can copy the library of versions so far and start creating new branches to add updates or changes to what's been done.

**How does git help you keep track of changes?**

Git helps you track the changes that have been made to all files in a repository through git log. Here you can see all the commit messages, which (ideally) lay out what was added and updated in each successive commit, and who performed that commit. Git also tracks the number of lines that have been added or deleted, and allows you to check out any of these earlier commits and compare it to the commit you're currently working on.

**Why use GitHub to store your code?**

Github is a giant centralized directory of repositories. It's not only a handy (and free) offsite backup for your work, but also a way to track much of the same information you'd find in command line git in a pleasing graphical format, to find collaborators and similar projects, and to make your code available to interested users.