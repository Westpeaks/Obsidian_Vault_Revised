## First Steps in the Bootstrap Process

### Mount Drive

- Follow the steps laid out here:
  [[Mount an External Drive in the Linux Terminal]]
- Once the drive is mounted, copy the files from the drive into your home directory.

### Copy Drive Contents

- Create a directory in your home directory called `bootstrap`. Copy the contents of the external drive to the bootstrap. 
   
   - This will located at `/var/home/wpeak` in an immutable fedora distro.
   - Run the following command:
     ```bash
	     rsync -av --progress /mnt/external/. ~/bootstrap/
     ```
    - rsync should be preinstalled on the distro so you should be able to run the command without issue.   

### Run Initial Script

- Once the files are copied, run the `fedora` script to install the necessary dependencies via rpm ostree (nvim, kitty, and tmux).
- You can run the using the command `./fedora`.

### Reboot 

- This will install some initial dependencies. Because of the way that rpm ostree works you will need to reboot for the dependencies to take place via `sudo reboot`. 
- For more information on rpm ostree, check the links section. 
## Links:

[[Immutable OS Process Index]]

[Ostree and rpm-ostree](https://docs.fedoraproject.org/en-US/atomic-desktops/technical-information/)

20260227