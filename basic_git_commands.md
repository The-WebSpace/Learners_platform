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

- **Staged Files**: Files that are not added (either using + sign in the source control or using git add .) 

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
# Some Common Git Commands (MUST KNOW)
## Initializing and cloning repository
A project might either be started by initiating a repo ourselves (git init would help here) or by cloning already existing repo. 


1. **git init**: Use this if local repo is to be created first and we just need to push it to remote repo
   Creates new hidden file named .git 
   Initialize a new Git repository in the current directory.
   ```bash
   git init
   ```

2. **git clone repository_url**: Use this if remote repo is created and we need to pull that to local repo
   Clone an existing repository from GitHub.
   ```bash
   git clone repository_url
   ```

## Checking Status and Logs

3. **git status**  
   Check the current status of your repository, including changes and staged files.
   ```bash
   git status
   ```
   To check the status of your repository from the notation in right side of the file-

   **M** Modified (Changes not staged for commit)

   **U** Untracked file (New file that is not staged for commit)

5. **git log**  
   View the commit history.
   ```bash
   git log
   ```

## Adding and Committing Changes

5. **git add .**  
   Stage all changes in the current directory.
   ```bash
   git add .
   ```

6. **git commit -m "Your commit message"**  
   Commit staged changes with a message.
   ```bash
   git commit -m "Your commit message"
   ```

## Branching and Merging

7. **git branch branch_name**  
   Create a new branch named `branch_name`.
   ```bash
   git branch branch_name
   ```

8. **git checkout branch_name**  
    Switch to the branch named `branch_name`.
    ```bash
    git checkout branch_name
    ```

9. **git merge branch_name**  
    Merge the specified branch into the current branch.
    ```bash
    git merge branch_name
    ```

## Pushing and Pulling Changes

10. **git push origin branch_name**  
    Push changes to the specified branch on the remote repository.
    ```bash
    git push origin branch_name
    ```

11. **git pull origin branch_name**  
    Pull updates from the specified branch on the remote repository.
    ```bash
    git pull origin branch_name
    ```

## Undoing Changes

12. **git reset --hard HEAD~1**  
    Revert to the previous commit (destructive).
    ```bash
    git reset --hard HEAD~1
    ```

13. **git checkout file_name**  
    Discard changes in a specific file.
    ```bash
    git checkout file_name
    ```

