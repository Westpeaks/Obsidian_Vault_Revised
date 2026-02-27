Because I am running Omarchy, my kernel will auto update with Omarchy updates. 

- The rebuild is simple and requires the following steps:  
  ```bash
  cd ~/snd_hda_macbookpro 
  sudo ./install.cirrus.driver.sh
  ```
- After it finishes, reboot and run a speaker test to confirm:
  ```bash
  sudo reboot
  ```
  ```bash
  speaker-test -c 2
  ```
  
## Links:

[[2026-01-19]]

2026011927