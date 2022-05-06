# Lab Report 3
By: jt

## Streamlining ssh Configuration

1) First locate the ssh folder by navigating to user and look for the folder called ".ssh".  

![SSH Folder](https://raw.githubusercontent.com/jt-ucsd/cse15l-lab-report-3/main/Streamlining%20SSH%201.jpg)

2) Create a new text file in the folder and type in the following where you replace `cs15lsp22atu` with your own username:

```
Host ieng6
   HostName ieng6.ucsd.edu
   User cs15lsp22atu
```

![SSH Config Code](https://raw.githubusercontent.com/jt-ucsd/cse15l-lab-report-3/main/Streamlining%20SSH%202.jpg)

3) Using command prompt, navigate to the folder and type in: ``ren config.txt config``.

![Rename File from TXT](https://raw.githubusercontent.com/jt-ucsd/cse15l-lab-report-3/main/Streamlining%20SSH%203.jpg)

4) Now, you can open powershell and log in with just the command ``ssh ieng6``.

![SSH ieng6 login](https://raw.githubusercontent.com/jt-ucsd/cse15l-lab-report-3/main/Streamlining%20SSH%204.jpg)

5) You can even combine it with scp commands to copy over files like so.

![SCP with ieng6](https://raw.githubusercontent.com/jt-ucsd/cse15l-lab-report-3/main/Streamlining%20SSH%205.jpg)

## Setup Github Access from ieng6

1) First, you will need to make an ssh key on your remote computer through the methods discussed in lab 1.  Then, copy the key and put it into github.  If you do it correctly, it should look like this.

![Github SSH Keys](https://raw.githubusercontent.com/jt-ucsd/cse15l-lab-report-3/main/Github%20Access%20from%20Ieng6%201.jpg)

2) Afterwards, you can check by doing ``cd .ssh`` on your remote computer to move the directory to the folder that should hold both the private and public key.

![SSH Private and Public Directory](https://raw.githubusercontent.com/jt-ucsd/cse15l-lab-report-3/main/Github%20Access%20from%20Ieng6%202.jpg)

3) If you have done everything correct, you should be able to run ``git push origin main`` from your remote computer to push updates to github.

![Git Push Origin Main Working](https://raw.githubusercontent.com/jt-ucsd/cse15l-lab-report-3/main/Github%20Access%20from%20Ieng6%203.jpg)

4) The changes should be reflected in Github like so.  Here is my [link](https://github.com/jt-ucsd/markdown-parser/commit/aade8e55119b8781c2026ad4a1c5bcd1bef2dec6) to my repository updated through ieng6 remotely.

![Github Commit Remote](https://github.com/jt-ucsd/cse15l-lab-report-3/blob/main/Github%20Access%20from%20Ieng6%204.jpg)

## Copy whole directories with scp -r

1) You can copy your whole directory to the ieng6 account by running the following ``scp -r MarkdownParse cs15lsp22atu@ieng6.ucsd.edu``.

![Copying Whole Directory](https://raw.githubusercontent.com/jt-ucsd/cse15l-lab-report-3/main/Copy%20Whole%20Directory%201.jpg)

2) Once you copied it over, you can even compile and run tests on the ieng6 account.

![Running Tests Remotely](https://raw.githubusercontent.com/jt-ucsd/cse15l-lab-report-3/main/Copy%20Whole%20Directory%202.jpg)

3) You can combine ``scp -r`` with the streamlining ssh config section of this lab report to make it even faster to copy over and login.

![Combining with ssh streamline](https://raw.githubusercontent.com/jt-ucsd/cse15l-lab-report-3/main/Copy%20Whole%20Directory%203.jpg)