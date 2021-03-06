Learn to Use Git for Reproducible Research
========================================================
author: JungHwan Yang
date: September 11, 2015
font-family: 'Consolas'

What is Git?
========================================================

- Git is a version control system.

What is version control and why should you care?
========================================================
left: 45%
![PhD Comics](http://phdcomics.com/comics/archive/phd101212s.gif)
***
Version control is a system that records changes to a file or set of files over time so that you can recall specific versions later. For the examples in this book you will use software source code as the files being version controlled, though in reality you can do this with nearly any type of file on a computer.


Version Control Workflow
========================================================

![Version Control Workflow](https://www.vodori.com/blog/wp-content/uploads/2013/07/choosing-the-right-repository-svn-or-git-1.png)

Example: [R syntax](https://bitbucket.org/junghwanyang/irg-unfriending/src/93ad5c47ed430d157d1ba763df63419b9995b97a/Unfriending%20Colombia%202012%20-%20December%202014.Rmd?at=master&fileviewer=file-view-default)


Install Git on your local machine
========================================================

Windows user: [https://git-for-windows.github.io/](https://git-for-windows.github.io/)
Mac user: [http://git-scm.com/download/mac](https://git-for-windows.github.io/)

Open your terminal
========================================================

Learn how to:
- Browse directory
- List files
- Make a directory
- Remove a file and/or a folder
- Find a manual

Open your terminal
========================================================

Learn how to:
- Browse directory: cd
- List files: ls
- Make a directory: mkdir
- Remove a file and/or a folder: rm, rm -rf
- Find a manual: man

Check Setup
========================================================

Open a terminal window and type these commands, pressing enter after each one:
- `git --version`

If your setup is correct, the `git` version identifiers will be shown on your screen.

Make Changes from Anywhere (Github)
========================================================

The following material is largely from [UW-Software Carpentry Workshop] (https://github.com/UW-Madison-ACI/boot-camps/blob/2015-06-03/version-control/git/github/Readme.md)

## GitHub.com?

GitHub is a site where many people store their open (and closed) source
code repositories. It provides tools for browsing, collaborating on and
documenting code.

## GitHub password 

Setting up GitHub requires a GitHub user name and password.  Please take a
moment to [create a free GitHub account](https://github.com/signup/free).

Git configuration
========================================================

```
git config --global user.name "Your Name"

git config --global user.email email@youremail.com

git config --list
```

Create a Repository on github.com
========================================================

Go to your github page and click create a repository

Link your local machine with github.com
========================================================

```
echo "# MLW git exercise" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/junghwanyang/MLW.git
git push -u origin master
```

[Find more information](https://help.github.com/articles/set-up-git/)

Create a folder and a file on your local machine
========================================================

- Make a folder named *git_exercise*
- Make a file named *sample.txt*

git diff, add, commit, and push
========================================================

```
git diff
git add filename1 filename2 (git add *)
git reset
git commit -m 'make a comment'
git push origin master
```

If you don't want to push everything in a folder
========================================================

## You can make an exception!

```
touch .gitignore
echo '*.log' > .gitignore
git add 
git add .gitignore
git commit -m "list of ignored files"
```

More resources
========================================================
[Git Documentation](https://git-scm.com/documentation)
[Git Cheat Sheet](https://training.github.com/kit/downloads/github-git-cheat-sheet.pdf)
