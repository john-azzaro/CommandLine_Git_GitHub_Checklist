# Command Line, Git, and GitHub Checklist

**Table of Contents**

* [Command Line Checklist](#Command-Line-Checklist)
   * [Basic Commands](#Basic-Commands)
   * [Display Git Help](#Display-Git-Help)
   * [Establishing Location](#Establishing-Location)
   * [Creating New Directories and Files](#Creating-New-Directories-and-Files)
   * [Navigating Directories](#Navigating-Directories)
   * [Listing Directory Contents](#Listing-Directory-Contents)
   * [Moving Files and Folders](#Moving-Files-and-Folders)
   * [Copying Files and Folders](#Copying-Files-and-Folders)
   * [Deleting Files and Directories](#Deleting-Files-and-Directories)

* [Version Control](#Version-Control)

   


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

* **To navigate FORWARD to a directory:**
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
    cp folderToCopy folderToCopyFirstFolderTo
    ```


<br>

## Deleting Files and Directories 
  
* **To remove a file**
    > *note: "rm" stands for remove, "-i" gives you a warning prompt before you delete.*
    ```
    rm -i docToDelete.txt 
    ``` 
    
* **To remove a directory**
    > *note: "-r" stands for recursive and will remove sub folders.*
    ``` 
    rmdir -r folderToDelete 
    ``` 

<br>

# Version Control

## Version Control Step-by-Step

* **STEP 1: Check to make sure you are in the right directory**
```
pwd
```
    



