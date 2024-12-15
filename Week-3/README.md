# Git and Version Control Training Documentation

Welcome to the **Git and Version Control Training** repository! This repository serves as a comprehensive guide to help you learn and master Git, version control, and related workflows. Whether you're new to Git or looking to refine your skills, this training is designed to equip you with practical knowledge for real-world applications in software development and DevOps.

---

## Table of Contents

1. [Introduction](#introduction)
2. [What is Git?](#what-is-git)
3. [What is Version Control?](#what-is-version-control)
4. [Key Terms in Git](#key-terms-in-git)
5. [Essential Git Commands](#essential-git-commands)
6. [GitHub Setup and Usage](#github-setup-and-usage)
   - [Signing Up on GitHub](#signing-up-on-github)
   - [Using Git Locally](#using-git-locally)
7. [Using Git with Visual Studio Code](#using-git-with-visual-studio-code)
8. [Git Workflow](#git-workflow)
   - [Cloning a Repository](#cloning-a-repository)
   - [Committing Changes](#committing-changes)
   - [Pushing Changes](#pushing-changes)
9. [SSH Keys for GitHub](#ssh-keys-for-github)
10. [Git Workflow Review](#git-workflow-review)
11. [Git Branching](#git-branching)
12. [Undoing Changes in Git](#undoing-changes-in-git)
13. [Forking in Git](#forking-in-git)
14. [Conclusion](#conclusion)

---

## 📚 Introduction
Git is a powerful version control system that enables developers to collaborate, track changes, and manage codebases effectively. In this training, you'll learn the fundamentals of Git, how to use GitHub, and best practices for version control.

---

## 🎯 What is Git?
Git is a distributed version control system that allows multiple developers to work on a project simultaneously while tracking changes, merging code, and maintaining a history of modifications.

---

## 🗂️ What is Version Control?
Version control is the practice of managing changes to code or documents over time. It ensures collaboration, prevents conflicts, and provides a history of revisions for easy rollback when needed.

---

## 📝 Key Terms in Git
Understanding these terms will help you navigate Git effectively:
- **Repository**: A project containing files and their history.
- **Commit**: A snapshot of changes made to the files.
- **Branch**: A separate line of development.
- **Merge**: Combining changes from one branch into another.
- **Pull**: Fetching and integrating changes from a remote repository.
- **Push**: Sending local changes to a remote repository.
- **Fork**: Creating a personal copy of someone else's repository.

---

## 🛠️ Essential Git Commands
Here are some of the most frequently used Git commands:
- `git init`: Initializes a new Git repository.
- `git clone <repository>`: Copies a remote repository locally.
- `git add <file>`: Stages changes for the next commit.
- `git commit -m "message"`: Saves changes with a message.
- `git push`: Uploads local changes to a remote repository.
- `git pull`: Updates local repository with changes from remote.
- `git branch`: Lists, creates, or deletes branches.
- `git merge <branch>`: Merges another branch into the current one.

---

## 🌐 GitHub Setup and Usage

### Signing Up on GitHub
1. Visit [GitHub](https://github.com) and create an account.
2. Verify your email address and log in to access GitHub features.

---

### Using Git Locally
1. **Install Git**: Follow the instructions for your operating system:
   - Windows: Download and install Git from [git-scm.com](https://git-scm.com/).
   - macOS/Linux: Use a package manager (`brew install git` or `apt install git`).
2. **Set Up a Code Editor**:
   - Download and install [Visual Studio Code](https://code.visualstudio.com/).
3. **Configure Git**:
   ```bash
   git config --global user.name "Your Name"
   git config --global user.email "your.email@example.com"

---

## 🖥️ Using Git with Visual Studio Code
Cloning a Repository
1. Open Visual Studio Code.
2. Use the Source Control tab or terminal to clone a repository:
```bash
    git clone <repository-url>
```

**Committing Changes**
1. Stage changes:
```bash
    git add <file>
```

2. Commit changes with a message:
```bash
    git commit -m "Describe your changes"
```

**Pushing Changes**
Send your committed changes to the remote repository:
```bash
    git push
```
---

## 🔒 SSH Keys for GitHub
SSH keys provide secure authentication for GitHub:

1. Generate an SSH key:
```bash
    ssh-keygen -t ed25519 -C "your.email@example.com"
```

2. Add the key to GitHub via your account settings.

---

## 🔁 Git Workflow Review

**Local Workflow
1. Clone the repository.
2. Make changes and commit them.
3. Push changes to the remote repository.

**GitHub Workflow
1. Fork a repository.
2. Clone your fork locally.
3. Make changes, push them to your fork, and submit a pull request.


---

## 🌲 Git Branching
Branches allow multiple lines of development:

- Create a new branch:
```bash
    git branch <branch-name>
    git checkout <branch-name>
```

- Merge changes from another branch:
``` bash
    git merge <branch-name>
```
---

## ⏪ Undoing Changes in Git
- Undo staged changes:
```bash
    git reset <file>
```

- Revert a commit:
```bash
    git revert <commit-hash>
```
---

## 🔄 Forking in Git
Forking creates a personal copy of a repository:

1. Click the Fork button on GitHub.
2. Clone the fork to your local machine.
3. Make changes and create a pull request to propose updates to the original repository.

---

## 📖 Conclusion
This training provides a solid foundation in Git and version control. By mastering these skills, you can confidently manage codebases, collaborate with teams, and streamline your development workflow.