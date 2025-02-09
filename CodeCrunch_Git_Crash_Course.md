# Git and GitHub

## Git & GitHub Walkthrough

Git and GitHub are tools we will be using throughout the course to track and store changes to our code, collaborate with others, and keep everything in sync.

This guide introduces using Git with the terminal and GitHub web UI.

**Note:** You do not need GitHub to use Git, but you cannot use GitHub without using Git.

---

## Overview

### What is Git?
Git is software for tracking changes in any set of files, usually used for coordinating work among programmers collaboratively developing source code during software development. [(Read more)](https://en.wikipedia.org/wiki/Git).

### What is GitHub?
GitHub is a code hosting platform for version control and collaboration. It lets you and others work together on projects from anywhere.

### Why use Git?
Version control is very important. Without it, you risk losing your work. With Git, you can save your work as often as you like and revert to previous versions when necessary.

> **Tip:** Commit often and commit early. This way, you'll never have that gut-sinking feeling of overwriting or losing changes.

---

## Initial Setup

To get started, you will need to download, install, and configure Git on your computer and create a free GitHub account.

### Install Git
Download the latest version based on your operating system:
- [Mac](https://git-scm.com/download/mac)
- [Windows](https://git-scm.com/download/win)
- [Linux](https://git-scm.com/download/linux)

Follow the instructions provided during the installation.

### Verify Installation
Open a terminal and type:
```sh
git --version
```
This will confirm if Git is installed correctly.

### Setting Your User in Git
Git uses a username and email to associate commits with an identity. Set your user details with:
```sh
git config --global user.name "Your Name"
git config --global user.email "email@example.com"
```

### Authenticating with GitHub
When connecting to a GitHub repository from Git, you must authenticate using either HTTPS or SSH. We recommend using HTTPS and caching your credentials following [these instructions](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/caching-your-github-credentials-in-git).

---

## Working with Git & GitHub Through the Command Line

### General Development Flow
1. Make local code changes on your computer.
2. Commit your local changes to save your progress.
3. Push new changes to GitHub to store them in the cloud.
4. Pull the latest changes from GitHub to keep your local code updated.

### Setting Up a Local Git Repository
Create a new project directory, navigate into it, and initialize a Git repository:
```sh
mkdir newproject
cd newproject/
git init
```

### Adding and Committing Changes
Check for changes in your working directory:
```sh
git status
```
Stage files for commit:
```sh
git add <file>
```
Or stage all changes:
```sh
git add .
```
Commit your changes:
```sh
git commit -m "Your commit message"
```

### Creating a New Repository on GitHub
1. Log in to [GitHub](https://github.com/).
2. Click the `+` in the top-right and select **New repository**.
3. Enter a repository name and optional description.
4. Choose the repository visibility.
5. Click **Create repository**.

For more details, see GitHub's [Creating a new repository](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository).

### Linking the Local Repository to GitHub
Connect your local repository to the GitHub repository:
```sh
git remote add origin https://github.com/yourUserName/yourRepoName.git
```
Push your local changes to GitHub:
```sh
git push -u origin main
```
Refresh your repository on GitHub to see your code.

### Syncing Local and Remote Repositories
To pull the latest changes from GitHub:
```sh
git pull
```
> **Note:** `git pull` fetches and merges changes. If auto-merge is not possible, you'll need to resolve conflicts manually.

### Cloning a Remote Repository
To clone an existing repository from GitHub:
1. Copy the repository's HTTPS URL from GitHub.
2. Open a terminal and navigate to the desired directory.
3. Run:
   ```sh
   git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY
   ```

### Setting Up a Repository from Starter Code
If provided with starter code, follow these steps:
1. Download the starter code from the GitHub repository (as a ZIP file).
2. Extract it to a suitable location on your computer.
3. Initialize a Git repository:
   ```sh
   cd /path/to/unzipped/project
   git init
   git add .
   git commit -m "Initial starter code setup"
   ```

---

## Further Reading
- [GitHub Flow](https://guides.github.com/introduction/flow/)
- [Git Documentation](https://git-scm.com/doc)
- [GitHub Docs](https://docs.github.com/en)

Happy Coding! 🚀
