# ⚙️ Essential Git Configurations

---

### ✅ config user_name and email, this is required to identify the author of commits.
```bash
# Applies to all repositories for the given user
git config --global user.name 'your_user_name'
git config --global user.email 'your_email@gmail.com'
# If you prefer to config only for particular repo only, remove --global
```

---

### ✅ Check all git configurations set up currently
```bash
git config --list
```

### ✅ Setup Git aliases
```bash
# Show concise commit history, the one i use frequently
git config --global alias.lg "log --oneline --graph --decorate --all"
git lg # Now use like this
```

### ❌ Remove already set configurations
```bash
# In case required to remove the user.name or user.email, or any other configuration
git config --global --unset user.name
git config --global --unset user.email
```

> We can directly edit the config file as well
```bash
# Change these two files directly if required
~/.gitconfig # (Global config file)
.git/config  # (config file within current repo)
```