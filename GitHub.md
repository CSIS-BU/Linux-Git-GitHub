# GitHub

## References

* [Introduction to GitHub](https://lab.github.com/githubtraining/introduction-to-github)
* [GitHub.com Help Documentation](https://help.github.com/en/github)

## Introduction

* GitHub is an online Git-repository manager. While I was preparing the materials for GitHub, I found that the **Introduction to GitHub** provides a good learning by doing tutorial.


## Reminder

* The tutorial provides the actions that you can take on GitHub. You should also learn how to execute the commands through the Git tool. See the Git Cheat Sheet below.

[Git Cheat Sheet](https://github.github.com/training-kit/downloads/github-git-cheat-sheet.pdf)

## Git and GitHub

### __Create a remote, **empty** folder/repository on Github.__

1. Login to your Github account.
2. At the top right of any Github page, you should see a '+' icon. Click that, then select 'New Repository'.
3. Give your repository a name--ideally the same name as your local project. If I'm building a travel application, its folder will be called 'travel-app' on my computer, and 'travel-app' will be the Github repository name as well.
4. Click 'Create Repository'. The next screen you see will be important, so don't close it.

### __Connect your local project folder to your **empty** folder/repository on Github.__

The screen you should be seeing now on Github is titled 'Quick setup — if you’ve done this kind of thing before'.

Copy the link in the input right beneath the title, it should look something like this: https://github.com/[your ID]/test-repo.git 
    
This is the web address that your local folder will use to push its contents to the remote folder on Github.

1. Go back to your project in the terminal/command line.
2. In your terminal/command line, type git remote add origin [copied web address]

    Example: git remote add origin https://github.com/[your ID]/test-repo.git

3. Push your branch to Github

        git push origin master
4. Go back to the folder/repository screen on Github that you just left, and refresh it.
   
    The title 'Quick setup — if you’ve done this kind of thing before' should disappear, and you should see your files there.

### __Cloning a repository__

[Reference (GitHub)](https://help.github.com/en/github/creating-cloning-and-archiving-repositories/cloning-a-repository)

### __Notes__

1. To date, you CANNOT create a GitHub repo through the Git command
2. [Managing remote repositories](https://help.github.com/en/github/using-git/managing-remote-repositories)

        git remote -v

    to see the remote info.
