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

### Inspecting Changes
#### Logging
This will logs the changes in a branch easily.
```bash
# Get a simple logs from this branch
$ git log --oneline

# ... or you can get more details
$ git log
```

#### Reset the Changes
If you do this, you can undo the updates on your files.
```bash
# Undone your commit, and the file left staged
$ git reset <commit-tag> --soft

# Undone your commit, but changes will be destroyed
$ git reset <commit-tag> --hard
```

#### Checkout
Jump to spesific commit as branch or jump to another branch.

```bash
# Jump to spesific commit
$ git checkout <commit-tag>

# Jump to a branch, or create new if unavailable
$ git checkout -b <commit-tag>
```
