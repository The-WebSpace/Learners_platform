# Git and GitHub: A Beginner's Guide

### **What is Git?**
- Git is a powerful Version Control System (VCS) used by developers to track changes in their code.
- It allows multiple people to collaborate on the same project without overwriting each other's work.
- Think of Git as a time machine for your code—you can go back to any previous version at any time.

### **What is GitHub?**
- GitHub is a web-based platform that hosts Git repositories (folders with version-controlled code).
- It acts as a central hub where developers can store their code, collaborate with others, and manage projects.
- While Git is the tool, GitHub is the service that enhances collaboration.

---

### **Basic Git Terminologies**
- **Repository (Repo)**: A folder that contains your project's files and their version history.
- **Local Repo**: The repository on your computer where you make changes.
- **Remote Repo**: The repository stored on GitHub.
- **Staged Files**: Files prepared for the next commit (marked using `git add`).

---

## **Setting Up Git**

### **For Windows Users:**
- Requirements: Install **VS Code** and **Git Bash**.

### **For Mac Users:**
- Requirements: Install **VS Code**. The Terminal app is pre-installed; you can use it directly.

#### **How to Check if Git is Installed**
1. Open your terminal (Git Bash on Windows, Terminal on Mac).
2. Run the following command:
   ```
   git --version
   ```
   - If Git is installed, it will display the installed version.
   - If not, it will show an error indicating Git is not recognized.

---

## **Configuring Git Globally**
Before using Git, configure your name and email (these details appear in your commits).

```bash
# Set your name
git config --global user.name "Your Name Here"

# Set your email
git config --global user.email "youremail@email.com"

# Check your configuration
git config --list
```
This configuration applies to all repositories on your computer.

---

# **Essential Git Commands**

### **Starting a New Project**
1. **Initialize a Repository:**
   If your project is new, you need to initialize it as a Git repository.
   ```bash
   git init
   ```
   - This creates a hidden `.git` folder in your project directory to track changes.

2. **Cloning an Existing Repository:**
   If the project already exists on GitHub, clone it to your local machine.
   ```bash
   git clone <repository_url>
   ```
   - Replace `<repository_url>` with the GitHub repository link.

## **Connecting a Local Repository to GitHub**
1. If you initialized the repository locally, link it to a remote GitHub repository:
      ```bash
      git remote add origin <repository_url>
      ```
- `origin` is the name of the remote.
- `<repository_url>` is the URL of your GitHub repository.

2. Checking Out the Remote Branch Directly on Local Device (Detached HEAD Mode):
      ```
      git checkout origin/<branch-name>
      ```
   - Detached HEAD mode means you can view files, but any commits you make won't be attached to a branch.
   - If you try to commit, Git will warn you that you're not on a branch.

3. Checking Out the Remote Branch on Local Device by creating branch:
      ```
      git checkout -b <branch-name> origin/<branch-name>
      ```
 - Now you are on a proper local branch that tracks origin/<branch-name>.
---

## **Adding and Committing Changes**
1. **Stage Changes:**
   Add all modified files to the staging area (preparing them for commit):
   ```bash
   git add .
   ```
   - The `.` stages all changes in the current directory.

2. **Commit Changes:**
   Save the staged changes with a descriptive message:
   ```bash
   git commit -m "Your commit message"
   ```
   - Example: `git commit -m "Added user authentication feature"`.

---

## **Working with Branches**
Branches allow you to work on new features or fixes without affecting the main code.

1. **Check Current Branch:**
   ```bash
   git branch
   ```
   - The branch with an asterisk (`*`) is your current branch.

2. **Create a New Branch:**
   ```bash
   git branch <branch_name>
   ```
   - Replace `<branch_name>` with the desired name for your branch.

3. **Switch to a Branch:**
   ```bash
   git checkout <branch_name>
   ```

4. **Create and Switch to a Branch:**
   ```bash
   git checkout -b <branch_name>
   ```

5. **Rename the Current Branch:**
   ```bash
   git branch -M <new_branch_name>
   ```

6. **Delete a Branch:**
   ```bash
   git branch -d <branch_name>
   ```

---

## **Syncing Changes**

1. **Push Changes to GitHub:**
   ```bash
   git push origin <branch_name>
   ```
   - Upload your changes to the remote repository on the specified branch.

2. **Pull Changes from GitHub:**
   ```bash
   git pull origin <branch_name>
   ```
   - Fetch and merge updates from the specified branch of the remote repository.

---

## **Stashing Changes**
If you need to pull updates but have uncommitted changes, stash them temporarily:

1. **Save Changes to Stash:**
   ```bash
   git stash
   ```
   - This clears the working directory without losing your changes.

2. **Apply Stashed Changes:**
   ```bash
   git stash pop
   ```

3. **Clear All Stashed Changes:**
   ```bash
   git stash clear
   ```

---

## **Checking Repository Status**
1. **Check Current Status:**
   ```bash
   git status
   ```
   - Look for files marked as modified (M), untracked (U), or staged for commit.

2. **View Commit History:**
   ```bash
   git log
   ```
   - Shows a history of commits.
   - The output of git log looks like:
   ```
   commit a1b2c3d4e5f6g7h8i9j0k1l2m3n4o5p6q7r8s9t
   Author: Your Name <youremail@example.com>
   Date:   Wed Dec 27 10:30:00 2023 +0000

   Added feature X to the project
   ```
   Here, a1b2c3d4e5f6g7h8i9j0k1l2m3n4o5p6q7r8s9t is the commit hash representing the specific commit with commit message "Added feature X to the project"
---

## **Undoing Changes**

1. **Undo Staged Changes:**
   ```bash
   git reset <file_name>
   ```
   - Removes the specified file from the staging area.

2. **Undo the Last Commit:**
   ```bash
   git reset HEAD~1
   ```
   - Keeps the changes but removes the commit.

3. **Undo a Push:**
   - Option 1: Revert the commit (recommended for public branches):
     ```bash
     git revert <commit_hash>
     ```
   - Option 2: Reset the branch and force push:
     ```bash
     git reset --hard <commit_hash>
     git push origin <branch_name> --force
     ```

---

## **Removing Git from a Directory**
If you initialized Git by mistake, remove the `.git` folder:
```bash
rm -r -force .git
```
- This removes the repository but keeps your files.

This command will:
- Remove (rm) the hidden .git directory recursively (-r)
- Use -force flag since .git contains read-only files
---





