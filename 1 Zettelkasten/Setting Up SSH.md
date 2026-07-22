The process involves three main pieces: generating an SSH key pair on your laptop, copying the public key to your server, and optionally hardening the server config. Let me show you the flow first:
![[ssh_setup_flow.png]]

---

#### Step 1 — Generate a key pair on your Arch laptop

```bash
ssh-keygen -t ed25519 -C "arch-laptop"
```

Accept the default path (`~/.ssh/id_ed25519`) and set a passphrase (recommended). Ed25519 is faster and more secure than the old RSA default.

---

#### Step 2 — Copy your public key to the server

If the server already has SSH running and you can log in with a password:

```bash
ssh-copy-id user@<server-ip>
```

That appends your public key to `~/.ssh/authorized_keys` on the server automatically. If `ssh-copy-id` isn't available, do it manually:

```bash
cat ~/.ssh/id_ed25519.pub | ssh user@<server-ip> "mkdir -p ~/.ssh && cat >> ~/.ssh/authorized_keys && chmod 600 ~/.ssh/authorized_keys"
```

---

#### Step 3 — Test the connection

```bash
ssh user@<server-ip>
```

It should log you in without asking for a password (only your key's passphrase if you set one).

---

#### Step 4 — Make it convenient with `~/.ssh/config`

```
Host homeserver
    HostName 192.168.1.x
    User your-username
    IdentityFile ~/.ssh/id_ed25519
```

Now you can just do `ssh homeserver`.

---

#### Step 5 (optional but recommended) — Harden the server

On the server, edit `/etc/ssh/sshd_config`:

```
PasswordAuthentication no
PermitRootLogin no
```

Then restart sshd:

```bash
sudo systemctl restart sshd
```

## Links: 

[[2026-01-01]]

2026010146