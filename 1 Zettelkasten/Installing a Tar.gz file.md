## Steps

**1. Extract the archive**

```bash
tar -xzf filename.tar.gz
```

This creates a folder in the current directory. Navigate into it:

```bash
cd extracted-folder/
```

**2. Install — the method depends on what's inside**

**If there's a `./configure` script** (compiled from source):

```bash
./configure
make
sudo make install
```

**If there's an `install.sh` script:**

```bash
sudo bash install.sh
```

**If it's a pre-compiled binary** (just an executable file):

```bash
sudo mv the-binary /usr/local/bin/
sudo chmod +x /usr/local/bin/the-binary
```

**If it's a Python package** (has `setup.py`):

```bash
pip install .
```

**Useful flags for `tar`:**

- `-x` — extract
- `-z` — handle `.gz` compression
- `-f` — specifies the filename
- `-v` — verbose (shows files as they extract)

If you're not sure what's inside before extracting, you can peek first:

```bash
tar -tzf filename.tar.gz
```