### 1. Install Git

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

### 2. Configure Git and GitHub

Go to GitHub.com and create an account! During the account setup, it will ask you for an email address. This needs to be a real email, and will be used by default to identify your contributions. If you are privacy conscious, or just don’t want your email address to be publicly available, make sure you tick the following two boxes on the Email Settings page after you have signed in:

- GitHub Email Settings

Having these two options enabled will prevent you accidentally exposing your personal email address when working with Git and GitHub.

You may also notice an email address under the Keep my email addresses private option, this is your private GitHub email address. If you plan to use this, make note of it now as you will need it when setting up Git in the next step.

- Setup Git (Do check the [reference](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-personal-account-on-github/managing-email-preferences/setting-your-commit-email-address))

For Git to work properly, we need to let it know who we are so that it can link a local Git user (you) to GitHub. When working on a team, this allows people to see what you have committed and who committed each line of code.

The commands below will configure Git. Be sure to enter your own information inside the quotes (but include the quotation marks)!
```
git config --global user.name "Your Name"
git config --global user.email "yourname@example.com"
```

If you opted to use the private GitHub email address, the second command will look something like this:
```
git config --global user.email "123456789+odin@users.noreply.github.com" # Remember to use your own private GitHub email here.
```

GitHub recently changed the default branch on new repositories from master to main. Change the default branch for Git using this command:
```
git config --global init.defaultBranch main
```
To enable colorful output with git, type
```
git config --global color.ui auto
```

You’ll also likely want to set your default branch reconciliation behavior to merging. You’ll learn what all those terms mean later in the curriculum, but for now just know that we suggest running the below command as part of the Git setup process when doing The Odin Project.
```
git config --global pull.rebase false
```

To verify that things are working properly, enter this command and verify whether the output matches your name, email address and other settings.
```
git config --list
```

In case you have made any errors and want to reconfigure git use:
```
rm ~/.gitconfig
```
Remember to rewrite all the previous commands in Configure Git and Github after this.

---- 

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
