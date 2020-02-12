# Sync the Local Git Repo. and the Remote (GitHub) Repo.

There are different scenarios when you work on your local and remote/GitHub repo.

* Assuming that you have a GitHub repo is https://github.com/djlin/hello.git
* And your project’s folder is called **PP1**

1. __If the repo is empty (no files at all), and you already completed the program without Git history (no previous commit log)__

Then, you will go to **PP1** and do the following

        git init
        git add .
        git commit
        git remote add origin https://github.com/djlin/hello.git
        git push

2. __If the repo is empty (no files at all), and you already completed the program with existing Git history__
Then, you will go to **PP1** and do the following

        git remote -v

    => if the above command has not output (no result), do

        git remote add origin https://github.com/djlin/hello.git
        git push

3. __If the repo is **NOT** empty, and you just start working on the project (has no files on the local machine)__

    Then, INSTEAD of going into the **PP1** folder, you do the following

        git clone https://github.com/djlin/hello.git

    => after executing this command, a folder hello is created on your local machine. Change directory to the “hello” folder and start developing.
    As usual, every time you work on your Git repo, always do the following when you make progress & finish.

        git add .
        git commit
        git push

4. __If the repo is NOT empty, and you made some progress (or have finished the project) with existing Git history/commits__
Since the repo on GitHub and your local repository have NO relationship, Git/GitHub would NOT allow you to push your local history to the remote.
In this case, you need to force Git to ignore the unrelated history and combine them together.

    a. First, commit your changes locally.

        git add .
        git commit

    b. Build the connection to the remote repo on GitHub

        git remote add origin https://github.com/djlin/hello.git
        git push --set-upstream origin master
        git pull --allow-unrelated-histories
        (or git pull origin master --allow-unrelated-histories)

