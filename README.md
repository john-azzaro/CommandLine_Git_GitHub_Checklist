# Git Bash, Git, and GitHub Checklist

**Table of Contents**

* [Git Bash Checklist](#Command-Line-Checklist)
   * [Basic Commands](#Basic-Commands)
   * [Display Git Help](#Display-Git-Help)
   * [Establishing Location](#Establishing-Location)
   * [Creating New Directories and Files](#Creating-New-Directories-and-Files)
   * [Navigating Directories](#Navigating-Directories)
   * [Listing Directory Contents](#Listing-Directory-Contents)
   * [Moving Files and Folders](#Moving-Files-and-Folders)
   * [Copying Files and Folders](#Copying-Files-and-Folders)
   * [Deleting Files and Directories](#Deleting-Files-and-Directories)

* [Git Version Control](#Git-Version-Control)
   * [Working with Branches](#Working-with-Branches)
   * [Moving between Branches (or Master)](#Moving-between-branches-(or-master))
   * [Merging Branches (and Manage Conflicts)](#Merging-Branches-(and-Manage-Conflicts))
   * [Cloning a Repository (and pushing to GitHub)](#Cloning-a-Repository)
   * [Pulling Upstream Changes](#Pulling-Upstream-Changes)

* [Version Control Step-by-Step](#Version-Control-Step-by-Step)
   * [Setting Up Your Project](#Setting-Up-Your-Project)
   * [Initializing Your Project as a Git Repository](#Initializing-Your-Project-as-a-Git-Repository)
   * [Committing Staged Changes](#Committing-Staged-Changes)
   * [Uploading Local Repository to GitHub](#Uploading-Local-Repository-to-GitHub)


   


# Command Line Checklist

## Basic Commands
* ```   cd       ``` **Change directory** *(used to move from one directory to another).*

* ```   pwd      ``` **Print working directory** *(used to find your current location).*

* ```   ls       ``` **List contents of directory** *(used to print out contents of the directory you are currently in).*

* ```   mkdir    ``` **Make a new directory** *(used to create a new directory).*

* ```   touch    ``` **Create an empty file** *(used to create a new file with a given name).*

* ```   rm       ``` **Remove a file** *(used to remove a file or folder).*

* ```   rmdir    ``` **Remove a directory** *(used to remove a directory).*

* ```   mv       ``` **Move a file** *(used to move a file or directory).*

* ```   cp       ``` **Copy a file** *(used to copy a file or directory).*

* ```   clear       ``` **Clear the window** *(used to clear all commands and start with a fresh window).*

<br>

## Display Git Help
* **To display help information about Git**
   ``` 
   git --help
   ```
 <br> 
 
## Establishing Location

* **To show your current location:** 
   ```   
   pwd  
   ```
   
* **To return to your user account home folder**
   ``` 
   cd ~ 
   ```
 <br>
 
## Creating New Directories and Files

* **To create a new directory:**
    > *note: this will make a new directory (i.e. folder) named TestCL.*
   ```
   mkdir TestCL
   ``` 

* **To create a series of nested folders:**
     ``` 
     mkdir -p test/cats/dogs/bears 
     ```

* **To create a new file:**
    > *note: this will create a file called "hello.txt" in the folder "text".*
    ```
    touch text/hello.txt
    ``` 
<br>

## Navigating Directories 

* **To navigate FORWARD into a directory:**
    > *note: typing "cd" will "change directory" to the folder "test".*
     ``` 
     cd test 
     ``` 
     
   **If the folder contains any spaces, use quotations.**
     ``` 
     cd 'test folder' 
     ```

<br>

* **To navigate FORWARD to a subfolder:** 
     ``` 
     cd test/cats/dogs
     ```

* **To go navigate BACK to the parent (previous) directory (i.e. go back one folder):** 
     ``` 
     cd .. 
     ```
    
* **To navigate BACK to the grandparent directory (i.e. go back two folders):**
     ``` 
     cd ../.. 
     ```

<br>

## Listing Directory Contents

* **To list contents of a directory:**
     ``` 
     ls 
     ```

<br>

## Moving Files and Folders

* **To move a file to another name (i.e. rename a file)**
    > *note: this renames first.txt to second.txt*
     ``` 
     mv first.txt second.txt 
     ``` 
<br>

## Copying Files and Folders

* **To copy files and folders**
    > *note: follwing cp (copy), the first folder is what is copied, the second folder is where the first folder is copied to.*
    ```
    cp <folder-To-Copy> <folder-To-Copy-First-Folder-To>
    ```


<br>

## Deleting Files and Directories 
  
* **To remove a file**
    > *note: "rm" stands for remove, "-i" gives you a warning prompt before you delete.*
    ```
    rm -i <DOC-TO-DELETE> 
    ``` 
    
* **To remove a directory**
    > *note: "-r" stands for recursive and will remove sub folders.*
    ``` 
    rmdir -r <FOLDER-TO-DELETE> 
    ``` 
<br>
 

 # Git Version Control
  
 ## Working with Branches
   > When you create a branch, you are creating a parallel version of your repository.  Once you start working on your branch, all changes will occur inside that branch and not the master.
   
1. **CREATE and CHECKOUT a branch**
    ```
    git checkout -b <INSERT-NEW-NAME-OF-BRANCH>
    ```

2. **modify you branch now that you are in**
    > In VSCode, see bottom left corner of editor.  You should see the new name you are working on.
    > If not, click the name and you'll see file locations to change.
    > If you want to do so from Gitbash:
    ```
    git checkout <INSERT-NEW-NAME-OF-BRANCH>
    ```
     
3. **Now that modifications are made, add the modified file in branch**
    ```
    git add index.html
    ```
     
4. **Commit the file to your branch and check to see if the changes were committed**
    ```
    git add index.html
    ```

5. **Commit the updated file**
    ```
    git commit -m 'modified branch content'
    ```
    
* Note: by this time, in the bottom left hadn corner of VSCode you shoul dbe able to switch between bracnh and master.

    
<br> 

## Moving between branches (or master)
   > So suppose at this point that you have a master(i.e. "master") and a branch (i.e. "newbranch").  
   > In VSCode, when you switch between the two in the command line, that change will reflect in what you se in VSCode.  
   ```
   git checkout <location>
   ```
   > Also useful is when you want to list out your branches, to do this:
   ```
   git branch
   ```
   
<br>

## Merging Branches (and Manage Conflicts)
   > Important: If you want to merge your branch into the master, you need to be in master for this step.
   
   > If you want to merge your master into the branch, you need to be in newbranch for this step.
   
   > If you want to merge your branch into the master, you need to be in master.
   
   ```
   git merge newbranch
   ```
* *In the editor, you will see the conflicts in the code and you will need to manually modify*
<br>   


  


## Cloning a Repository
   ```
   git clone <link-of-repository-to-clone-here>
   ```
### Posting a cloned repository to GitHub
   ```
   git clone <link-of-repository-to-clone-link-here>
   ```
   ```
   git remote set-url origin <your-new-repository-to-link-here>
   ```
   ```
   git push
   ```


<br>


<br>

## Pulling Upstream Changes
   > To pull from master or branch, be in the file location and issue the command:
   ```
   git pull
   ```



<br>

# Version Control Step-by-Step

### Setting Up Your Project
   > In this phase, you are simply creating the folder and the files you wish to apply version control to.
   > The method below creates the folder and files in command line, however you can also create the files from your editor as well.
   
1. **Check to make sure you are in the right directory**
    ```
    pwd
    ```
2. **Create a new directory**
    ```
    mkdir project
    ```
3. **Move into the new directory**
    ```
    cd project
    ```
4. **Create files for your project**
    ```
    touch index.html index.css index.js
    ```
5. **Check to make sure the files are there**
    ```
    ls
    ```

<br>

### Initializing Your Project as a Git Repository
   > In this phase you are "initializing" your project.  This means that you are telling Git that you want to use version control for this folder and TRACK the files that you add.  Once you add the file, you have changes that are STAGED to be committed.    

6. **Initialize the project folder as a Git repository**
    ```
    git init
    ```
7. **Check the status of your repository**
    ```
    git status
    ```
8. **TRACK your files by adding them**
    ```
    git add index.html index.css index.js
    ```
    or use ``` . ``` to track all files in folder.
    ```
    git add .
    ```

<br>

### Committing Staged Changes

9. **Commit your staged changes SHORT WAY**
    ```
    git commit -m 'initial commit'
    ```
    
9. **Commit you staged changes LONG WAY**
    ``` 
    git commit
    :i
    initial commit
    ```  
    
    *Press escape key*
    
10. **Check status**
    ```
    git status
    ```
   
<br>

### Uploading Local Repository to GitHub
  > Assuming you have an account with GitHub already, you need to first create a new repository.  Once you have created the new repository, you copy the provided link to that repository to use in the next step.
  
12. **Add a new remote repository (named origin) that lives at the provided address**
      > if fatal error, try to remove first... git origin remove <gitaddress> 
    ```
    git remote add origin https://github.io/<name>/<foldername>.git
    ```
13. **Push the local commit history to the remote repo (origin) to a local branch called "master"**
      > *note: the -u flag setps things up so that you only need to use ```git push``` instead of the full ```git push origin master```*
    ```
    git push -u origin master
    ```
 
 <br>



