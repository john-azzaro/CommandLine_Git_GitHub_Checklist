# Command Line, Git, and GitHub Checklist

##### What is Command Line, Git, and GitHub Checklist?
The Command Line, Git, and GitHub Checklist is a handy collection of step-by-step instructions for Command Line, Git, and GitHub.



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

## Basic Navigation Using Command Line

#### Print out Git Help
     > ``` git --help ```


#### Finding your current location

**To show your current location:** 
     > ```    pwd   ```

**To return to your user account home foldder**
     >``` cd ~ ```
   
#### Creating new directories and files

* **To create a new directory:**
       > ```mkdir TestCL``` *(this will make a new directory(i.e. folder) named TestCL*

* **To create a series of nested folders:**
       > ``` mkdir -p test/cats/dogs/bears ```

* **To create a new file:**
       > ```touch text/hello.txt``` *(this will create a file called "hello.txt" in the folder "text")*

#### Navigating directories 

* **To navigate FORWARD to a directory:**  
      > ``` cd test ``` *(typing "cd" will "change directory" to the folder "test")*
   **If the folder contains any spaces, use quotations.**
      > ``` cd 'test folder' ```
   
* **To navigate FORWARD to a subfolder:** 
      > ``` cd test/cats/dogs ```

* **To go navigate BACK to the parent (previous) directory (i.e. go back one folder):** 
       > ``` cd .. ```
    
* **To navigate BACK to the grandparent directory (i.e. go back two folders):**
       > ``` cd ../.. ```

#### Finding out whats in a directory

* **To list contents of a directory:**
       > ``` ls ```

#### To move files and folders

* **To move a file to another name (i.e. rename a file)**
       > ``` mv first.txt second.txt ``` *(renames first.txt to second.txt)*
    
#### Deleting Folders and Directories

* **To remove a file**
      > ```rm -i doctodelete.txt ``` *("rm" stands for remove, "-i" gives you a warning prompt before you delete)*

* **To remove a directory**
      > ``` rmdir -r foldertodelete ``` *("-r" stands for recursive and will remove sub folders)*





