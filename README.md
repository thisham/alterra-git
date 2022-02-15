<center>
<h1>Getting Started on GIT</h1>
<span>Submission for task 1, Git by Alterra</span>
</center>

<br />
GIT is software for tracking changes in any set of files, usually used for coordinating work among programmers collaboratively developing source code during software development. Its goals include speed, data integrity, and support for distributed, non-linear workflows (thousands of parallel branches running on different systems). 

src: [Wikipedia](https://en.wikipedia.org/wiki/Git)

## Getting Started on GIT
### Installation
You can download on [git-scm download page](https://git-scm.com/downloads).

## Basic Operations
### Starting a GIT Repository
#### Initialize a New
This command can be used to initialize a new Git repository from a local. So that, it can be directly used from local device.
```bash
$ git init
```

#### Clone from Remotes
This command will copy from remote repository to the local. So that, it doesn't need to initialize git anymore in local.
```bash
$ git clone <remote-repository-url>
```

### Saving Changes
#### Deliver to the Staging
There a simple way to add the files to the staging stage of a branch.
```bash
# If you want to add all files to the staging stage
$ git add .

# If you want to add a file to the staging stage
$ git add <filename.ext>

# If you want to add some files to the staging stage
$ git add <filename-1.ext> <filename-2.ext> <filename-n.ext>
```

#### Commiting the Changes
If the file are ready to be commited (aka. saved to the branch), there a command to make them commited.
```bash
$ git commit -m "drop your descriptive commit message here"
```

#### Stashing Your Changes
Sometimes, we need to fix something to the other branch from our local. But, if we switch directly to the target branch, it will be conflicted with the files on target branch. So, we need to stash the edited file in order to prevent unnecessary conflict when switching to the other branch in local.

Before to do it you must to add your edited files to the staging stage. Git will recognize what's will be added to the stash.

```bash
# Add your work to the stash with stash name
$ git stash push -m "drop your stash name here"

# Apply your stash to the workspace again
$ git stash apply "stash name that will be applied"

# ... or you can pop the stash to the workspace.
# When you choose this method, the called stash will be deleted 
$ git stash apply "stash name that will be applied"
```

#### Show Commits Differences
When it's all completed, sometimes we need to track the differences between two commits or two branches. We can use these:

```bash
# Get differences between two commits
$ git diff <commit-tag-1> <commit-tag-2>

# Get differences between two branches
$ git diff <branch-name-1> <branch-name-2>
```
