2024-05-17 11:48

Tags: [[Fundamentals]] [[Engineering]] [[Khazad-dûm/Tags/Git|Git]]

Git and Github are two different things. There is also Gitlab now.

## What is Git?

- Git is a software that is installed on your computer (if you have Linux or Mac). 
- Git is a memory card for code. It also controls versioning of a program. 

### Central Commands to Git

To save and control versioning with Git, you first have to initialize Git with the project (folder) that you would like to use Git with.

###### **Using** a terminal, navigate to the appropriate file path in your OS and run
`git init` 

###### **Then** you need to add what you want to save. Using git add . will save everything of you can select a specific file.
`git add *your specific file (ex. index.html)*` 
OR
`git add .` 

###### **After** you have added what you want to save, you'll need to commit that selection to memory. This you can do by using git commit. You'll also need to add -m to create a message explaining those changes. 
`git commit -m "First commit. Created files and added boilerplate HTML."`

**All** the saves can be accessed by running git log.
`git log`

**If** you would like to replace or explore a previous commit, first pull the commit ID from git log. Then, execute the command git checkout. 
`git checkout *commit ID here*`

**Previous** commits exist on separate branches than the most recent change. If you want to revert to a previous commit, that branch has to override the current existing main branch. More on that later.

# <span style="color:#ffd700">GitHub </span>

## What is GitHub?

**GitHub** is a website that is structurally the same as **Bitbucket** and **GitLab**. It allows you to upload git commits to their website and allows other users the ability to access that code.

### How do you get your code onto GitHub?

**Make** an account.

**Then**, you create a repository in GitHub and upload your project. Once the repository is created, the readme file that gets created should provide instructions to link the online repository to your local one. Also, a link to the repository is provided. The connection will be made back in your terminal. The command to make this link is:
`git remote add origin *the link from the GitHub repository*`

**Once** a connection is established, you then must push the code from your local directory to the GitHub repository. This uploads the code into your GitHub repository. 
`git push -u origin master`

### Branching

**By** default, all the code is on a master branch. A different branch is like creating a different file system that can exist on its own or be routed back into the main file system. Use git checkout to create a branch. 
`git checkout -b new-branch

You can then check out the branch using the following:
`git branch`

You can push the new branch back into the GitHub repository using:
`git push origin new-branch`

Once the new branch is in the GitHub repository, it can be merged into the master branch via a pull request in the GitHub interface.  

When GitHub has changes that you do not have on your local repository, you need to pull those changes to ensure that both your GitHub and local machine are synced. 
`git pull origin master`

### Summary

![[Screenshot 2024-05-18 at 11.54.20 PM.png]]

## References
https://www.youtube.com/watch?v=mJ-qvsxPHpY&list=PLtN8qmRCMH0i1MfuDa1DL8GJP23Ks17m7&index=39&ab_channel=NickWhite

