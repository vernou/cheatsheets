# git

## config

```shell
# Set user information
git config user.name "Mona LISA"
git config --global user.email "mona.lisa@hotmail.com"

# Set proxy
git config --global http.proxy http://<url>:<port>
# Unset proxy
git config --global --unset http.proxy

# List configuration
git config --list
# List configuration with origin
git config --list --show-origin
```

## log

```shell
git log --graph --all
```

## commit

```shell
# Commit all modified/deleted files (but no new unstagged files)
git commit -a
git commit --all

# Amend commit
git commit --amend
# Keep the commit information message, author and author date (but override commiter and commiter date)
git commit --amend -C HEAD
git commit --amend --reuse-message HEAD
```

## rebase

```shell
git rebase master
```

## diff

```shell
# Compare working area to stage area
git diff
# Compare stage area to repository
git diff --staged
# Compare working area to repository
git diff HEAD
```

## reset

```shell
# Undo last commit, keep in stage area
git reset --soft HEAD~1
# Undo last commit, keep in working area
git reset --mixed HEAD~1
git reset HEAD~1 #--mixed is the default mode
# Undo last commit, lost
git reset --hard HEAD~1
```

## branch

```shell
# Open UI that display the graph of all branches
gitk --all

# Delete locally remote branches non-existent on remote repositories
git fetch --prune

# Display all branches, those with the tag [gone] they no longer exist on the remote
git branch -v
```

## remote

```shell
# Display remote with urls (fetch/push)
git remote -v
# Show remote's informations
git remote show origin
# Set url's remote
git remote set-url origin <remote_url>
```

## submodule

```shell
git submodule add https://github.com/dotnet/efcore.git submodule/efcore 
cd submodule/efcore
git checkout v3.1.32
cd ../..
git commit -m "add git submodule efcore at v3.1.32"
```
