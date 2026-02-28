## Mounting

1. Find the drive
   ```bash
   lsblk
   ```
2. Create a mount point
```bash
sudo mkdir /mnt/external
```

3. Mount the drive
```bash
sudo mount /dev/sdb1 /mnt/external
```

4. Verify it's mounted
```bash
df -h
```

5. Unmount when done
```bash
sudo umount /mnt/external
```
## Links:

[[Immutable OS Process Index]]

20260226