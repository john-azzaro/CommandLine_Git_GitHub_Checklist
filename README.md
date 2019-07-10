# Git Bash, Git, and GitHub Checklist

**Table of Contents**

* [Git Bash Checklist](#Git-Bash-Checklist)
   * [Basic Commands](#Basic-Commands)
   * [Display Git Help](#Display-Git-Help)
   * [Establishing Location](#Establishing-Location)
   * [Creating New Directories and Files](#Creating-New-Directories-and-Files)
   * [Navigating Directories](#Navigating-Directories)
   * [Listing Directory Contents](#Listing-Directory-Contents)
   * [Renaming Files and Folders](#Renaming-Files-and-Folders)
   * [Copying Files and Folders](#Copying-Files-and-Folders)
   * [Deleting Files and Directories](#Deleting-Files-and-Directories)
   * [Deleting File from Local AND GitHub](#Delete-File-from-Local-AND-GitHub)
   * [Deleting File from GitHub ONLY](#Delete-File-from-GitHub-ONLY)

* [Version Control Step-by-Step](#Version-Control-Step-by-Step)
   * [Setting Up Your Project](#Setting-Up-Your-Project)
   * [Initializing Your Project as a Git Repository](#Initializing-Your-Project-as-a-Git-Repository)
   * [Committing Staged Changes](#Committing-Staged-Changes)
   * [Uploading Local Repository to GitHub](#Uploading-Local-Repository-to-GitHub)

* [Git Version Control](#Git-Version-Control)
   * [Working with Branches](#Working-with-Branches)
   * [Moving Between Branches](#Moving-Between-Branches)
   * [Merging Branches and Managing Conflicts](#Merging-Branches-and-Managing-Conflicts)
   * [Cloning a Repository (and pushing to GitHub)](#Cloning-a-Repository)
   * [Pulling Upstream Changes](#Pulling-Upstream-Changes)



   


# Git Bash Checklist

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

* ```   code .       ``` **Open file in text editor** *(used to quickly open file location in text editor).*

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

## Renaming Files and Folders

* **To rename a file to another name**
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
    > *note: "-i" gives you a warning prompt before you delete.  ALWAYS USE "rm -y" FOR ADDTIONAL SAFETY!*
    ```
    rm -i <DOC-TO-DELETE> 
    ``` 
    
* **To remove an EMPTY directory**
    > *note: "-r" stands for recursive and will remove sub folders.*
    ``` 
    rmdir -r <FOLDER-TO-DELETE> 
    ``` 
    
* **To remove an POPULATED directory**
    > *note: "-rf" stands for recursive and will remove sub folders and will remove files and folder without confirmation.*
    ``` 
    rm -rf <FOLDER-TO-DELETE-WITH-ALL-CONTENTS> 
    ``` 
<br>
 
## Delete File from Local AND GitHub
    > *note: Remember to use '' to encapsulate document.
    ```
    git rm '<DOC-TO-DELETE>' 
    git add .
    git commit -m 'Removed: XYZ'
    git push origin master
    ```
<br>

## Delete File from GitHub ONLY
    > *note: Remember to use '' to encapsulate document.
    ```
    git rm --cached '<DOC-TO-DELETE>' 
    git add .
    git commit -m 'Removed: XYZ'
    git push origin master
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
   > Note: Remember to track your files first before you commit using "git add ."
   
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


 # Git Version Control
  
 ## Working with Branches
   > When you create a branch, you are creating a parallel version of your repository.  Once you start working on your branch, all changes will occur inside that branch and not the master.
   
1. **See all branches that have been created**
    ```
    git branch 
    ```
    
2. **To CHECKOUT (i.e. move) to a desired branch**
    ```
    git checkout <INSERT-NEW-NAME-OF-BRANCH-HERE>
    ```   
   
3. **To CREATE and CHECKOUT a branch**
    ```
    git checkout -b <INSERT-NEW-NAME-OF-BRANCH-HERE>
    ```
         
4. **New commits will be within this branch alone**
    ```
    git add index.html
    git commit -m 'modified branch content'
    ```
    
5. **To PUSH branch to GitHub**
    ```
    git push origin <INSERT-NAME-OF-BRANCH>
    ```
    
6. **To DELETE branch on local machine**
    ```
    git branch -d <NEW-NAME-OF-BRANCH-HERE>
    ```
   
7. **To DELETE branch on GitHub**
    ```
    git push origin :<NEW-NAME-OF-BRANCH-HERE>
    ```
  
VSCode Note: In the bottom left hand corner of VSCode you should be able to switch between branches and master.

    
    
    
    
<br> 

## Moving Between Branches 
   > In VSCode, see bottom left corner of editor to see which branch (or master) you are currently in.
   > If you are NOT in the desired location, click the location name and you'll see file locations to change to.
   > Also note that in VSCode, when you switch between the two in the command line, that change will reflect in what you se in VSCode.  
   > However, if you want to do so from Gitbash:
   
1. **Show all existing branches**
    ```
    git branch 
    ```
   or to see path with branch listing:
    ```
    git branch -a
    ```
 
2. **Move into desired branch with "checkout"**
    ```
    git checkout <NAME-OF-BRANCH-HERE>
    ```
   
<br>





## Merging Branches and Managing Conflicts
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


