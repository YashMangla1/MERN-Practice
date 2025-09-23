Git & Github

Concept Explanation
Repository (Repo) A project folder tracked by Git. Local vs Remote (GitHub)
Commit A snapshot of your code at a point in time
Branch Parallel version of the repo (like a feature line)
Merge Combining changes from different branches
Rebase Reapplying your commits on top of another branch (linear history)
Staging Area The “ready-to-commit” area (git add)
HEAD Pointer to current commit

1. Check git version : git —version
2. Create a new repository on Github
3. Initialise a git Repository: git init
4. Setup the git identity on your local: git config --global user.name “username“, git config --global user.email “user email”
5. Clone the repository on your local system: git clone “repo link”
6. Check the untracked changes: git status
7. Stages everything: git add .
8. Create the local commit: git commit -m “ commit message”
9. Push to Github: git push origin main

What’s the Git Pull?

1. git pull is basically two commands in one: git fetch # gets latest changes from remote , git merge # merges those changes into your current branch
2. If someone else (or another laptop) has pushed changes to the repo, pulling ensures your local copy is up-to-date: git pull origin main

main (on GitHub)
│
│ clone → work locally
│
├── create new branch
│ │
│ ▼
│ new-feature (local branch)
│ │
│ │ make changes → commit → push
│ │
│ ▼
└── merge new-feature into main
│
▼
main (local + GitHub updated)

Branches in Git

1. Check current Branch: git branch
2. Create a new feature branch: git checkout -b branch-name
3. Stages everything: git add .
4. Create the local commit: git commit -m “ commit message”
5. Push to Github: git push -u origin branch-name
6. Creates a merge commit, retains all history: git checkout main, git merge feature/login
7. Rebasing: git checkout feature/login, git rebase main

8. Switch to existing feature branch: git checkout feature-branch-name
9. Merge your feature branch: git checkout main, git pull origin main, git merge feature-branch-name, git push origin main(Push updated main to remote)

Troubleshooting Commands

1. Check last 5 commits: git log —oneline -5
2. Check remotes : git remote -v shows all the remote repos linked to your local repo
3. Abort a rebase: git rebase —abort Cancels an ongoing rebase, we’ll use when we started a rebase and got conflicts and feel stuck.
4. If Push rejected because git has new commits: git pull —rebase origin main if git push is rejected because someone else pushed commits to main. This command moves your local commits on top of latest commits from the remote branch.
5. Show Changes: git diff
6. See Commit History: git log

Undo & Recovery Commands

1. Abort rebase: git rebase —abort
2. Dangerous. Reset to last commit: git reset —hard HEAD
3. Undo last commit but keep changes staged: git reset —soft HEAD~1

Remote Collaboration

1. Git remote add origin <repo_url>
2. Git push -u origin main
   Fetching & Pulling:
3. Get remote commits, don’t merge: Git fetch origin
4. fetch+merge: git pull
5. fetch+reapply local commits: git pull —rebase
   Pushing:
6. Git push origin feature/login
   Cloning:
7. Git clone <repo_url>

Github Workflows:

1. Fork & Pull request(open source): Fork repo->make branch->push->create PR->review ->merge
2. Feature branch Workflow: Branch per feature->PR for review->CI/CD runs-> merge into main
3. Github Actions: Automate Testing, deployment, or listing on push/PR

Advance Git Topics

1. Stashing Changes: Save uncommitted work temporarily: git stash, git stash pop
2. Interactive Rebase: Clean-up commits: git rebase -I HEAD~5
3. Cherry pick commits: Apply Specific commit elsewhere: git cherry-pick <commit-hash>
4. Submodules: Include another git repo inside yours: git submodule add <repo_url> path/
5. Squash commits: Merge multiple commits into one: git rebase -I HEAD~3 “mark ’s’ for squash”

Git Rebase

git rebase moves your commits to a new base commit.

- Imagine you have a branch feature that diverged from main.
- Meanwhile, main has moved ahead with new commits.
- If you rebase feature onto main, Git reapplies your commits on top of the latest main commits, creating a linear history.

Before rebase:
main: A---B---C
feature: A---X---Y

After rebase:
main: A---B---C
feature: X'---Y'

X' and Y' are rebased copies of your original commits X and Y.

- History looks clean, as if you started your work after the latest main commit.
