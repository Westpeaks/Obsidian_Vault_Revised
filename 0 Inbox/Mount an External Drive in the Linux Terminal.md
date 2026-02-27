Here are the steps to mount an external drive in Linux:

**1. Find the drive**

bash

```bash
lsblk
```

or

bash

```bash
sudo fdisk -l
```

Look for your drive (e.g., `/dev/sdb1`).

**2. Create a mount point**

bash

```bash
sudo mkdir /mnt/external
```

**3. Mount the drive**

bash

```bash
sudo mount /dev/sdb1 /mnt/external
```


## Links:

20260225