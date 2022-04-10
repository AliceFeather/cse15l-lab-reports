# Remote Access Tutorial
How to log onto course-specific account on **ieng6**?

---

## Step 1: Installing VScode
![Step1:](step1.png)
- Go to https://code.visualstudio.com/ website to download VScode
- Install the version that match with your computer operating system

![Step1/2](part2.png)
- When the VScode is successfully installed, the first page shown when VScode is open would like be like this

## Step 2: Remotely Connecting

- If the computer operating system is Windows, install [openSSH](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse) through the link

- Look up CSE15L course-specific account through this website:
https://sdacs.ucsd.edu/~icc/index.php


![step2](step2.png)
- Open up a terminal in VSCode and type in **ssh** followed by the account
- Then enter the password (the password will not be shown as you type)
- Then when you log in, the terminal should looks like the above
- *If you didn't connect to the server before, a message that ask "Are you sure you want to continue connecting may be shown. Press yes to continue and enter the password*

## Step 3: Trying Some Commands
- Try running some commands, like `cd`, `cd ~`, `ls -lat`, `ls -a`, `pwd`, `mkdir`, `cp`<br/><br/>
![step3](step3.png)
- For example, I try the command `cp /home/linux/ieng6/cs15lsp22/public/hello.txt ~/`, and the output of permission denied is displayed

## Step 4: Moving Files with **scp**

## Step 5: Setting an SSH Key

## Step 6: Optimizing Remote Running
