# ![#f03c15](https://via.placeholder.com/15/f03c15/000000?text=+)Git Practice!

This document explains the common process and steps while working with  **Git**. This is not a universal standard and many of the readers may not agree with the suggested approach but this is what I have learned through hard way.

### ![#FFFF00](https://via.placeholder.com/15/FFFF00/000000?text=+)Open Git Repository
[vkg-mca/GitPractice (github.com)](https://github.com/vkg-mca/GitPractice)

### ![#FFFF00](https://via.placeholder.com/15/FFFF00/000000?text=+)Feature Branch Creation
Lets assume you are working on changing the format of a document so want to create the feature *change document fomatting* from the **master** or base branch

Feature branch name format : `f/EPIC-JIRA-feature-name-slug`
Where

	 - f: is feature branch name indicator (this can be used as a rule for advanced CI/CD features
	 - EPIC: This is the EPIC name (if available)
	 - JIRA: This is the Jira task number
	 - feature-name-slug: slugified feature name
 - [ ] Open [URL Slug Generator](https://slugify.online/) and create the branch name slug
 change document formatting => change-document-formatting
 - [ ] Go to repository and create feature branch from base branch 
 Example: f/UEI-106-change-document-formatting
 Where UEI is the EPIC User Experience Inhancement
 
### ![#FFFF00](https://via.placeholder.com/15/FFFF00/000000?text=+)Pulling the code
 - [ ] Open Git Bash CLI and navigate to the application folder `cd /x/gitpractice`
 - [ ] Initialize the git repository `git clone https://github.com/vkg-mca/GitPractice`
 - [ ] Checkout the feature branch `git checkout f/UEI-106-change-document-formatting` or `git switch f/UEI-106-change-document-formatting`
 
### ![#FFFF00](https://via.placeholder.com/15/FFFF00/000000?text=+)Working with Code

#### ![#1589F0](https://via.placeholder.com/15/1589F0/000000?text=+)Adding a new file
 - [ ] Add a file to the local folder `MardownFormattingTemplate.md` and add the code needed
 - [ ] Add files to the working directory `git add .`
 - [ ] Check status of the work with `git status` command
 - [ ] Commit the code to local repository which is also called staging the changes `git commit -m "added inital formatting template"`
 - [ ] Optional: Check the git history `git log --oneline --graph`
 - [ ] Optional: Check git status `git status`
 - [ ] Optional: Check git log`git log`
 - [ ] Rebase:  switch to base branch `git switch master` 
 - [ ] Rebase:  Pull the master changes `git pull master` 
 - [ ] Rebase:  reabse the branch `git rebase master` 
 - [ ] Rebase:  Resolve if there is any conflict 
 - [ ] Push the changes to remote repository `git push f/UEI-106-change-document-formatting`
 
 #### ![#1589F0](https://via.placeholder.com/15/1589F0/000000?text=+)Updating a file
 - [ ] Edit `MardownFormattingTemplate.md` by adding some other information
 - [ ] Optional: Check git status `git status`
 - [ ] Amend the changes `git commit --amend`
 - [ ] Rebase:  switch to base branch `git switch master` 
 - [ ] Rebase:  Pull the master changes `git pull master` 
 - [ ] Rebase:  reabse the branch `git rebase master` 
 - [ ] Rebase:  Resolve if there is any conflict
 - [ ] Push the changes forcefully to the remote branch
 - [ ] Push the changes to remote repository `git push -f f/UEI-106-change-document-formatting`
