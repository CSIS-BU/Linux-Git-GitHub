# Linux commands, Git, and GitHub

## Linux

### References

* [Linux Tutorial](https://ryanstutorials.net/linuxtutorial/)
* [PuTTY](https://www.chiark.greenend.org.uk/~sgtatham/putty/)

* How to log into the departmental Linux service under Windows?

1. Download and install PuTTY
2. Open PuTTY, and enter **playground.bradley.edu** in the "Host Name (or IP address)"
3. You may safe this session for future use by entering **playground** in the "Saved Sessions", then click "Save" button on the right
4. Double-click on the **playground** session you just saved, or select the **playground** session and click "Open" button to open connection to **playground.bradley.edu**

Note: if your system is Linux or Mac OS, you may just open a terminal and type in

        ssh [Your ID]@playground.bradley.edu

Here, [Your ID] is the your ID for Bradley's login ID.

* What can you do after you log into playground.bradley.edu through an ssh client (like putty)?
1. The first time you use PuTTY to connect to a machine, it will prompt you to trust the host key. You may accept it.

    [Ref: Verifying the host key (SSH only)](https://tartarus.org/~simon/putty-snapshots/htmldoc/Chapter2.html#gs)

2. Once successfully log into the system with your Bradley ID and password, you will see a command prompt ($, or %, or some other symbols that may be customized). You can now enter commands. A few commands that you should learn to get yourself started would be

        ls, pwd, cd, mkdir, rmdir, touch, mv, cp, rm, chmod, nano, ps, head, tail, grep, man

**man**: online reference manual for commands/functions/configurations/etc
* Usage:

        man ls

**ls**: list all the files and folders under the current working directory
* you may add options to show more information.

        ls -l

which shows something like

        drwxr-xr-x 2 djlin ADUsers     4096 Oct  3  2014 CIS210/
        drwxr-xr-x 4 djlin users       4096 Oct 16  2018 cis445/
        -rw-r--r-- 1 djlin ADUsers     1366 Apr 16  2015 client.c

Here, the 

        drwxr-xr-x

represents the permissions of the specific file or directory.

1. d: directory. If it's a file, the first char will be -
2. r: read permission
3. w: write permission (binary)
4. x: executable permission

See **chmod** for detail info.

**chmod**: change file mode bits.
* Usage: please execute the following command for more detail info.

        man chmod 

In short, if you want to change a file 'pqr''s permission to read/write for the owner, read for the people in the same group of the file, and no access for anyone else, do

        chmod 640 pqr

**pwd**: print current working directory
* Note: under the Linux terminal, you are always working under a directory similar to the Windows' **C:\Users\XYZ** folder. You may need to switch back and forth among different directories while working.

**mkdir**: make directories
* Usage: (created three folders *folder1, folder2, folder3*)

        mkdir folder1 folder2 folder3

**rmdir**: remove empty directories => you cannot remove non-empty directories with this command
* Usage:

        rmdir folder1

**touch**: change file timestamps (Update the access and modification times of each FILE to the current time.)
* Usage:

        touch xyz
* Note: If the file 'xyz' does not exist, **touch** will create an empty file called 'xyz'

**cp**: copy files and directories
* Usage: copy a file 'xyz' to another file 'abc'

        cp xyz abc
* Note: to copy a directory, you'll need to provide additional options. Run the following command for more detail.

        man cp

**rm**: remove files or directories (**BE CAREFUL!!** **BE CAREFUL!!** **BE CAREFUL!!**)
This is a powerful command as you may delete everything you have accessed to. When you run this command in the terminal to remove a file, it will NOT go to recycle bin but **permanently deleted**.
* Usage: delete a file 'abc' under the current working directory

        rm abc

**nano**: an editor, which you use to edit files
* Usage: to open a file XYZ, run

        nano XYZ

**ps**:  displays information about a selection of the active processes. You man use this command to check the status of your current running programs.
* Usage:

        ps

**grep**: searches for some pattern in each file.
* Usage: search in the file ABC for a pattern **hello**

        grep hello ABC
* Note: see the manual for more detail. You can also use **regular expression**



