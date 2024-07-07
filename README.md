**Git-Github-Notes**
=====================

### 1. What is a Version Control System?

Version control, also known as source control, is the process of tracking and managing software code changes. Some famous version control systems include:

* Git (most famous)
* Apache SubVersion
* Piper (used by Google)

### 2. Introduction to Git VCS

#### What is Git?

Git is a version control system that allows you to track and manage changes to your code.

#### Installation of Git CLI

To install Git, follow the instructions for your operating system.

#### Basic Git Commands

Here are some basic Git commands to get you started:

* Setting up Git global configuration:
	+ `git config --global user.name "[firstname lastname]"`
	+ `git config --global user.email "[valid-email]"`
	+ `git config --global color.ui auto`
* To verify your settings, use: `git config --global --list`

You can find a cheat sheet for mostly used Git commands here: https://education.github.com/git-cheat-sheet-education.pdf

### 3. Version Controlling with Git

#### Initializing a Git Project

To initialize a Git project, use: `git init`

#### Adding Files to VCS

To track a particular file, use: `git add <FILE_PATH>`

To track all files, use: `git add .`

#### Removing Files from VCS

To remove a file from VCS, use: `git rm <FILE_PATH>`

#### Introduction to Commits

A commit is a snapshot of your project's code at a particular point in time. It's a way to save your changes and track the history of your project.

#### What is a Commit?

A commit is a collection of changes made to your code, along with a message that describes those changes.

#### The Commit Process

Here's a step-by-step overview of the commit process:

1. **Make changes**: Make changes to your code, such as adding new files, modifying existing files, or deleting files.
2. **Stage changes**: Use `git add` to stage the changes you want to commit.
3. **Commit changes**: Use `git commit` to commit the staged changes.
4. **Create a commit**: Git creates a new commit, which includes the changes you made, the commit message, and other metadata.

#### Commit Message

The commit message is a brief description of the changes you made. A good commit message should:

* Be concise and clear
* Describe the changes you made
* Explain why you made the changes

#### Best Practices for Commits

Here are some best practices to keep in mind when working with commits:

* **Make frequent commits**: Commit your changes regularly to keep your repository up-to-date.
* **Write good commit messages**: Take the time to write clear and concise commit messages.
* **Use meaningful commit messages**: Use keywords and phrases that describe the changes you made.
* **Keep commits small**: Try to keep each commit focused on a single change or feature.

#### Staging Area

The staging area is where you prepare your changes to be committed.

#### Logging Commit History

To view your commit history, use:

* `git log`
* `git log --oneline`, this commands display the commit history in concise manner.

