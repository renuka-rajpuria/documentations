## References
[Linux Beginners Guide]([https://ubuntu.com/tutorials/command-line-for-beginners](https://ubuntu.com/tutorials/command-line-for-beginners))

## Introduction
Wrapping the user’s commands this **shell** program.

The original Unix shell program was just called sh, but it has been extended and superceded over the years, so on a modern Linux system you’re most likely to be using a shell called **bash**. 

Users could even write simple code (called **shell scripts**) which could be used to automate long series of shell commands in order to make complex tasks easier.  

## Shortcuts
| Shortcut  | Use case |
| ------------- | ------------- |
| Ctrl-Alt-T  | Open the terminal  |
| Ctrl-C  |  (control character intr) sends SIGINT which will interrupt the application. |
| Ctrl-Z  | (control character susp) sends SIGTSTP to a foreground application, effectively putting it in the background, suspended. |
| Ctrl-Shft-C  | Copying in the terminal |
| Ctrl-Shft-V  | Pasting in the terminal |

## All Commands
| Command | Function | Comments |
| ------------- | ------------- | ------------- |
| pwd | print working directory | all file operations will take place here |
| cd | change directory | [see variations]() |
| ls | list | lists all files |
| mv | move | can also be used to rename files |
| la | list | lists even hidden files |
| rmdir | remove | only for empty directories |
| rm -r | remove | recursively remove all files from directory |


## Basics
1. /home/YOUR_USERNAME - computer’s way of prompting you that it is ready for commands therefore it is a prompt.
2. Linux is case sensitive - sometimes the command will not run and other times it can run to give undesired output.
3. Command Line - shell running in a terminal.

## File System and the Root directory
1. Directory separator is a forward slash (”/”), unlike Windows (backward slash).
2. Root has multiple meanings in the Linux world, so context is important.
3. "/" directory which is the root directory, is the base of the unified Linux file system. From there everything else branches out. (cd / -> root). 
4. Unified file system -  each drive is not split up differently.
5. Individual drives can be attached (“mounted”) to whatever location in the file system makes most sense.
6. From home to “etc” directory (which is directly inside the root of the file system) `cd ../../etc`
7. Relative v/s absolute paths - 

| Command  | Function | Comments |
| ------------- | ------------- | ------------- |
| pwd  | print working directory  | all file operations will take place here |
| cd  | change directory  | cd / or simple cd will take to root directory |
| cd <DIR_NAME> | change directory to given one | immediate sub-directory of "/" is home |
| cd .. | to go to parent directory | remember the space |
| cd ../.. | moving through multiple levels of parent directories | starting from the working directory, move to the parent / from that new location move to the parent again |
| cd ../../etc | moving from destination to required file | go straight from our home directory to the “etc” directory (which is directly inside the root of the file system) |

## For absolute beginners

### 1. Remember to do the following everytime you login to your system: [(Reference)](https://www.cyberciti.biz/faq/how-do-i-update-ubuntu-linux-softwares/)

```
sudo apt update
sudo apt-get upgrade (There are different variations of this)
```

### 2. To check version of ubuntu go for neofetch, if not installed type:

```
sudo apt install neofetch
```

### 3. To check version for Python:

```
python --version or python3 --version
python -V or python3 -V
```
(Check the capital V, if you write small V it will go in the interpreter)

### 4. To install gcc:

```
sudo apt install gcc
sudo apt install g++

```

### 5. If you have python3 and do not want to write it repeatedly:

```
sudo apt install python-is-python3
```

### 6. To install VSCode (with snapd pre installed)

```
sudo snap install --classic code
```

otherwise might need to do:
```
sudo apt update
sudo apt install snapd
```

### 7. To open VSCode
```
code .
```

### 8. To install Anaconda:

- To install Conda on Linux, you can follow these steps:

- Visit the official Miniconda website at https://docs.conda.io/en/latest/miniconda.html to download the installer script appropriate for your Linux distribution. You will find different installer scripts for different versions of Linux (e.g., 64-bit or 32-bit).

- Once you have downloaded the installer script, open a terminal and navigate to the directory where the script is located.

- Make the installer script executable by running the following command: ```chmod +x Miniconda*.sh```

- Run the installer script with the following command: ```./Miniconda*.sh```

- The installer will guide you through the installation process. You will be prompted to review and accept the license agreement, choose the installation location, and optionally add Conda to your system's PATH variable.

- After the installation is complete, close and reopen your terminal to activate the changes to the PATH variable.

- You can verify that Conda is installed correctly by running the following command:
```conda --version```

- This should display the version of Conda installed on your system. Remember that Conda is a separate package management system, so you may need to create and activate Conda environments to manage packages and dependencies for different projects. You can refer to the Conda documentation for more details on how to work with Conda environments.

### 8. To use Jupyter Notebooks:
a) Without virtual environment:
- Install Jupyter using Conda:```conda install jupyter```
- This command will install Jupyter and its dependencies into your Conda environment.
- Once the installation is complete, you can launch Jupyter Notebook by running:```jupyter notebook```
- This will start the Jupyter Notebook server, and you can access it through your web browser.

b) With virtual environment:
- Create a new Conda environment (optional but recommended): ```conda create --name myenv```
- Replace "myenv" with the desired name for your environment.
- Activate the Conda environment: ```conda activate myenv```
- Replace "myenv" with the name of your environment.
- Install Jupyter using Conda:```conda install jupyter```
- This command will install Jupyter and its dependencies into your Conda environment.
- Once the installation is complete, you can launch Jupyter Notebook by running:```jupyter notebook```
- This will start the Jupyter Notebook server, and you can access it through your web browser.
- Please note that you can also install JupyterLab, an alternative web-based interface to Jupyter Notebook, using Conda with the following command:```conda install jupyterlab```
- JupyterLab provides a more feature-rich and flexible environment for interactive computing and data science workflows.
- Remember to activate your Conda environment before installing or running Jupyter to ensure that it is installed within the correct environment.

