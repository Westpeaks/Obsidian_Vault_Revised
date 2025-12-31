## Push your changes:

1. **Stage your changes:**

```bash
git add .
```

(Or `git add filename` for specific files)

2. **Commit your changes:**
```bash
git commit -m "Your commit message"
```

3. **Push to GitHub:**
```bash
git push origin main
```

(Replace `main` with your branch name if different)

## Quick Reference

**Basic workflow:**

- `git add .` - Stage all changes
- `git commit -m "message"` - Commit with a message
- `git push origin main` - Push to remote branch

## One-liner for quick updates:
```bash
git add . && git commit -m "Update" && git push origin main
```
## Common scenarios:

**First push to a new repo:**
```bash
git push -u origin main
```

**Force push (overwrites remote - use carefully!):**
```bash
git push -f origin main
```

**Check what will be pushed:**
```bash
git status
```

# Links

#git 