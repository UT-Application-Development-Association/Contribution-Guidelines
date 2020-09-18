# Contribution-Guidelines
This document serves as a basic guideline on how to contribute to ADA's open-source projects. If you are a pure beginner, don't worry, this document will help you get started :)

# Table of contents
* [Required settings](#Required-settings)
    * [Setup Github account](##Setup-Github-account)
    * [Setup a command-line terminal](##Setup-a-command-line-terminal)
    * [Install git](##Install-git)
    * [git basic usages](##git-basic-usages)
    * [git pull requests](##git-pull-requests)
* [Optional settings](#Optional-settings)
    * [Install Vscode](##Install-Vscode)
    * [Install Vscode](##Install-Vscode)
    * [Install node.js & npm](##Install-node.js-&-npm)


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
(TO BE FILLED BY DINO)
### Windows
If you followed the terminal setup above, then you should have git built-in in your WSL

## git basic usages

## git pull requests

# Optional settings

## Install Vscode
https://code.visualstudio.com  
Vscode is one of the easiest and multi-purpose IDEs/text editors, for web front-end, JavaScript, Python, C/C++ and more. If you don't know how to start, you can start from it. 

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
