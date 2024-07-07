# Git-Github-Notes
### 1. What is a Version Control System?
Version control, also known as source control, is tracking and managing software code changes.

Famous VCS:

- Git (Most Famous)
- Apache SubVersion
- Piper (Used by Google)


### 2. Introduction to Git VCS
- What is Git?
- Installation of Git CLI
- Basic Git Commands
    - Setting up Git Global Configuration
    - Here's a cheat sheet for mostly used git commands : https://education.github.com/git-cheat-sheet-education.pdf

### SETUP
Configuring user information used across all local repositories
git config --global user.name “[firstname lastname]”
set a name that is identifiable for credit when review version history
git config --global user.email “[valid-email]”
set an email address that will be associated with each history marker
git config --global color.ui auto
set automatic command line coloring for Git for easy reviewing
To verify you settings use
git config --global --list

### 3. Version Controlling with Git
- Initializing Git Project
- Adding Files to VCS
    - For tracking Particular file use : git add <FILE_PATH>
    - For tracking all files use : git add . 
- Removing Files from VCS
    - git rm <FILE_PATH>
- Introduction to Commits
    - Committing Files
        - git commit -m "MESSAGE"
    - Staging Area
    - Logging Commit History
        - git log
        - git log --oneline
    - Reverting Back
