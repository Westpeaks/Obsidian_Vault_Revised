## Container Management

**Run containers:**

bash

```bash
podman run -d --name mycontainer nginx              # Run detached
podman run -it ubuntu bash                          # Run interactive
podman run -p 8080:80 nginx                         # Port mapping
podman run -v /host/path:/container/path nginx      # Volume mount
podman run -e VAR=value nginx                       # Environment variable
```

**Container operations:**

bash

```bash
podman ps                    # List running containers
podman ps -a                 # List all containers (including stopped)
podman start mycontainer     # Start container
podman stop mycontainer      # Stop container
podman restart mycontainer   # Restart container
podman rm mycontainer        # Remove container
podman rm -f mycontainer     # Force remove running container
```

**Interact with containers:**

bash

```bash
podman exec -it mycontainer bash        # Execute command in container
podman logs mycontainer                 # View logs
podman logs -f mycontainer              # Follow logs
podman inspect mycontainer              # Detailed container info
podman top mycontainer                  # Show running processes
```

## Image Management

**Images:**

bash

```bash
podman images                           # List images
podman pull nginx                       # Pull image from registry
podman rmi nginx                        # Remove image
podman build -t myimage:tag .           # Build from Dockerfile
podman tag myimage:tag myimage:latest   # Tag image
podman push myimage:tag                 # Push to registry
podman save -o image.tar myimage        # Export image
podman load -i image.tar                # Import image
```

**Search and inspect:**

bash

```bash
podman search nginx          # Search for images
podman inspect nginx         # Inspect image details
podman history nginx         # Show image layers
```

## Pods (Podman-specific feature)

bash

```bash
podman pod create --name mypod -p 8080:80   # Create pod
podman pod ls                                # List pods
podman pod start mypod                       # Start pod
podman pod stop mypod                        # Stop pod
podman pod rm mypod                          # Remove pod
podman run --pod mypod nginx                 # Add container to pod
```

## Networks

bash

```bash
podman network ls                           # List networks
podman network create mynetwork             # Create network
podman network inspect mynetwork            # Inspect network
podman network rm mynetwork                 # Remove network
podman run --network mynetwork nginx        # Use specific network
```

## Volumes

bash

```bash
podman volume ls                            # List volumes
podman volume create myvolume               # Create volume
podman volume inspect myvolume              # Inspect volume
podman volume rm myvolume                   # Remove volume
podman volume prune                         # Remove unused volumes
```

## System Management

bash

```bash
podman info                  # System information
podman version               # Show version
podman system df             # Show disk usage
podman system prune          # Remove unused data
podman system prune -a       # Remove all unused images
podman stats                 # Show container resource usage
```

## Podman Compose (Docker Compose alternative)

bash

```bash
podman-compose up -d         # Start services in background
podman-compose down          # Stop and remove services
podman-compose ps            # List services
podman-compose logs -f       # Follow logs
```

## Rootless vs Root

bash

```bash
# Run as regular user (rootless - default)
podman run nginx

# Run with root privileges
sudo podman run nginx

# Generate systemd service (rootless)
podman generate systemd --new --files --name mycontainer
```

## Useful Combinations

bash

```bash
# Remove all stopped containers
podman container prune

# Remove all containers (force)
podman rm -f $(podman ps -aq)

# Remove all images
podman rmi -f $(podman images -q)

# Copy files to/from container
podman cp mycontainer:/path/to/file /local/path
podman cp /local/path mycontainer:/path/to/file

# Export/Import containers
podman export mycontainer > container.tar
podman import container.tar myimage:tag
```


## Links:

2025110531