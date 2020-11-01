# GIT CHEATSHEET

## Logs

git log --oneline

## Rebase

### Combine N commits
git rebase -i HEAD~N

N is the total number of commits you want to combine

This will bring up your text editor (-i is for "interactive") with a file that looks like this:

```shell
pick 16b5fcc Code in, tests not passing
pick c964dea Getting closer
pick 06cf8ee Something changed
pick 396b4a3 Tests pass
```

Change all the pick to squash (or s) except the one in which you want to use as the message for the combined commit:

```shell
pick 16b5fcc Code in, tests not passing
squash c964dea Getting closer
squash 06cf8ee Something changed
squash 396b4a3 Tests pass
```