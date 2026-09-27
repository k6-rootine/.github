# Getting Started with Rootine

## 1. Install Git

If you don't have Git yet, [install it here](https://git-scm.com/)!

Then tell Git who you are. You only need to do this once per computer:

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

> [!TIP]
> Use the same email address as your GitHub account so your commits are linked to your profile.

## 2. Set up your workspace

Create a folder to hold all the repositories you'll clone, then open a terminal in it.

```bash
mkdir k6-rootine
cd k6-rootine
```

## 3. Clone the repositories

First, clone the main project into that folder:

```bash
git clone https://github.com/k6-rootine/rootine.git
```

Next, clone the documentation into the same folder:

```bash
git clone https://github.com/k6-rootine/docs.git
```

Your folder should now look like this:

```
k6-rootine/
├── rootine/
└── docs/
```

> [!IMPORTANT]
> **Don't generate documentation from inside the `docs` folder.** Go to the main project folder (`rootine`) and run the command described in the documentation from there.

## 4. Everyday workflow

### Get the latest changes

Before you start working, always download your teammates' latest changes:

```bash
cd rootine
git pull
```

### Check what you've changed

```bash
git status      # lists modified, new, and deleted files
git diff        # shows exactly what changed inside the files
```

### Save your changes (commit)

Stage the files you want to include, then commit them with a clear message:

```bash
git add file1.pas file2.pas   # add specific files
# or
git add .                     # add every change in the current folder

git commit -m "Adding something very important"
```

> [!TIP]
> Write short, descriptive commit messages that say *what* you did, like "Fix crash when tree is empty" instead of "fix" or "update".

### Upload your changes (push)

```bash
git push
```

If Git rejects the push because the remote has new changes, pull first, then push again:

```bash
git pull
git push
```

## 5. Resolving merge conflicts

If two people edited the same lines, `git pull` will report a **conflict**. Git marks the affected sections in the file like this:

```
<<<<<<< HEAD
your version
=======
their version
>>>>>>> origin/main
```

Edit the file to keep the correct version, delete the markers, then:

```bash
git add the-file.pas
git commit
git push
```

## 📋 Quick reference

| Command | What it does |
|---|---|
| `git clone <url>` | Download a repository |
| `git pull` | Get the latest changes |
| `git status` | See what's changed |
| `git add <file>` | Stage a file for commit |
| `git commit -m "msg"` | Save staged changes locally |
| `git push` | Upload your commits to GitHub |
| `git checkout -b <name>` | Create and switch to a new branch |
| `git log --oneline` | View the commit history |

Happy coding! 