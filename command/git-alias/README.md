In Git, **aliases** are shortcuts you can create to simplify or customize Git commands. They allow you to create shorter or more intuitive commands for frequently used Git operations.

---

## **How to Set Up Git Aliases**

### **1. Set a Git Alias (Temporary for Current Session)**
You can set a temporary alias for your current session using:
```bash
git config --global alias.<alias-name> "<git-command>"
```
**Example:**
```bash
git config --global alias.co "commit -m"
```
Now, you can use `git co "Your commit message"` instead of `git commit -m "Your commit message"`.

---

### **2. Set a Git Alias Permanently**
To make the alias persistent, add it to your Git configuration file. The command above (`git config --global`) already does this by default, as it modifies your global Git config file (`~/.gitconfig`).

**Example:**
```bash
git config --global alias.st "status"
git config --global alias.br "branch"
git config --global alias.ci "commit"
git config --global alias.lg "log --oneline --graph --all --decorate"
```

Now:
- `git st` = `git status`
- `git br` = `git branch`
- `git ci` = `git commit`
- `git lg` = `git log --oneline --graph --all --decorate`

---

### **3. View All Git Aliases**
To see all the Git aliases you've set, run:  
[--get-regexp](https://github.com/seaboie/git/new/main/command/git-alias)
```bash
git config --global --get-regexp alias
```
or
```bash
git config --global --list | grep alias
```

---

### **4. Remove a Git Alias**
To remove an alias, use:
```bash
git config --global --unset alias.<alias-name>
```
**Example:**
```bash
git config --global --unset alias.co
```

---

### **5. Edit Git Aliases Directly**
You can also manually edit your Git config file (`~/.gitconfig`) to add, modify, or remove aliases. Open the file in a text editor:
```bash
nano ~/.gitconfig
```
Add or modify aliases under the `[alias]` section:
```ini
[alias]
    co = commit -m
    st = status
    br = branch
    lg = log --oneline --graph --all --decorate
```

---

## **Common Git Aliases Examples**
Here are some useful Git aliases you might want to set:

| Alias | Command | Description |
|-------|---------|-------------|
| `git st` | `git status` | Check the status of your repository |
| `git co` | `git checkout` | Switch branches |
| `git br` | `git branch` | List all branches |
| `git ci` | `git commit` | Commit changes |
| `git cm` | `git commit -m` | Commit with a message |
| `git lg` | `git log --oneline --graph --all --decorate` | View a compact log with a graph |
| `git df` | `git diff` | Show changes |
| `git ds` | `git diff --staged` | Show staged changes |
| `git aa` | `git add .` | Stage all changes |
| `git au` | `git add -u` | Stage modified and deleted files |
| `git cp` | `git cherry-pick` | Cherry-pick a commit |
| `git rb` | `git rebase` | Rebase a branch |
| `git pl` | `git pull` | Pull changes from a remote |
| `git ps` | `git push` | Push changes to a remote |

---
