# Introduction
This document provides a comprehensive overview of the basic configuration of a Git environment as completed in Lab 1 for the Distributed Systems subject.

# Goals
- Install and configure Git.
- Understand and apply local and global configurations.

# Installation and Configuration
All the screenshots for this lab will be attached in the appendix.

## Step 0: Running `whoami` script (see Appendix A)
```sh
echo "$(whoami): $(date "+%Y-%m-%d %H:%M:%S")"
```

## Step 1: Installing Git (see Appendix B)
Navigate to our folder:
```sh
cd ~/Downloads/2025-2-UNAM/
mkdir distributed_systems
cd distributed_systems/
```

Install Git: Use Homebrew to install Git:
```sh
brew install git # I have a macOS ARM-based processor and use brew package manager.
```

Verify Installation: Check the installed version of Git:
```sh
git --version
```

## Step 2: Configuring Git (see Appendix C)
### Global Configuration
Set the default branch, preferred editor, and user details globally:
```sh
git config --global init.defaultBranch main
git config --global core.editor "vim"
git config --global user.name "Aldo Navarrete"
git config --global user.email "aldo.navarrete@fi.unam.edu"
```

View all global configurations:
```sh
git config --global --list
```

### Local Configuration
Configure local settings within a specific repository:
```sh
git init
git config --local user.email "aldo.navarrete@fi.unam.edu"
git config --local user.name "aldonavarretefp"
```

We can list all configurations with the following command:
```sh
git config --local --list
```

## Step 3: Using Git
### Create and Modify Files
Create a new file and track changes:
```sh
echo "Hello World" > file.txt
git add file.txt
git commit -m 'adding file.txt with a welcome message'
```

### Branching and Merging
Manage branches for features and fixes:
```sh
git branch feature/add-file
git checkout feature/add-file
```

### Viewing Logs and Status
Use various Git commands to view repository history and status:
```sh
git status
git log --graph --oneline
git adog
```

# Challenge
Research the difference between local and global configurations and explain their differences. Repeat steps 1 to 3 for the local configurations. (see Appendix C)

## Difference Between Local and Global Configurations
- **System Git config** controls settings for all users and all repositories on your computer.
- **Global Git config** controls settings for the currently logged-in user and all their repositories.

To repeat steps 1 and 3, we created a local Git repository and changed the local configuration (see Appendix C for execution).

### Configure Your Username
```sh
git config --global user.name "Aldo Navarrete"
git config --local user.name "aldonavarretefp"
```

### Configure Email
```sh
git config --local user.email "aldo.navarrete@fi.unam.edu"
```

### Set the Default Branch: `main`
```sh
git config --global init.defaultBranch main
```

# Conclusion
The lab provided a practical introduction to setting up and managing our Git environment (in my case, using macOS). The configurations and commands were documented to complete this laboratory successfully.

# Appendix
## Appendix A. Whoami Command
## Appendix B. Git Installation
## Appendix C. Git Configuration Commands

# References
Tomas, I. (n.d.). System vs Global vs Local Git config. Retrieved from [ihatetomatoes.net](https://ihatetomatoes.net/git-config-tutorial/#:~:text=System%20vs%20Global%20vs%20Local%20Git%20config&text=System%20Git%20config%20controls%20settings,settings%20for%20a%20specific%20repository)
