# Linux commands, Git, and GitHub

## Git

## Reference

* [Git](https://git-scm.com/)
* [Official Git tutorial](https://git-scm.com/docs/gittutorial)
* [Learn Git branching](https://learngitbranching.js.org/)
* [Git Immersion](http://gitimmersion.com/)
* [Everyday Git](https://git-scm.com/docs/giteveryday)
* [(free e-book) Pro Git](https://git-scm.com/book/en/v2)

## Introduction

* Note: In this tutorial, I'll NOT use the Git client with the GUI but just the command under the command prompt/terminal. You are free to use any Git client with GUI if you want. I don't have any preference for the Git client.

* What is Git?

    A [version control](https://git-scm.com/book/en/v2/Getting-Started-About-Version-Control) tool that is commonly used in many fields. You may use Git to keep track of your projcet/assignment whenever you make changes. With Git, you may work on the project on your own, or contribute to a big project with hundreds or thousands of developers.

* A bit background of Git

    You can use Git to take a [snapshot](https://git-scm.com/book/en/v2/Getting-Started-What-is-Git%3F) of the project you're working on, which only stores the **differences** (new additions/deletions or changes) with respect to the prior version.

## Instructions

1. Download and install Git on your machine
2. Open a command prompt (Windows) or terminal (Linux/Mac OS)

    For Windows, you can run the **cmd** command for command prompt or open **Windows PowerShell**

3. Switch to the **home directory** or the **Desktop** of the current user
    For example, on Windows (assuming that when you run **cmd** or **PowerShell**, the default directory is **C:\Users\\[your login ID]**), you can run

        cd Desktop

    to switch to the Desktop folder (**C:\Users\\[your login ID]\Desktop**) of the current user.

Note: Here, [your login ID] is the account you use to log into the Windows system. If you are under Linux/Mac OS, the directory would look like

        /home/[your login ID]

4. Now, create a folder *Git** on your Desktop

        mkdir Git
5. Again, change the current working directory to the **Git** folder on your Desktop (**C:\Users\\[your login ID]\Desktop\Git**)

        cd Git

Note: if you are under different current working directory, you may also run the following to switch to the respective directory

        cd C:\Users\[your login ID]\Desktop\Git
6. To user the current folder as a Git repository, do

        git init
Note: You may be prompt to run

        git config --global user.email "your e-mail address"
        git config --global user.name "your name"

You only will need to go this once as what you enter above will be stored as the global variable and will be adopted everytime you make changes to the repository. You can see the global variables through

        git config --global -l

Note: I would recommend running the following command under your Linux/Mac OS environment if you are NOT familiar with the editor **vi**

        git config --global core.editor nano

If you are using Windows, do the following instead

        git config --global core.editor notepad

7. Once you initiated the current folder as a Git repository (**repo** in short for **repository**), you can now add/change/modify the content in the folder. 
   
    For example, use any editor you like to create a file **test.txt** and save it in the **Git** folder.

    Add **Hello, World!** as the content to the file.

8. Check the current state of the repo.

        git status

    It says something similar to 

        On branch master
        No commits yet
        Untracked files:
            (use "git add <file>..." to include in what will be committed)
            test.txt

        nothing added to commit but untracked files present (use "git add" to track)

Note: Git will NOT track the changes automatically, and it would not know the newly added/deleted/modified files unless you track it by **git add**

9. Now, we track the changes to the file **test.txt** with

        git add test.txt

10. Run **git status** again and see the changes.
11. Now, we are tracking the changes on the file **test.txt**. However, we have not taken the snapshot yet, so the file is currently under a *pending* state -- that means the changes on the file is not OFFICIALLY recorded. To officially record the changes, you'll need to **commit** the changes by 

        git commit

    The command above will bring you to an editor of your choice (which we changed in step. 6 above). Here, at the very beginnnig/first line of the file, you enter the comments corresponding to the changes you made to the repository, then save the file. 
    
    For example, I'll put **Add a file to demo the Git commands** in the first line.

12. Once done, you may check the status again

        git status


13. Use another command to see the history of the snapshots you took

        git log

14. Once the snapshot is taken, you are safe to delete the file **test.txt** as you'll be able to recover it through the repo. First delete the **test.txt** file, then check the status of the repo again.

        git status

    It says

        Changes not staged for commit:
            (use "git add/rm <file>..." to update what will be committed)
            (use "git restore <file>..." to discard changes in working directory)
                    deleted:    test.txt

15. You may recover the deleted file with

        git restore test.txt

    And, Kaboom! The file is back.

16. If you make changes to many files and folders, and would like to track all changes under the current directory, you may run

        git add .

17. Don't forget, tracking a file is not equivalent to taking a snapshot. The files being tracked may get changed before the snapshot is taken. So, before you **commit**, make sure you **track** the version of the files you want to have in the snapshot.

## Conclusion

Please be aware that I cannot cover all the important features provided by Git. This tutorial is just to get you started. Ther are many other things, such as **Branching, Merging, Stashing, Cleaning, Selection, Staging** and many more that you should learn. Please refer to the **Pro Git** book provided above to learn Git. 

## Important Commands

[Git Cheat Sheet](https://github.github.com/training-kit/downloads/github-git-cheat-sheet.pdf)

        git init
        git add
        git commit
        git branch
        git checkout
        git push
        git pull
        git clone
        git log
        git status
        git diff
        git reset
        git remote

[Git cheat sheet (more commands!)](https://www.atlassian.com/git/tutorials/atlassian-git-cheatsheet)