**Git-Github-Notes**
=====================

**What is a Version Control System?**
---------------------------

Version control, also known as source control, is the process of tracking and managing software code changes. Some famous version control systems include:

* Git (most famous)
* Apache SubVersion
* Piper (used by Google)

**Introduction to Git VCS**
---------------------------

**What is Git?**

Git is a version control system that allows you to track and manage changes to your code.

#### Installation of Git CLI

To install Git, follow the instructions for your operating system.

**Basic Git Commands**

Here are some basic Git commands to get you started:

* Setting up Git global configuration:
	+ `git config --global user.name "[firstname lastname]"`
	+ `git config --global user.email "[valid-email]"`
	+ `git config --global color.ui auto`
* To verify your settings, use: `git config --global --list`

You can find a cheat sheet for mostly used Git commands here: https://education.github.com/git-cheat-sheet-education.pdf

**Version Controlling with Git**
---------------------------

#### Initializing a Git Project

To initialize a Git project, use: `git init`

#### Adding Files to VCS

To track a particular file, use: `git add <FILE_PATH>`

To track all files, use: `git add .`

#### Removing Files from VCS

To remove a file from VCS, use: `git rm <FILE_PATH>`

**Introduction to Commits**
---------------------------

A commit is a snapshot of your project's code at a particular point in time. It's a way to save your changes and track the history of your project.

#### What is a Commit?

A commit is a collection of changes made to your code, along with a message that describes those changes.

**The Commit Process**
---------------------------

Here's a step-by-step overview of the commit process:

1. **Make changes**: Make changes to your code, such as adding new files, modifying existing files, or deleting files.
2. **Stage changes**: Use `git add` to stage the changes you want to commit.
3. **Commit changes**: Use `git commit` to commit the staged changes.
4. **Create a commit**: Git creates a new commit, which includes the changes you made, the commit message, and other metadata.

**Commit Message**
---------------------------

The commit message is a brief description of the changes you made. A good commit message should:

* Be concise and clear
* Describe the changes you made
* Explain why you made the changes

**Best Practices for Commits**
---------------------------

Here are some best practices to keep in mind when working with commits:

* **Make frequent commits**: Commit your changes regularly to keep your repository up-to-date.
* **Write good commit messages**: Take the time to write clear and concise commit messages.
* **Use meaningful commit messages**: Use keywords and phrases that describe the changes you made.
* **Keep commits small**: Try to keep each commit focused on a single change or feature.


**Staging Area?**
---------------------------

The staging area is a virtual space where you stage your changes before committing them. When you make changes to your code, you need to stage those changes before you can commit them. The staging area is where you prepare those changes to be committed.

**How Does the Staging Area Work?**
--------------------------------

Here's a step-by-step overview of how the staging area works:

1. **Make changes**: You make changes to your code, such as adding new files, modifying existing files, or deleting files.
2. **Stage changes**: You use the `git add` command to stage the changes you want to commit. This adds the changes to the staging area.
3. **Review changes**: You can review the changes in the staging area using `git status` or `git diff --staged`.
4. **Commit changes**: You use the `git commit` command to commit the staged changes. This creates a new commit in your Git repository.

**Benefits of the Staging Area**
-----------------------------

The staging area provides several benefits:

* **Allows for selective committing**: You can choose which changes to commit and which to leave out.
* **Enables review of changes**: You can review the changes in the staging area before committing them.
* **Helps with commit organization**: You can organize your commits by staging related changes together.

**Common Git Commands for the Staging Area**
-----------------------------------------

Here are some common Git commands related to the staging area:

* `git add <FILE_PATH>`: Stages a specific file or directory.
* `git add .`: Stages all changes in the current directory and subdirectories.
* `git reset <FILE_PATH>`: Unstages a specific file or directory.
* `git reset --hard`: Unstages all changes and resets the staging area to the last commit.
* `git status`: Displays the status of the staging area, including which files are staged and which are not.
* `git diff --staged`: Displays the differences between the staging area and the last commit.

**Best Practices for the Staging Area**
-----------------------------------

