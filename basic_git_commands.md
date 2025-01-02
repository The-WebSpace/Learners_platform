# Git and Github

### Git: 
- A Version Control System Software
- Tracks changes in code
- Platform for collaboration

### Github
- Website to store and manage repositories (folder) using git

### Basic git terminologies
- **Repository**: Folder

- **Local Repo**: Local Repository (folder on your pc or the system you are working on)

- **Remote Repo**: Remote Repository (folder in the github)

## Setting-up git 
- In windows: 
> Requirements: VS code, Git bash (Install both)

- In MAC:
> Requirements: VS code, Terminal (Terminal might be pre-installed, just check by searching terminal)

#### To Check if Git is installed 
```
git --version //checks the version of installed git, if not installed then shows git as unrecognised command
```
## Configure Git (In local repo)
Git can be configured locally and globally. But for now lets look at how to configure it globally.
```
git config --global user.name "Your Name Here"
git config --global user.email "youremail@email.com"
git config --list              //checks the configuration details
```