Extra: Pros and Cons of Virtual Environments:
Pros:

> - Isolation
> - Reproducibility
> - Easy package management
> - Cross-platform compatibility
> - Environment sharing

Cons:

> - Disk space
> - Installation time
> - Learning curve
> - Overhead


### 8. To setup Git and Github:
Instructions are available on git.md



## Useful Addons/Applications

1. Tab completions
    For example, it’s pretty common to have a Documents folder and a Downloads folder in the home directory. If you’ve typed ```cd D``` and then press Tab, the command line will let you know that it’s not sure which one you want by showing you the different options that match what you’ve typed so far: ```bash $ cd D Documents/ Downloads/ $ cd D``` 
    
    But once you’ve typed in a little bit more, it will complete the name for you, making it possible to write out the full file path above by typing as little as ```cd Doc[tab]O[tab]f[tab]j[tab]cal[tab]```


2. xtrlock
   > - Locks X display until the password is supplied, leaving the windows visibile. This is great if you want to lock your screen, but still keep windows visible.
   > - Install via ```sudo apt-get install xtrlock```
   > - Kindly note that this will only work well on systems containing the *[X display server](https://ubuntu.com/tutorials/command-line-for-beginners)*. Hence it's most likely to not work in modern versions of Ubuntu
   
3. xwinwrap
   > - A lightweight application that allows you to set a video/gif as a desktop wallpaper. For more details on implementation visit [ujjwal96/xwinwrap](https://github.com/ujjwal96/xwinwrap) and this Reddit [post](https://www.reddit.com/r/archlinux/comments/8jnnm3/how_do_i_set_a_gif_as_my_background_with_xwinwrap/)
   > - This application is limited to devices containing the X display server.

4. net-tools
    > - They help in configuring the network details. 
    > - Install it using: ```sudo apt install net-tools ```
    > - Some common network commands are:
      ```nmtui, ifconfig```

5. Installing whatsapp for linus:`sudo snap install whatsapp-for-linux`
6. Installing obsidian for linus: [Follow this](https://help.obsidian.md/Getting+started/Download+and+install+Obsidian)
7. Getting rid of the entire directory location: ```PS1='\u:\W\$ '``` [For further reading](https://askubuntu.com/questions/145618/how-can-i-shorten-my-command-line-bash-prompt)


