# Lab: Setting Up Git and Pushing to GitHub via CLI

---

## General Information

| Item | Details |
| :--- | :--- |
| Platform | Local Lab (Kali Linux) |
| Objective | Clone repository, configure Git identity, and use PAT for authentication |
| Target OS | Linux (Debian-based) |
| Difficulty | Beginner |

---

## Process Summary

The objective of this practice was to successfully clone a GitHub repository to a local Kali Linux machine, make file modifications, and securely push those changes back to the remote repository using modern authentication methods.

The process covered:
1. **Repository Cloning:** Downloading the project to the local environment.
2. **Git Configuration:** Setting up user identity to sign commits.
3. **Authentication:** Bypassing the deprecated password method by using a GitHub Personal Access Token (PAT).

---

## Step-by-Step

### 1. Cloning the Repository
The repository was cloned from GitHub to the local machine using the command line. This created a local directory to track changes.

### 2. File Creation
A dedicated folder was created for project organization, and a documentation file was initiated using the `nano` text editor.

### 3. Identity Configuration
Git initially blocked the commit process because the author's identity was unknown. The default global email and username were configured to allow Git to sign the changes.

### 4. Pushing Changes with PAT
Standard password authentication failed because GitHub no longer supports it for Git operations. A Personal Access Token (PAT) was generated in GitHub's developer settings and used as the password to successfully authenticate and push the files.

---

## Commands Used

```bash
# Cloning the project
git clone [https://github.com/Arcanjo-Gabriel/tryHackMe-Writeups.git](https://github.com/Arcanjo-Gabriel/tryHackMe-Writeups.git)

# Navigating directories
cd tryHackMe-Writeups

# Configuring identity
git config --global user.email "your_email@example.com"
git config --global user.name "Arcanjo-Gabriel"

# Staging and committing
git add .
git commit -m "Add Linux-Basics room writeup"

# Pushing to remote repository
git push
