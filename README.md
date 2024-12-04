# Git Assignment 2

# Create a New Directory and Initialize as a Git Repository:

 - mkdir git-assignment-2
 - cd git-assignment-2
 - git init
 - Add a README.md File:

 - echo "# Git Assignment 2" > README.md
 - Make an Initial Commit:

 - git add README.md
 - git commit -m "Initial commit: Added README.md"
 - Push to Remote Repository: Create a new repository on GitHub (e.g., git-assignment-2). Follow the instructions provided for pushing an existing repository.

 - git remote add origin <remote_repository_url>
 - git branch -M main
 - git push -u origin main

# Create and Switch to Feature-1 Branch:
 - git checkout -b feature-1
 - Make Changes on Feature-1: Add or modify files. Example:

 - echo "Feature 1 content" > feature1.txt
 - git add feature1.txt
 - git commit -m "Feature-1: Added feature1.txt"

# Switch Back to Main and Create Feature-2 Branch:
 - git checkout main
 - git checkout -b feature-2

# Make Changes on Feature-2:
 - echo "Feature 2 content" > feature2.txt
 - git add feature2.txt
 - git commit -m "Feature-2: Added feature2.txt"

# Push Both Feature Branches to Remote:
 - git push origin feature-1
 - git push origin feature-2

# Create Pull Requests (PRs):
Go to the repository on GitHub.
Create PRs for feature-1 and feature-2 to merge into main.
Review and Update Feature Branches: Before merging, update the branches:

 - git checkout feature-1
 - git fetch origin
 - git rebase main
 - git push --force

 - git checkout feature-2
 - git fetch origin
 - git rebase main
 - git push --force

# Merge Pull Requests:
On GitHub, merge feature-1 PR into main.
Update feature-2 with the latest changes from main:

 - git checkout feature-2
 - git pull origin main
 - git push

Merge feature-2 PR into main.
Check Commit History: Verify the commit history is linear:

git log --oneline --graph --all
Delete Merged Branches Locally and Remotely:

 - git branch -d feature-1
 - git branch -d feature-2
 - git push origin --delete feature-1
 - git push origin --delete feature-2
 
 - git add README.md
 - git commit -m "Added commands used to README.md"
 - git push origin main

