# How to create new repo

This guide contains instructions on how to create a new GitHub repository for 'new-project' and a development branch in it, so a work on new features can be done without affecting the main branch. 

---
#### Prerequisites:
- Locally installed Git
- GitHub account
- Added SSH key or personal access token
---
#### Create a New Repository on GitHub:
- Go to GitHub.
- Click the + icon in the upper right corner and select New repository.
- Fill in the repository name with "new-project", description (optional), and choose whether it will be public or private.
- Do not initialize the repository with a README, .gitignore, or license (you can add these later if needed).
- Click Create repository.

#### Create local repo add branch and push to GitHub

- Create new dir called "new-project"
```
mkdir new-project
```
- cd to the dir
```
cd new-project
```
- Create empty git repository
```
git init
```
- Create README.md file and add some content
```
vim README.md
```
- Stage the file for commit
```
git add README.md
```
- Commit change to the repo with "init" message
```
git commit -m "init"
```
- Add remote repo
```
git remote add origin git@github.com:<github_username>/new-project.git
```
- Push local repo to the cloud
```
git push -u origin main
```
- Create and switch to development branch
```
git switch -c development
```
- Add some content to README.md
```
vim README.md
```
- Commit all changed files and push to the cloud
```
git commit -am "added more content to README.md"
git push origin development
```
- Switch to main branch
```
git switch main
```
- Merge changes from development into main
```
git merge development
```
- Push to the cloud
```
git push
```
