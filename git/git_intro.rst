
.. _git_intro:

****************
Collab using git
****************


Basic configuration after installation
======================================

Basic configure::

  git config --global user.name "your_name"
  git config --global user.email your_email_address

then check if the configuration applied::

  git config --list

detailed reference:

http://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup

Build git repository
====================

build, at the root of project directory::

  git init

then add all files::

  git add -A 

then commit::

  git commit -m "add all"

detailed reference:

Connect to Github
=================

add remote server, with shortname lecthub::

  git remote add lecthub https://github.com/anyonsites/xmulect.git

and the creation of remote could be checked::

  git remote -v

before push the local repo to remote, first pull to merge the two::

  git pull

then push the local to remote repo::

  git push lecthub master

detailed reference:

http://git-scm.com/book/en/v2/Git-Basics-Working-with-Remotes


References:
===========

* Useful tips:
  http://sixrevisions.com/web-development/git-tips/

* Tower's learning eBook:
  http://www.git-tower.com/learn/ebook/command-line/introduction

* Pro Git book on Git official site:
  http://git-scm.com/book/en/v2


