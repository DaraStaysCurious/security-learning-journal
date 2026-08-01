# Git Notes

## What is Git?

Today I learned that Git and GitHub aren't the same thing.

Git is software that runs on my computer and tracks changes to files over time.

GitHub is a website that stores copies of Git repositories, making it easy to collaborate with other people.

Before today, I didn't understand the difference between them.

---

## Commands

### pwd

Print Working Directory.

Shows me where I currently am in the filesystem.

### ls

Lists everything inside my current directory.

### cd

Changes directories.

### mkdir

Creates one or more directories (folders).

### touch

Creates empty files.

## Mental Models

### Git vs. GitHub

Git and GitHub are different tools.

Git lives on my computer and keeps track of changes to my files.

GitHub stores a copy of my Git repository online so I can back it up, collaborate with others, and access it from another computer.

---

### The Terminal Always Has a Current Location

I can think of the terminal like standing in a room.

- `pwd` tells me which room I'm standing in.
- `ls` shows me what's in the room.
- `cd` moves me to another room.

---

### Spaces Separate Arguments

The shell uses spaces to separate arguments.

When I typed:

```bash
cd /Users/darathomas/Desktop/CYBERSECURITY JOURNEY/LOCAL GIT/security-learning-journal
```

the shell thought I was giving it multiple directory names because of the spaces.

Wrapping the path in quotes tells the shell to treat it as one argument:

```bash
cd "/Users/darathomas/Desktop/CYBERSECURITY JOURNEY/LOCAL GIT/security-learning-journal"
```

---

### Untracked Doesn't Mean Unknown

When Git says a file is "untracked," it doesn't mean Git can't see it.

It means Git sees the file, but I haven't told Git that I want it included in the repository's history yet.

`git add` changes a file from untracked to staged.

---

### What `git init` Really Does

A normal folder becomes a Git repository when Git creates a hidden `.git` directory inside it.

The `.git` directory contains all of Git's history, configuration, and metadata.

The files I'm working on are not the repository.

The hidden `.git` directory is the repository.

## Still Curious About...

- Why does Git use a staging area?
- What is a commit, exactly?
- Why do commits have long hash values?
- What is the difference between fetch, pull, and clone?

## Git Workflow Practice

Today I learned how to:
- initialize a repository
- clone a repository
- stage files
- commit changes
- push changes to GitHub

## Git Branching, Merging, and Change Management

### Branches

Branches allow developers to work on changes independently without affecting the main codebase.

Common workflow:

1. Create a feature branch
2. Make changes
3. Commit changes
4. Merge approved changes into the main branch
5. Push updates to the remote repository

Example commands:

```bash
git branch feature-name
git switch feature-name
git add .
git commit -m "Describe changes"
git switch main
git merge feature-name
git push

Merge Conflicts

A merge conflict occurs when Git cannot automatically combine changes because multiple branches modified the same part of a file.

Resolving conflicts requires:

Reviewing the conflicting changes
Deciding which version should be kept
Updating the file
Committing the resolution

Merge conflicts demonstrate the importance of human review and decision-making when managing changes.

Why Git Matters in Cybersecurity

Git supports security practices by providing:

Traceability — tracking who made changes and when
Accountability — associating changes with specific contributors
Change management — reviewing and approving modifications before deployment
Version history — maintaining an audit trail of system changes

These concepts connect to cybersecurity governance, risk management, compliance frameworks, and secure software development practices.