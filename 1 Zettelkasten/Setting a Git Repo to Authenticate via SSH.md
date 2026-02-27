## Background 

- You may run into issues when trying to run the following command to push changes for the first time in local repo. 
  `git push origin main`
- It seems that Git no longer allows local authentication with access tokens so SSH is the best choice for this task.

## Solution

- If you have not set up an SSH key:
  ```bash
	  ssh-keygen -t ed25519 -C "your_email@example.com"
	  cat ~/.ssh/id_ed25519.pub  # Copy public key
  ```
  - Once you have copied the public key, you can then update this in GitHub under the SSH key section in your settings
  - If you already have an SSH configured, you can run the following command to authenticate via SSH:
    
    `git remote set-url origin git@github.com:{Your GitHub URL}`

After these steps, you should be able to push your changes via `git push origin main`.

## Links:

[[GitHub]]

[[Git Basics]]

2025123101