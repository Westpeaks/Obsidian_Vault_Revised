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

## Summary of Commands

![[gitsummary.png]]


## Links:

[[Git Basics]]

[[Pulling a Repository from GitHub to a Local Destination]]

[[Pushing Local Changes Back to a GitHub Repository]]

[[Changing a GitHub Master Branch to Main]]

2025120121