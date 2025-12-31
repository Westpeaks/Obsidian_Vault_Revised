
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

## Links:

[[Pulling a Repository from GitHub to a Local Destination]]

[[Pushing Local Changes Back to a GitHub Repository]]

[[Changing a GitHub Master Branch to Main]]
 

2025111243