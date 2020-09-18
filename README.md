# Contribution-Guidelines
This document serves as a basic guideline on how to contribute to ADA's open-source projects. If you are a pure beginner, don't worry, this document will help you get started :)

# Table of contents
* [Required settings](#Required-settings)
    * [Setup Github account](#Setup-Github-account)
    * [Setup a command-line terminal](#Setup-a-command-line-terminal)
    * [Install git](#Install-git)
    * [git basic usages](#git-basic-usages)
    * [git pull requests](#git-pull-requests)
* [Optional settings](#Optional-settings)
    * [Install Vscode](#Install-Vscode)
    * [Install Vscode](#Install-Vscode)
    * [Install node.js & npm](#Install-node.js-&-npm)


# Required settings

## Setup Github account
Go to https://github.com and make yourself an account. Github is what we usually use for our online repositories. Make yourself a profile picture and ask one of our administrators to add you to our UTADA organization. 

## Setup a command-line terminal
### Linux & Mac
Open the `Terminal` app. Done.
### Windows (**WSL**)
If you use Windows, I assume you use Windows 10. Then you may follow this instruction: https://www.windowscentral.com/install-windows-subsystem-linux-windows-10   
This will install Windows Subsystem for Linux (**WSL**) for you. It is very useful in software development on Windows.   
Follow the steps until you reach the `Uninstalling Linux distros using Settings` section (plz don't uninstall). Now you should be able to use Ubuntu (A distribution of Linux) on Windows 10. 

*Note that your windows files are under /mnt/. You can use `cd /mnt/c` to access your files in Disk C:*

*Note: I strongly recommend to use a terminal emulator for your Ubuntu if you are on Windows. Examples: [Terminus](https://eugeny.github.io/terminus/), [Hyper](https://hyper.is/), [ConEmu](https://conemu.github.io/)*

## Install git
### Linux
git is built-in in any Linux distributions.
Type `git --help` in terminal to double-check.
### Mac
There are several ways to install git on macOS
1. If you have already installed Xcode then the git will automatically be installed to the system
2. Download the installer from [Git Installer](https://sourceforge.net/projects/git-osx-installer/files/) and follow prompt

You can verify the installation by typing `git --version` on terminal
### Windows
If you followed the terminal setup above, then you should have git built-in in your WSL

## git basic usages

## git pull requests
Branching is a powerful feature supported by git.  The workflow of our project will heavily rely on the branch.
Two branches will be created by the lead before the project start. That are **master** & **dev**.
+ master - This is the branch designed to store code for final release
+ dev - This is the branch designed to store code with the latest progress  

The following workflow will be applied to all of the future ADA's projects.
1. Clone the repository to your local machine(i.e your laptop)
2. Create a new branch by typing `git branch <branch name>`
3. Switch to your branch `git checkout -b <branch name>`
4. **When you finish your work you need to push the work to your branch instead of pushing to the master or dev**
This is done by typing `git push origin <branch name>`
5. You can go to the repository page to check your work after you pushed your work.  Under the branch of the page, you can see various branches, you need to go to the branch created by you.
6. When you are confident to submit your work for review you need to create a pull request so that the lead or person doing the review can decide which part of your code will be merged.  When you create a pull request
pick the **dev** as the base, choose **your branch** as the compare.  At this stage, you can safely ignore any warning for conflicted code.  The person who reviews your code will decide how to resolve it.
7. Lastly, if the reviewer accepted your pull request or leave a comment to your pull request you will receive an email about it.  
# Optional settings

## Install Vscode
https://code.visualstudio.com  
Vscode is one of the easiest and multi-purpose IDEs/text editors, for web front-end, JavaScript, Python, C/C++ and more. If you don't know how to start, you can start from it. 

## Install WebStorm
https://www.jetbrains.com/webstorm/download

For developers who prefer ide in JetBrains-style, WebStorm is also a great and smart IDE for web development.
## Install node.js & npm
### Linux & WSL
Go to https://nodejs.org/en/download, right-click on the `64bit` button next to `Linux Binaries (x64)`, Then select `copy link address`.  
In your terminal, find a place where you would download nodejs, run 

    wget <The link you just copied>

for example, 

    wget https://nodejs.org/dist/v12.18.4/node-v12.18.4-linux-x64.tar.xz

**Note: ctrl-c and ctrl-v won't work in most terminals, use right-click or ctrl-shift-v.**  
After download, type `ls` to double-check you have node's package downloaded.  
The next step is to unzip the package: 

    tar -xvf <Name of the tar.xz file you downloaded>

Type `ls`, you should be able to see the unzipped directory of node.  
Type 

    cd <the directory name of node>/bin

After you are inside the bin folder, execute this command

    echo PATH=\$PATH:$(pwd) >> ~/.bashrc

Then restart your terminal. You should be able to use `node` and `npm` command now. 
### Mac
