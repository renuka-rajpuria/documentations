### Setting up Git

Step 1.1: Update the system

Run these commands in the terminal to update the Linux system:
```
sudo apt update
sudo apt upgrade
```

Step 1.2: Install git

You likely have git installed already, but to make sure that we have the most up to date version of git, run the following commands:

```
sudo add-apt-repository ppa:git-core/ppa
sudo apt update
sudo apt install git
```

Step 1.3: Verify version

Make sure your git version is at least 2.28 by running this command:
```
git --version
```

If the version number is less than 2.28, follow the instructions again.


- Cloning the repository:
```
git clone <REPOSITORY_HTTPS_LINK>
```

- Moving a file to repository:
```
mv <FILE_NAME>
cd <REPOSITORY_NAME>/
git status
```

- Pushing your commit into git
```
git add <FILE_NAME>
git commit -m "<COMMIT_MESSAGE>"
```
