# Git

## Referencing branches
- `HEAD~` —  One behind HEAD
- `HEAD~~` —  Two behind HEAD
- `HEAD~3` —  Three behind HEAD

## Restore a file
Restore a file to it's version on the master branch
```
git checkout -- {file}
```

Restore a file to it's version from a specific branch
```
git checkout {branch} -- {file}
```

## Feature branch workflow
1. Rebase feature branch onto master
```
git checkout feature-branch
git rebase master
```

2. Update master with the feature branch
```
git checkout master
git merge feature-branch
```

## Undo
Add another commit undoing a previous commit
```
git revert 0ad5a7a6
```

## Branches
List all branches
```
git branch -a
```

Delete *local* branches
```
git branch -d feature/login
```

Delete *remote* branches
```
git push origin --delete feature/login
```

## Remotes
List remotes
```
git remote -v
```

## Submodules
Pull all submodules for the first time
```
git submodule update --init --recursive
```

Update all submodules
```
git submodule update --recursive --remote
```

## Git hooks
Git hooks live by default in `.git/hooks`, which is a private directory. To change the location
(e.g. to `.githooks`):
```
git config --local core.hooksPath .githooks
```
