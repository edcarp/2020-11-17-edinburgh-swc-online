---

theme: sky
revealOptions:
    slideNumber: true

---

# Git

Mario Antonioletti (mario@epcc.ed.ac.uk)


Note: To run:
```
npm install -g reveal-md. # If it requires installing (assumes npm is installed)
reveal-md ./git-slides.md
```
The default markdown-md keyboard shortcuts are:

* Up, Down, Left, Right: Navigation
* f: Full-screen
* s: Show slide notes
* o: Toggle overview
* . (Period or b: Turn screen black
* Esc: Escape from full-screen, or toggle overview

---

### Scenario

<img src="imgs/PhDcomic.png" alt="PhD Comic" style="background:none; border:none; box-shadow:none;">
<small>
From: http://www.phdcomics.com/comics/archive.php?comicid=1531
</small>

----

### More working scenarios

* Want to work on files across different systems
   * e.g. home PC, your laptop, work PC, Eddie, ...
   * How do you keep files synchronized?
* Want to know the provenance of your files
   * Need to check previous code version
   * Who did what/when?
* Back-up precious files
   * Laptop stolen/disk fails/recover deleted files
* You want to be able to collaborate


----

### Version control can help!

* Also known as  *revision control* or *source control*
  * There are others: SVN, mercurial, ...
* Records &  preserves history of changes to files
* Not just for source code:
  * Configuration files
  * Parameter sets
  * Data files (git lfs for large files)
  * User documentation & manuals
  * Conference/journal papers/book chapters

----

### With version control you can...

* Keep track of changes
   * Lab notebook for code/documents
* Roll back to points in the change history
* Back up history of changes to various locations
* Work on files from multiple locations/systems
* Identify and resolve conflicts
   * Same file edited in the same place by more than one user
* Collaborate on code/documents/other files

---

### What we will cover ...

1. Tracking changes with a local repository

2. Working with a remote repository

3. Collaborating with colleagues using a repository

4. A little on branching

----

### You can get dedicated git GUIs

<img src="imgs/DedicatedGitClient.png" alt="git GUI client." style="background:none; border:none; box-shadow:none;">
<small>
SmartGit (https://www.syntevo.com/smartgit/),free for non-commercial use.</small>


----

### Or as part of an IDE

<img src="imgs/Rstudio.png" alt="Rstudio client." style="background:none; border:none; box-shadow:none;">
<small>
Rstudio (https://www.rstudio.com/)
</small>

* But we will use git from the shell

----

### Why use the shell ?

* All IDEs/GUIs use shell commands
* GUI may not be available remotely
* You can still use a GUI locally
   * Use git on remote machine
* But you have a choice
   * Easier: command line -> GUI

---

###  Initiatialise local repository

1. Tell git who you are (only once):
    * email address 
	* your name
2. Initialise a repository (only do once).
3. You **add** files to your local repository
4. Files are then in one of the following states:
    * **untracked** - repo does not know them
    * **tracked** - you have *add*ed them
       * **unmodified** - tracked file not changed 
       * **modified** -  tracked files changed
    * **staged** - about to add to the repository

----

### States

<img src="imgs/DevCycle.png" alt="git GUI states." style="background:none; border:none; box-shadow:none;">

----
## FAIR Data/Software

Observing these will make you a better researcher:

* **F**indable, e.g. use DOIs and registries
* **A**ccessible, e.g. use open non-propretioritary formats to access software/data.
* **I**nteroperable,
* **R**eusable, think of reproducible

Using repositories take you  a long way (but not all). For more details see [Towards FAIR principles for research software](https://content.iospress.com/articles/data-science/ds190026) or these [slides](https://fair-software.nl/).

----
## Let's start ...

---

## Setting up remote repositories

----

### Service Providers


* *University GitLab* (https://git.ecdf.ed.ac.uk/)
* *GitHub* (https://github.com)
* *Bitbucket* (http://bitbucket.org)
* *GitLab* (https://about.gitlab.com)
* *Launchpad* (https://launchpad.net)
* *SourceForge* (http://sourceforge.net)
* ….

For more options see: https://git.wiki.kernel.org/index.php/GitHosting

---

# GitLab

----

## Sign in to University GitLab

* Go to https://git.ecdf.ed.ac.uk
* Sign in with your EASE credentials

<img src="imgs/GitLab.png" alt="Sign up to GitHub 1" style="background:none; border:none; box-shadow:none;">

----

## Create a new project (1)

<img src="imgs/GitLabNewProject.png" alt="Sign up to GitHub 1" style="background:none; border:none; box-shadow:none;">

----

## Create a new project (2)

<img src="imgs/GitLabNewProject2.png" alt="Sign up to GitHub 1" style="background:none; border:none; box-shadow:none;">

----

## Create a new project (3)

* Provides you with information on what to do.
* Let's try it out...

---

# GitHub

----

### Create new account on GitHub (1)

<img src="imgs/SignUp.png" alt="Sign up to GitHub 1" style="background:none; border:none; box-shadow:none;">

----

### Create new account on GitHub (2)

<img src="imgs/SignUp2.png" alt="Sign up to GitHub 2" style="background:none; border:none; box-shadow:none;">

Verify Your email address


----

### Create a new repository

<img src="imgs/NewRepository.png" alt="Create a new repository" style="background:none; border:none; box-shadow:none;">


---

## Branching

----

## What is this master thing?

<img src="imgs/master.png" alt="Better Software, Better Research" style="background:none; border:none; box-shadow:none;">

----

## Why branch?

* Start with your first commit:

<img src="imgs/branch01.png" alt="First commit" style="background:none; border:none; box-shadow:none;">

----

### Add another commit

<img src="imgs/branch02.png" alt="Second commit" style="background:none; border:none; box-shadow:none;">

----

### Code ready, tag and release

<img src="imgs/branch03.png" alt="Tag and release" style="background:none; border:none; box-shadow:none;">

----

### Branch at the release point

<img src="imgs/branch04.png" alt="Branch" style="background:none; border:none; box-shadow:none;">

----

### Continue development

<img src="imgs/branch05.png" alt="Fourth commit" style="background:none; border:none; box-shadow:none;">

----

### Continue working ...

<img src="imgs/branch06.png" alt="Fourth commit" style="background:none; border:none; box-shadow:none;">

----

###  Bug Identifed also in the first release

<img src="imgs/branch07.png" alt="Bug found" style="background:none; border:none; box-shadow:none;">

----

### Fix bug in release branch

<img src="imgs/branch08.png" alt="Bug fixed" style="background:none; border:none; box-shadow:none;">

----

### Tag and release

<img src="imgs/branch09.png" alt="New release" style="background:none; border:none; box-shadow:none;">

----

### Merge fix to the main branch

<img src="imgs/branch11.png" alt="Merge back" style="background:none; border:none; box-shadow:none;">

----

## Popular model

* A release branch, representing a released version of the code.

* A master branch, representing the most up-to-date stable version of the code.

* Various feature and/or developer-specific branches representing work-in-progress, new features, etc.

----

## Example

* Can have more complex topologies:

<img src="imgs/branch-model.png" alt="Better Software, Better Research" style="background:none; border:none; box-shadow:none;">

---

## Recap

What we have learnt:
* Know how to create remote repositories.
* Know how to clone repositories.
* Know how to push content to the repository.
* Know how to fetch and merge or pull content.
* Know how to resolve conflicts.

----

### **pull**ing content (fetch and merge)

<img src="imgs/merge.png" alt="Merging content"
     style="background:none; border:none; box-shadow:none;">

----

### Conflict

<img src="imgs/conflict.png" alt="Conflicting content"
     style="background:none; border:none; box-shadow:none;">

----

### More stuff

Not enough time to cover:

* Forking code
* For public repositories, LICENCE your code
   * Permissive: BSD, Apache, ...
   * Viral: GPL, ... 

----

### Cloning

<img src="imgs/fork1.png" alt="Cloning" style="background:none; border:none; box-shadow:none;">

----

### Forking

<img src="imgs/fork2.png" alt="Fork" style="background:none; border:none; box-shadow:none;">

----

### Pull request

<img src="imgs/fork3.png" alt="Fork" style="background:none; border:none; box-shadow:none;">

----

## Hopefully not

<img src="imgs/xkdc1597.png" alt="Better Software, Better Research" style="background:none; border:none; box-shadow:none;"><br/>

<small>
From: http://xkcd.com/1597/
</small>


---


## What do we now know

* Know how initialise a local repository
* How to add files
* How to commit files
* How to navigate between different versions
* How look at the file log
* How to tag files
* Know what a branch is

----

## Further information

* Visual Git Reference - pictorial representations of what Git commands do (http://marklodato.github.io/visual-git-guide/index-en.html).
* Pro Git - the "official" online Git book (http://git-scm.com/book)
* Version control by example - an acclaimed online book on version control by Eric Sink (http://www.ericsink.com/vcbe/index.html)

---

## End
