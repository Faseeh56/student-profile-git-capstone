# 🚀 Git & GitHub Capstone Project

A practical capstone project completed as the final assessment of my **Git & GitHub learning series**.

This repository brings together the Git and GitHub concepts covered throughout the series into one complete hands-on workflow, including repositories, local and remote development, pushing, cloning, branching, merging, conflict resolution, Pull Requests, undoing changes, and forks.

> **Learn → Practice → Build → Collaborate → Document**

---

## 🎯 Project Purpose

The purpose of this capstone is to demonstrate practical understanding of Git and GitHub rather than simply memorizing commands.

Throughout this project, I practiced how Git is used to:

- Track project history
- Save changes through commits
- Connect a local repository to GitHub
- Push local work to a remote repository
- Clone a remote repository
- Work with branches
- Merge changes
- Resolve merge conflicts
- Collaborate through Pull Requests
- Undo and recover from changes
- Work with forks

The goal is to finish with a public repository that acts as **proof of practice**.

---

## 🧠 Concepts Covered

### Git & GitHub Fundamentals

- Git
- GitHub
- Git vs GitHub
- Repository
- Local Repository
- Remote Repository
- `main`
- `origin`
- Commits
- Commit history
- Commit hashes

### Local → GitHub Workflow

```bash
git init
git status
git add .
git commit -m "message"
git remote add origin <REMOTE-URL>
git remote -v
git push -u origin main
````

### GitHub → Local Workflow

```bash
git clone <REPOSITORY-URL>
```

### Branching

* What branches are
* Why branches are used
* Feature branches
* Creating branches
* Switching branches
* Working separately from `main`

```bash
git branch
git branch <branch-name>
git switch <branch-name>
git switch -c <branch-name>
git switch main
```

### Collaboration

* Merge
* Merge conflicts
* Conflict resolution
* Pull Requests
* Pull Request → Review → Merge workflow

### Undo & Recovery

* Undoing staged changes after `git add .`
* Undoing the latest commit
* Reversing a specific commit using its hash

### Forks

* Forking a GitHub repository
* Cloning a fork
* Creating a feature branch
* Making changes
* Committing changes
* Pushing changes

---

# 🛠️ Capstone Workflow

This project follows a complete Git and GitHub workflow:

```text
Create Local Project
        ↓
Initialize Git
        ↓
Track & Commit Changes
        ↓
Connect GitHub Remote
        ↓
Push to GitHub
        ↓
Create Feature Branch
        ↓
Make Changes
        ↓
Commit Changes
        ↓
Push Feature Branch
        ↓
Create Pull Request
        ↓
Merge Changes
        ↓
Create & Resolve Merge Conflict
        ↓
Practice Undo / Recovery
        ↓
Fork a Repository
        ↓
Clone the Fork
        ↓
Create Feature Branch
        ↓
Make Changes
        ↓
Commit + Push
```

---

# 📁 Project Structure

```text
student-profile-git-capstone/
│
├── README.md
├── profile.txt
└── skills
      └──skills.txt
```

The project itself is intentionally simple.

The main purpose of this capstone is to demonstrate the **Git and GitHub workflow**, not to build a complex software application.

---

# 🏠 1. Create the Local Repository

The project was first created as a normal folder on the local computer.

Git was then initialized:

```bash
git init
```

This converted the folder into a **local Git repository**.

To check the repository status:

```bash
git status
```

---

# 💾 2. Stage and Commit Changes

Project files were added to Git's staging area:

```bash
git add .
```

The changes were then committed:

```bash
git commit -m "Initial project"
```

A commit can be thought of as a **checkpoint in the project's history**.

> `git add` → Prepare changes
> `git commit` → Save a checkpoint

---

# ☁️ 3. Connect the Local Repository to GitHub

A GitHub repository was created to act as the remote repository.

The local repository was connected using:

```bash
git remote add origin <REMOTE-URL>
```

The remote connection was verified using:

```bash
git remote -v
```

Here, `origin` is the conventional name given to the configured remote repository.

---

# 🚀 4. Push the Local Repository to GitHub

The local project was pushed to GitHub using:

```bash
git push -u origin main
```

The basic direction is:

```text
LOCAL → GITHUB
        PUSH
```

This demonstrated how committed local work can be published to the remote repository.

---

# 📥 5. Clone the Repository

The GitHub repository was also cloned to another local location.

```bash
git clone <REPOSITORY-URL>
```

The basic direction is:

```text
GITHUB → LOCAL
        CLONE
```

After cloning, the repository could be opened and worked with locally.

---

# 🌿 6. Create and Use Branches

A feature branch was created so that new work could be developed separately from `main`.

To see available branches:

```bash
git branch
```

A branch can be created using:

```bash
git branch feature-profile
```

To switch to the branch:

```bash
git switch feature-profile
```

Or create and switch in a single command:

```bash
git switch -c feature-profile
```

The important idea is:

> **A branch is a separate development path inside the same repository.**

Example:

```text
              main
                |
                ●
                |
          ┌─────┴─────┐
          ↓           ↓
   feature-profile  feature-bio
```

A branch is **not a completely new project**.

---

# 🔀 7. Merge Changes

After completing work on a feature branch, the changes can be brought into another branch through a merge.

The basic workflow practiced was:

```text
Feature Branch
      ↓
     Merge
      ↓
     main
