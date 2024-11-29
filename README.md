# Git Basics

## What is Git?
Git is a version control system (VCS) that allows you to manage and keep track of your source code history. It helps you collaborate with other developers by allowing multiple people to work on the same project simultaneously.

Git records changes in your project and stores them in repositories (repos). You can commit changes, revert them, and track modifications over time.

---

## Git Basic Concepts

1. **Repository (Repo)**: A repository is where your project’s files and history are stored. It can either be local (on your computer) or remote (on platforms like GitHub, GitLab, or Bitbucket).

2. **Commit**: A commit is like a snapshot of your project at a particular point in time. When you commit your changes, Git saves the state of your files.

3. **Branch**: A branch is a version of your code. By default, every Git repository has a `main` (or `master`) branch. You can create new branches to work on new features without affecting the main code.

4. **Clone**: Cloning means copying a remote repository to your local machine.

5. **Push and Pull**: 
   - **Push**: Uploads your local changes to the remote repository.
   - **Pull**: Downloads changes from the remote repository to your local machine.

---

## Setting Up Git and GitHub

### Step 1: Install Git
First, make sure you have Git installed on your system:
- [Download Git](https://git-scm.com/downloads)

After installing, you can check if it's installed by running:
```bash
git --version
```

### Step 2: Configure Git
Set your Git user name and email (these will be used for your commits):
```bash
git config --global user.name "Your Name"
git config --global user.email "youremail@example.com"
```

### Step 3: Create a New Git Repository
1. Open a terminal (or PowerShell on Windows).
2. Navigate to the folder where you want to initialize the Git repository:
   ```bash
   cd path/to/your/project
   ```

3. Initialize the repository:
   ```bash
   git init
   ```

   This creates a new `.git` folder in your project, marking it as a Git repository.

---

## Basic Git Commands

### 1. `git status`
Shows the current state of the repository (e.g., which files have been modified, added, or deleted).

```bash
git status
```

### 2. `git add`
Stages changes for commit (prepares them to be committed).

- Add a single file:
  ```bash
  git add filename
  ```

- Add all changes in the current directory:
  ```bash
  git add .
  ```

### 3. `git commit`
Commits your staged changes with a message describing what you changed.

```bash
git commit -m "Your commit message"
```

### 4. `git log`
Shows the commit history of the repository.

```bash
git log
```

### 5. `git branch`
Shows the current branch and all other branches in your repository.

```bash
git branch
```

- To create a new branch:
  ```bash
  git branch new-branch-name
  ```

- To switch to another branch:
  ```bash
  git checkout branch-name
  ```

- To create and switch to a new branch in one command:
  ```bash
  git checkout -b new-branch-name
  ```

### 6. `git merge`
Merges changes from one branch into the current branch.

```bash
git merge branch-name
```

### 7. `git push`
Pushes your changes to a remote repository (e.g., GitHub).

- If you’re pushing for the first time:
  ```bash
  git push -u origin branch-name
  ```

- For subsequent pushes:
  ```bash
  git push
  ```

### 8. `git pull`
Pulls the latest changes from the remote repository to your local repository.

```bash
git pull
```

### 9. `git clone`
Clones a remote repository to your local machine.

```bash
git clone https://github.com/username/repository.git
```

### 10. `git remote add`
Links your local repository to a remote repository (e.g., on GitHub).

```bash
git remote add origin https://github.com/username/repository.git
```

---

## Common Git Workflow

1. **Create a repository** (or clone an existing one):
   ```bash
   git init      # For new repos
   git clone URL # To clone a remote repo
   ```

2. **Make changes** in your project.

3. **Add changes** to staging area:
   ```bash
   git add .
   ```

4. **Commit the changes**:
   ```bash
   git commit -m "Your commit message"
   ```

5. **Push your changes** to GitHub (or any remote repository):
   ```bash
   git push -u origin main
   ```

6. **Pull changes** from the remote repository if there are updates:
   ```bash
   git pull
   ```

---

## Branching and Merging

Git allows you to work on different features in different branches.

### 1. Creating and Switching Branches
To create and switch to a new branch:
```bash
git checkout -b new-branch
```

### 2. Merging Branches
When you are done working on your branch, you can merge it into the `main` branch:
```bash
git checkout main
git merge new-branch
```

---

## Git Ignore
Git ignores files you don’t want to track, like log files, build directories, or sensitive data. You can specify these files in a `.gitignore` file.

Example `.gitignore`:
```
node_modules/
dist/
*.log
```

---

## Next Steps
Once you get comfortable with the basic commands, you can dive deeper into more advanced Git features, such as:

- **Git Rebase**: Reapply commits on top of another base commit.
- **Git Cherry-pick**: Apply changes from a specific commit.
- **Git Stash**: Temporarily save changes that you’re not ready to commit.
- **Git Tag**: Mark specific points in history as important (e.g., releases).
