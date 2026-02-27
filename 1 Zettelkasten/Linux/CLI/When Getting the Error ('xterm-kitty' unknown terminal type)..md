
On the client device:

```bash
vim ~/.ssh/config
```

Add this:
```
Host *
    SetEnv TERM=xterm-256color
```

Or for a specific server:
```
Host myserver
    HostName server_ip_address
    User username
    SetEnv TERM=xterm-256color
```

## Links:

2025111409