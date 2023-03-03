## References
[Linux Beginners Guide](https://ubuntu.com/tutorials/command-line-for-beginners)

## Introduction
Wrapping the user’s commands this **shell** program.

The original Unix shell program was just called sh, but it has been extended and superceded over the years, so on a modern Linux system you’re most likely to be using a shell called **bash**. 

Users could even write simple code (called **shell scripts**) which could be used to automate long series of shell commands in order to make complex tasks easier.  

## Shortcuts
| Shortcut  | Use case |
| ------------- | ------------- |
| Ctrl-Alt-T  | Open the terminal  |

## All Commands
| Command  | Function | Comments |
| ------------- | ------------- | ------------- |
| pwd  | print working directory  | all file operations will take place here |
| cd  | change directory  | [see variations]() |

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
6. From home to “etc” directory (which is directly inside the root of the file system) _cd ../../etc_

| Command  | Function | Comments |
| ------------- | ------------- | ------------- |
| pwd  | print working directory  | all file operations will take place here |
| cd  | change directory  | cd / or simple cd will take to root directory |
| cd <DIRECTORY_NAME> | change directory to given one | immediate sub-directory of "/" is home |
| cd .. | to go to parent directory | remember the space |
| cd ../.. | moving through multiple levels of parent directories | remember the space |

## Useful Addons/Applications

1. xtrlock
   > - Locks X display until the password is supplied, leaving the windows visibile. This is great if you want to lock your screen, but still keep windows visible.
   > - Install via `sudo apt-get install xtrlock`
   > - Kindly note that this will only work well on systems containing the *[X display server](https://ubuntu.com/tutorials/command-line-for-beginners)*. Hence it's most likely to not work in modern versions of Ubuntu
2. xwinwrap
   > - A lightweight application that allows you to set a video/gif as a desktop wallpaper. For more details on implementation visit [ujjwal96/xwinwrap](https://github.com/ujjwal96/xwinwrap) and this Reddit [post](https://www.reddit.com/r/archlinux/comments/8jnnm3/how_do_i_set_a_gif_as_my_background_with_xwinwrap/)
   > - This application is limited to devices containing the X display server.




