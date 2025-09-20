# Chattrix Monorepo (with Git Submodules)

This repository acts as the central hub for the **Chattrix** ecosystem.  
It integrates the following submodules:

- [`chattrix-api`](https://github.com/flourine95/chattrix-api) – Jakarta EE 11 + PostgreSQL backend  
- [`chattrix-ui`](https://github.com/flourine95/chattrix-ui) – Flutter desktop & mobile client  

---

## 🔹 Clone with submodules

```bash
git clone https://github.com/flourine95/chattrix.git
cd chattrix
git submodule update --init --recursive

```
## 🔹 Update submodules

Pull the latest commits from the remotes:

```bash
git submodule update --remote --merge

```
## 🔹 Useful commands

Show current submodule status:

```bash
git submodule status
```

Re-initialize submodules (after cloning on a new machine):

```bash
git submodule update --init --recursive
```
## 🔹 Remove a submodule

If you need to remove a submodule (e.g. `chattrix-ui`), follow these steps:

1. Delete the submodule entry from **.gitmodules**  
```bash
git config -f .gitmodules --remove-section submodule.chattrix-ui
```
2. Remove the submodule entry from git config
```bash
git config -f .git/config --remove-section submodule.chattrix-ui
```
3. Remove the submodule’s directory and metadata
```bash
git rm -f chattrix-ui
rm -rf .git/modules/chattrix-ui
```
4. Commit the changes
```bash
git commit -m "remove chattrix-ui submodule"
git push
```

