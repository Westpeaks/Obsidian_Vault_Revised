## The Basics

- Kubernetes is a program that manages and runs other programs to make sure they never stop running. 
- It watches the programs, making sure that if they crash, a new one is started in its place. 
- The is accomplished through containerized instances of applications. If a container crashes, then a new instance of that container is started back up and the data is maintained (as long as storage is configured and allocated properly).  

It is important to note that all resources will share the same pool of compute

## Structure

- **Namespaces** — logical dividers within a cluster. You might put your media server in one namespace, a database in another, and a web app in a third, keeping things organized and preventing name collisions.
- **Resource limits** — you can cap how much CPU/memory each app is allowed to use, so one greedy app doesn't starve the others.
- **Independent scaling** — each app can be scaled up or down on its own. Your website might run 3 copies while your background job runner only needs 1.
- **Independent deployments** — updating one app doesn't require touching the others. You can roll out a new version of just that one piece.

This structure makes a more lightweight and elegant management system than the traditional structure of running programs within a stack of VM's or bare metal services. 

## Links:

[[Kubernetes Common Commands]]

20260722