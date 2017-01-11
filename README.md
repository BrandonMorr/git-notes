# Git Notes

### Reverting commit and pushing to remote

```
git reset --hard <commit-hash>
git push -f <remote> <branch>
```

Should tread lightly with this one.

### Git diff not showing anything

```
git diff --staged --color
```

### Broke something and need to use git's magic time machine

```
git reflog
git reset HEAD@{index}
```

Reflog will show you all actions performed in git, use the corresponding HEAD@{index} to go back in time.

### Change commit message or author information

```
git commit --amend
```

### Commited to the wrong branch and need to move to proper

```
git reset HEAD~ --soft
git stash
git checkout name-of-the-correct-branch
git stash pop
git add . # or add individual files
git commit -m "your message here"
```

Undo your last commit while leaving the changes available, move to correct branch. Cool!
