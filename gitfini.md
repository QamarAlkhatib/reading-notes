### based on what I have learned from today class for Git and GitHub

#### 1. The difference between GUI and CLI

A **GUI** (GUI) and a command line interface **(CLI)** are two ways of interacting between a user and an electronic device. A **GUI** is a graphical representation in which users interact with software or devices via clickable icons. A **CLI** console is a text-based rendering where users type commands into a terminal to operate or navigate a software or device
A **graphical user interface** uses graphics to enable users to communicate with an operating system or application. **It provides windows, menus, buttons, scrollbars, icons, wizards and other mouse icons for users to interact with the program.**

#### 2. What is Git
Git is a version control system for managing changes to your source code and **GitHub** is a cloud hosting platform for managing Git repository changes. Git is a distributed **version control system** (VCS) that allows developers to manage and, if needed, branch out and merge changes, giving developers full control over the local code base. **Git allows you to store code as a distributed, open-source version control system (VCS), track revision history, merge changes and access previous versions of code as needed.**

### **Example Commands**
* git add .
* git commit -m "Text"
* git push origin main 
* git pull



## Git Findings

# To get Start 
So to **get start with git** we have to download it and it can installed in three ways:

1. **as a package**

2. **via another installer**

3. **by downloading it and compile the source code**


> Note: 

To see how to download it on your machine 

[check this link out](https://blog.udemy.com/git-tutorial-a-comprehensive-guide/#7_2) 

## Graphical clints 
The Graphical User Interface (GUI) tools in Git are built-in. Users can, however, utilize third-party solutions designed for specific systems.

## Default Text Editor
If you don't specify a default text editor, Git will use the system's default text editor, which is most likely Vim. Type the following into your Terminal or Command Line to set up an alternative text editor, such as Emacs:

``` $ git config --global core.editor emacs ```

## Check Settings
To check settings, use this command
 
 ```$ git config --list command. ```

## Getting Help

There are three ways to view the documentation for further information on a certain command:
```
git help command
git command --help
man git-command
```
# Setting up a Git Repository

## Importing
Using the Terminal or Command Line, follow these steps to import an existing project or directory into Git:

**1. Switch to the target project’s directory** 

``` cd test (cd = change directory) ```

**2.  Use the git init command**

``` git inti ```

**3. To begin monitoring these repository files, type the following as an initial commit:**
```
git add *.c

git add LICENSE

git commit -m “any message here”
```


## cloning 
You can also use the clone command with a repository's URL to make a copy of an existing Git repository from a specific server:


``` git clone https://github.com/test ```

You've duplicated all versions of all files in a project by cloning the file. This command creates a directory named "test" that has an initialized.git directory that contains copies of all versions of all files for the given project. A copy of the most recent version of the project is also checked out — or retrieved for editing — using the command.

**Use the following command format to clone a repository into a directory with a different name:**

``` git clone https://github.com/test mydirectory ```

# Workflow 

## Local Repository Structure

There are three parts to the local Git repository:

**1. Working Directory: The actual files reside here.**

**2. Index: The area used for staging**

**3. Head: Points to the most recent commit**

## Saving Changes
A tracked or untracked state exists for all files in a checked out (or working) copy of a project file.

1. **Tracked**
They were part of the most recent file snapshot and can be updated, unmodified, or staged.
2. **Untracked**
files were not present in the last snapshot and are no longer in the staging area. 

## The Life Cycle of File Status
**1.  After you edit a file, Git flags it as modified because of changes made after the previous commit.**

**2. You stage the modified file.**

**3.Then, you commit staged changes.** 

## Check File Status

Use the git status command to see what's up with your files:

``` git status ```

## Tracking and Staging a New File

 1. Single File
 we can track one file by :

``` git add filename``` 

 2. All files
 we can track all files by:

 ``` git add ```

 3. To see the information that changed using this command:

 ```git status``` 


## To Committing a File
 After staging one or more files, submit the changes and include the following information in the commit message:

``` git commit -m “made change x,y,z” ```

##  To Committing All Changes
 by this command:

  ``` git commit -a ```

## To Pushing Changes
You'd next submit the modifications to a remote repository. In the next part, we'll go through remote repositories in further detail. For now, let's take a look at how to push updates to remotes in general.

 **Example** 

``` git push origin master```

## To Stashing Changes
Git stash is a fantastic alternative when you're not ready to commit changes but don't want to lose them either. This command conceals and temporarily eliminates modifications, leaving you with a clean working directory. Simply use the git stash apply command to retrieve the concealed changes when you're ready to resume working on them.

## Remote Repositories
You must interact with remote repositories, which are versions of a project that are stored online or on a network, in order to collaborate on Git projects. You can work with numerous repositories and have read/write or read-only access to them. Remote repositories may be used to push and get data from by teams.
## Cloned Repositories

As previously stated, Git will automatically assign the name "origin" to the server from which you cloned and the name "master" to your local branch for cloned repositories.