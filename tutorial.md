# What I Learned from the LinkedIn Learning Git and GitHub Course

**Course**: Learning Git and GitHub
**Instructor**: Ray Villalobos
**Platform**: LinkedIn Learning

---

## Introduction

I completed the LinkedIn Learning course *Learning Git and GitHub* by Ray Villalobos. The course opened with an analogy that immediately made sense to me: Git is like a time machine for your project. Just like a time machine lets you travel back through history and even change it, Git lets you document and alter a project's history. That framing helped me understand the purpose of Git before touching a single command.

---

## What Git Actually Is

Before this course, I had heard of Git but did not fully understand what it did. I learned that Git is a **version control system** — a tool that tracks every change you make to your files over time. This means you can always go back to an earlier version of your work, see exactly what changed, and understand why. It is an essential skill for anyone working on code, and I can already see how useful it would be for managing data analysis projects and scripts.

---

## Setting Up Git

The first practical thing I learned was how to configure Git with my identity. Because Git is designed for teams, every change (called a commit) needs to be linked to a person. I ran these two commands to set that up:

```bash
git config --global user.name "James Tampanga"
git config --global user.email "jamestampanga@gmail.com.com"
```

I also learned how to turn any folder on my computer into a Git repository using:

```bash
git init
```

This creates a hidden `.git` folder that stores all of Git's tracking data in the background.

---

## The Core Workflow: Edit, Stage, Commit

The most important concept I took away was the three-stage workflow that Git uses:

1. **Working Directory** — where I make changes to my files
2. **Staging Area** — where I select which changes to include in the next save
3. **Repository** — the permanent record of saved snapshots

The staging area was new to me. I initially thought you just saved changes directly, but staging lets you be deliberate; you can change five files but only commit two of them if that is what makes logical sense.

The commands I use to move through these stages are:

```bash
git add filename.md            # stage a file
git commit -m "Add bio file"   # save it permanently with a message
```

I also learned that commit messages should be short (under 50 characters) and written in the imperative tense — "Add bio file" rather than "Added bio file." This keeps the project history clean and readable.

---

## Checking What Is Happening

Two commands I found myself using constantly while practising:

```bash
git status         # shows what has changed and what is staged
git log            # shows the full history of commits
git log --oneline  # shows the same history in a compact format
```

`git log --oneline` was particularly useful — being able to see the entire history of a project summarized in a few lines makes it easy to understand what has been done and when.

---

## GitHub: Taking Git Online

The course then introduced GitHub, which I learned is not the same thing as Git. Git is the local tool running on my computer; GitHub is a cloud platform that hosts Git repositories online. This means my work is backed up, shareable, and open to collaboration.

I learned how to create a repository on GitHub and link it to my local project:

```bash
git remote add origin https://github.com/JTampanga/repo-name.git
git branch -M main
git push -u origin main
```

The `git push` command was the moment everything clicked — my local commits were now live on the internet, visible on my GitHub profile.

---

## Cloning and Branching

I also learned two other important skills.

**Cloning** lets me download a complete copy of any GitHub repository, including its full history:

```bash
git clone https://github.com/JTampanga/repo-name.git
```

**Branching** lets me create a separate version of a project to experiment or build a new feature without affecting the main code:

```bash
git checkout -b new-branch
```

Branches reminded me of how I manage copies of GIS data files when testing different processing approaches — Git formalizes that habit into something clean and reversible.

---

## Pull Requests and Collaboration

The final section covered how teams use GitHub together through **pull requests**. When a developer finishes work on a branch, they open a pull request to propose merging it into the main branch. Team members can then review the changes line by line, leave comments, and either request edits or approve. Only then does the code get merged.

This was the most eye-opening part of the course. I had thought of GitHub mainly as a place to store code, but it is really a structured workflow that enforces quality and accountability across an entire team.

---

## Key Takeaways

- Git is not just a backup tool — it is a complete history of every decision made on a project
- The staging area gives me control over exactly what goes into each commit
- Commit messages are communication, not just labels — they should be clear and meaningful
- GitHub turns a local Git project into a collaborative, cloud-hosted platform
- Pull requests are how professional teams review and approve code before it goes live

Overall, this course gave me a solid foundation in Git that I feel confident building on. The time machine analogy stayed with me throughout — every `git commit` is a point in time I can always return to.