```

The purpose of merging is to combine development work from different branches.

---

# ⚔️ 8. Merge Conflict Practice

A merge conflict was intentionally created by modifying the same part of a file in different development paths.

The general workflow was:

```text
Different Changes
       ↓
Attempt Merge
       ↓
Git Detects Conflict
       ↓
Open Conflicting File
       ↓
Choose the Correct Content
       ↓
Remove Conflict Markers
       ↓
Stage the File
       ↓
Complete the Merge
```

A conflict may contain markers such as:

```text
<<<<<<< HEAD
Current version
=======
Incoming version
>>>>>>> feature-branch
```

The correct final content must be selected manually.

The important lesson:

> **A merge conflict is not simply a failure. It means Git needs a human decision about which changes should remain.**

---

# 🔎 9. Pull Requests

A feature branch was also used to practice the GitHub Pull Request workflow.

The basic flow is:

```text
Feature Branch
      ↓
Push to GitHub
      ↓
Pull Request
      ↓
Review
      ↓
Merge
      ↓
main
```

A Pull Request is a way to propose changes from one branch to another through GitHub.

In this project, the feature branch was used to create a Pull Request targeting `main`.

---

# ↩️ 10. Undoing Changes

Different recovery situations were practiced because "undo" is not one single Git operation.

## A. Undo changes after `git add .`

After staging files:

```bash
git add .
```

the changes can be removed from the staging area while keeping the actual work:

```bash
git restore --staged .
```

Concept:

```text
Working Directory
       ↓
    git add .
       ↓
   Staging Area
       ↓
git restore --staged .
       ↓
Working Directory
```

---

## B. Undo the latest commit

The latest commit was also practiced using the reset workflow:

```bash
git reset --soft HEAD~1
```

This moves the repository back by one commit while keeping the changes available for further work.

---

## C. Reverse a specific commit

To inspect commit history:

```bash
git log --oneline
```

This makes it easier to identify a specific commit hash.

A specific commit can then be reversed using:

```bash
git revert <commit-hash>
```

Unlike simply deleting history, `git revert` creates a new commit that reverses the effect of the selected commit.

---

# 🍴 11. Fork Workflow

A GitHub repository was also used to practice the fork workflow.

The process was:

```text
Original Repository
        ↓
       Fork
        ↓
My GitHub Repository
        ↓
      Clone
        ↓
Local Repository
        ↓
Feature Branch
        ↓
Make Changes
        ↓
Commit + Push
```

A fork creates my own GitHub copy of another repository.

### Fork vs Branch

**Branch**

> A separate development path inside the same repository.

**Fork**

> My own GitHub copy of another repository.

---

# 🧪 12. Practical Demonstrations Completed

This capstone was designed to practice the concepts rather than simply read about them.

The following workflows were practiced:

* Created a local Git repository
* Created commits
* Connected a local repository to GitHub
* Pushed local work to GitHub
* Cloned a repository
* Created feature branches
* Switched between branches
* Merged branch changes
* Created and resolved merge conflicts
* Created and merged Pull Requests
* Undid staged changes
* Practiced undoing the latest commit
* Reversed a specific commit using its hash
* Forked a GitHub repository
* Cloned the fork
* Created a branch in the fork
* Made, committed, and pushed changes

---

# 📚 What I Learned

Through this capstone, I learned that Git is much more than a collection of commands.

I learned how to manage a project's history, work with local and remote repositories, connect projects to GitHub, create and manage branches, collaborate through Pull Requests, resolve merge conflicts, recover from mistakes, and work with forks.

Most importantly, I learned to focus on **understanding what each Git command is doing instead of blindly copying commands**.

Git became much easier to understand once I stopped looking at individual commands and started looking at the complete workflow.

---

# 💡 Key Takeaways

| Concept               | Meaning                                                                  |
| --------------------- | ------------------------------------------------------------------------ |
| **Git**               | Version control system used to track project history                     |
| **GitHub**            | Remote platform for hosting and collaborating on Git repositories        |
| **Local Repository**  | Git repository on my computer                                            |
| **Remote Repository** | Repository hosted remotely, such as on GitHub                            |
| **Commit**            | A checkpoint in project history                                          |
| **Origin**            | Name of a configured remote                                              |
| **Push**              | Local → Remote                                                           |
| **Clone**             | Remote → Local                                                           |
| **Branch**            | Separate development path inside a repository                            |
| **Merge**             | Combine changes from branches                                            |
| **Pull Request**      | Proposal to bring changes from one branch into another                   |
| **Merge Conflict**    | A situation where Git needs a human decision between conflicting changes |
| **Fork**              | My own copy of another GitHub repository                                 |

---

# 🏆 Portfolio Outcome

This repository serves as my **Git & GitHub proof of practice**.

Instead of simply saying:

> "I completed a Git & GitHub course."

this repository demonstrates the workflows I actually practiced.

It shows my ability to:

* Work with Git locally
* Use GitHub as a remote repository
* Manage branches
* Collaborate through Pull Requests
* Resolve conflicts
* Recover from mistakes
* Work with forks
* Maintain a meaningful Git history

---

# 🚀 Future Use

The Git and GitHub skills practiced here will be used throughout my future software development and AI Engineering projects.

GitHub will not simply be a place where I upload finished projects.

It will be part of my development workflow for:

* Version control
* Collaboration
* Project management
* Documentation
* Portfolio building
* Proof of work

---

# 👨‍💻 Author

**Faseeh**

Computer Science Student
Aspiring AI Engineer

---
