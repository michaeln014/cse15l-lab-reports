# Lab Report 1
## Step 1: Installing VSCode
Install VSCode going to this [link](https://code.visualstudio.com/) and downloading it for your software.
After downloading, run the exe file and follow the steps. 

Upon opening you'll see something like this on VSCode
![Image](Code_0406_1938_08.png)

After opening up VSCode, create a new Terminal by going to "Terminal" on top, selecting it, and clicking New Terminal. Using " Ctrl+Shift+\` " will work too.
## Step 2: Remotely Connecting
Once at the terminal, we remotely connect using the `ssh` command to log into a course account under an `ieng6.ucsd.edu` email such as `cs15lsp23ko@ieng6.ucsd.edu`. This image is how it is done and what the result should be.

![Image](0410_1419_36.png)

Some issue can arise from logging on here. One issue is if your account password was recently set, it may not register on the terminal and not allow you to login with your cs15l account. If this happens, waiting until the password is registered will solve the issue. If there are still issues, check if your username and password are put in correctly. Also don't copy and paste the password in as the terminal may not register the password if it's pasted in instead of being typed.

An alternative account can be used to log in with `ssh` if there are still issues even trying those solutions. This can be done using your UCSD account and password instead. When using your UCSD account, use `@ieng6.ucsd.edu` instead of `@ucsd.edu`. 
## Step 3: Trying Some Commands
Here we can try commands on the terminal. The main commands are listed here:
`pwd` `cd <path>` `ls <path>` `cat <path1> <path2>`
Some commands that can be tried out are listed here:

`cd ~`

`cd`

`ls -lat`

`ls -a`

`cp /home/linux/ieng6/cs15lsp23/public/hello.txt ~/`

`cat /home/linux/ieng6/cs15lsp23/public/hello.txt`

Example of some commands run:
![Image](Code_0410_1421_57.png)

To log out, use Ctrl + D hotkey or run `exit` in the terminal.