Here are some best practices to keep in mind when working with the staging area:

* **Use `git add` and `git reset` wisely**: Be careful when using these commands, as they can affect the staging area and your commit history.
* **Review your changes**: Always review the changes in the staging area before committing them.
* **Keep your commits organized**: Use the staging area to organize your commits by staging related changes together.

By understanding the staging area and using it effectively, you can improve your Git workflow and create more organized, meaningful commits.

**Logging Commit History**
-----------------------------

Logging commit history is a way to see all the changes made to your code over time. Git provides a command to do this.

**`git log` Command**
--------------------

The `git log` command shows a list of all commits made to your repository.

**Example**
```
$ git log
commit 3456789abcdef
Author: John Doe <john.doe@example.com>
Date:   Fri Mar 12 14:30:00 2021 +0000

    Initial commit

commit 1234567abcdef
Author: Jane Doe <jane.doe@example.com>
Date:   Thu Mar 11 10:00:00 2021 +0000

    Added new feature
```
This shows two commits:

* The first commit was made by John Doe on March 12, 2021, with the message "Initial commit".
* The second commit was made by Jane Doe on March 11, 2021, with the message "Added new feature".

**`git log --oneline` Command**
-----------------------------

The `git log --oneline` command shows a concise version of the commit history.

**Example**
```
$ git log --oneline
3456789abcdef Initial commit
1234567abcdef Added new feature
```
This shows the same two commits, but in a shorter format.

**Why Log Commit History?**
---------------------------

Logging commit history is useful for:

* Seeing what changes were made to your code
* Identifying who made changes and when
* Tracking down bugs or issues introduced in specific commits

By using `git log` and `git log --oneline`, you can easily see the history of changes made to your code.


**Reverting Back**
---------------------
Sometimes, you may want to revert back to a previous version of your code. This can be useful if you've made changes that you want to undo, or if you want to go back to a previous working version of your code.

**`git revert` Command**
---------------------

The `git revert` command is used to revert back to a previous commit.

**Example**
```
$ git revert <COMMIT_HASH>
```
Replace `<COMMIT_HASH>` with the hash of the commit you want to revert back to.

**How `git revert` Works**
-------------------------

When you run `git revert`, Git creates a new commit that reverses the changes made in the original commit. This new commit is then added to your commit history.

**Example Scenario**
-------------------

Let's say you've made some changes to your code, but you realize that you've introduced a bug. You want to revert back to the previous version of your code.

**Step 1: Find the Commit Hash**
```
$ git log
commit 3456789abcdef
Author: John Doe <john.doe@example.com>
Date:   Fri Mar 12 14:30:00 2021 +0000

    Made some changes

commit 1234567abcdef
Author: Jane Doe <jane.doe@example.com>
Date:   Thu Mar 11 10:00:00 2021 +0000

    Initial commit
```
You find the commit hash of the previous version of your code, which is `1234567abcdef`.

**Step 2: Revert Back**
```
$ git revert 1234567abcdef
```
Git creates a new commit that reverts back to the previous version of your code.

**Step 3: Verify the Changes**
```
$ git log
commit 7890123abcdef
Author: John Doe <john.doe@example.com>
Date:   Fri Mar 12 14:35:00 2021 +0000

    Revert "Made some changes"

commit 3456789abcdef
Author: John Doe <john.doe@example.com>
Date:   Fri Mar 12 14:30:00 2021 +0000

    Made some changes

commit 1234567abcdef
Author: Jane Doe <jane.doe@example.com>
Date:   Thu Mar 11 10:00:00 2021 +0000

    Initial commit
```
You can see that a new commit has been created, which reverts back to the previous version of your code.

**Tips and Variations**
-------------------------

* You can also use `git revert -n` to revert back to a previous commit without creating a new commit.
* You can use `git revert` with a range of commits, such as `git revert HEAD~2..HEAD`, to revert back to a previous range of commits.

By using `git revert`, you can easily revert back to a previous version of your code, which can be useful for fixing mistakes or going back to a previous working version of your code.
