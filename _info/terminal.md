---
title: Getting a terminal on your computer (Mac or Windows)
desc: "Getting a terminal on your computer (Mac or Windows)"
---

# Getting a terminal on your computer (you need to get this working before your first lab)

Come to my office hours if you have any trouble. All the notes that I wrote in the videos are available for you to view using the "whiteboard notes" link on the homepage.

## Using a Mac

Watch this video: <https://youtu.be/OfYG6WxlXes>

## Using Virtualbox (Windows or Mac)

Watch this video: <https://youtu.be/M5yzMPNZMCw>. I had some trouble getting shared folders working properly, but just watch until the very end and it'll all work out!

## Using Windows Subsystem for Linux

There are 2 options for working in a Windows environment.
  * "Natively" - directly in the Windows OS and filesystem 
  * On the Windows Subsystem for Linux (WSL) - a tool that basically creates a separate Linux environment alongside your Windows environment. Kind of like a more lightweight VM, with access to local storage.
    * Any files you create within the WSL are still stored in your local filesystem, and can be found by entering `\\wsl$` into the filepath bar in a File Explorer window

### Getting started with WSL

You will need to be running Windows 10 (64-bit) in order to set up the Windows Sub-system for Linux (WSL).

If you don't have the WSL activated on your computer already, follow the directions at the following link to set it up. There will be a variety of Linux distributions from which to choose. If you don't have a preference, choose Ubuntu. It is the most popular, so online documentation and discussion about the WSL usually pertains to the Ubuntu distro.
    * https://docs.microsoft.com/en-us/windows/wsl/install-win10

Once you have the WSL set up, you should see the corresponding app (Ubuntu, for example) in your Start Menu. Opening the app will launch a terminal instance in that environment. You can navigate using all the typical Unix commands.

It should come with C++, the g++ compiler, and the GBD debugger included.

#### Git on WSL

WSL should come with git, but you can check by running `git --version`. If it is not installed, then follow the instructions at this link: https://peteoshea.co.uk/setup-git-in-wsl/

If you want to work remotely via SSH, you will have to generate new SSH keys specific to the WSL environment. For instructions on how to do that, take a look at this page: https://ucsb-cs56.github.io/topics/github_ssh_keys/
   * You don't need to set up SSH keys, since you can always work remotely with repos via HTTPS, but using SSH keys just makes it easier since you will not have to re-enter your GitHub login information whenever you want to clone a repo or push/pull.

#### WSL with Visual Studio Code

Visual Studio Code is a popular general-purpose code editor. If you are currently a VS Code user (or considering becoming one), you can install an extension to be able to access/edit/track files in the WSL from VS Code. Follow the instructions [here](https://code.visualstudio.com/docs/remote/wsl) to get started. 




