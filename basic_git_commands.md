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

## Link local repo with remote repo (if git initialized with git init)
3. **git remote add origin repository_url**: Origin denotes the remote repository and repository_url denotes the specific remote repository 
   ```
   git remote add origin repository_url
   ```
   

## Adding and Committing Changes

4. **git add .**  
   Stage all changes in the current directory.
   ```bash
   git add .
   ```

5. **git commit -m "Your commit message"**  
   Commit staged changes with a message.
   ```bash
   git commit -m "Your commit message"
   ```

## Branching 

6. **git branch**
   Check which branch we are currently working on
   ```
   git branch
   ```
   
7. **git branch branch_name**  
   Create a new branch named `branch_name`.
   ```bash
   git branch branch_name
   ```

8. **git branch -M new_branch_name**
   Rename the current branch name to new_branch_name
   ```
   git branch -M new_branch_name
   ```
   
9. **git checkout branch_name**  
    Switch to the branch named `branch_name`.
    ```bash
    git checkout branch_name
    ```
    
10. **git checkout -b branch_name**  
    Create and Switch to the branch named `branch_name`.
    ```bash
    git checkout -b branch_name
    ```
    
11. **git branch -d branch_name**  
    Delete the branch named `branch_name`.
    ```bash
    git branch -d branch_name
    ```

## Pushing and Pulling Changes

12. **git push origin branch_name**  
    Push changes to the specified branch on the remote repository.
    ```bash
    git push origin branch_name
    ```

13. **git pull origin branch_name**  
    Pull updates from the specified branch on the remote repository.
    ```bash
    git pull origin branch_name
    ```

## Checking Status and Logs

14. **git status**  
   Check the current status of your repository, including changes and staged files.
   ```bash
   git status
   ```
   To check the status of your repository from the notation in right side of the file-

   **M** Modified (Changes not staged for commit)

   **U** Untracked file (New file that is not staged for commit)

15. **git log**  
   View the commit history.
   ```bash
   git log
   ```


## Undoing Changes

16. Undoing the staged changes (undo git add)  
    
    ```bash
    git reset    //to undo all staged files
    git reset file_name   //to undo specific staged file named "file_name"
    or
    git restore --stage file_name   //same as git reset file_name
    ```

17. **Undo commits**  
    
    ```bash
    git reset HEAD~1   //Resets last commit.
    git reset commit_hash   //commit hash can be seen using git log, copy the hash till which you want to keep
    git reset --hard commit_hash   //resets commit from VS code as well
    ```

