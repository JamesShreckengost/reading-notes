# Revsions and the cloud
 
 ## Prerequisites
  * Have a solid understanding of terminal
 ## Version Control
  * allows you to revisit various versions of a file ore set of files
  * can revert a file or project to a previous version
  * mistakes with files can easily be rectified
  * Centrailzed version control - allows a developer team on a single file or set of files
  * Distributed Version Control - addresses the major vulnerability of the CVS: the server as a single point of failure
  * what is git? - Snapshots, Local Operations, Tracking Changes, Loss of data, States: committed, modified, and staged
 ## History of Git
  * made using dvcs called BitKeeper in 2002.
  * Linus Torvalds, the cheief architect of the Linux kernel, began creating git
 ## Getting started
  * Terminal
  * git website
  * github
 ## Setting up a git repository 
  * Importing - 
       * switch to the target project's directory
         Example: cd test (cd = change directory)
       * Use the git init command 
         Example: git init
       * git add -m "message"
    Cloning - 
       * you can create a copy of an exisiting Git repository
        Example: git clone https://github.com/test
 ## Workflow
  * Local Repository Structure 
    1. Working Directory: The actual files reside here
    2. Index: The area used for staging
    3. Head: Points to the most recent commmit
  * Saving Changes
    * Tracked - tracked files cna be modified, unmodified, or staged
    * Untracked - untracked files were not in the last snapshot and do not currently reside in the staging area
  * Check File Status
    * Example: git status
  * Tracking and Staging a new file
    * single file
      git add filename
    * all files
      Example: git add *
  * Commitng a file
    * Example git commit -m "made change"
  * Committing all changes
    Example: git commit -a
  * Pushing changes
    Example: git push origin main    
 ## Remote repository 
  * Cloned Repositories - git will automatically give the name origin to the server that you cloned and the master to your local brand
  * Seeing your remotes 
    * By running the git remote command, you can view the short names of all specified remote handles
    * By using git remote -v you can view all remote URLs next to their correspong short names
  * Adding remotes 
    * To create a new remote Git repository with a short name use:
    git remote add shortname url
  * Fetching - Fetching entails pulling data that you don't have from a remote project
    git fetch [remote-name]  
  * Pushing - push your changes "upstream" for sharing use:
    git push [remote-name][branch-name]  
    Example: git push origin master

