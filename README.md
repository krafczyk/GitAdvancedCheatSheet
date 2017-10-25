# GitAdvancedCheatSheet
A Cheat Sheet of advanced command tricks and tips to make git usage a bit more fluid.

## Git components

### Treeish

The treeish is how git represents positions in its version control tree. There are several variants which can be used as treeishes

* **commit id**: `abcdef7489` Can be the actual commit id you want to checkout
* **branch label**: `branch-name`, `HEAD`, `origin/branch-name-2` Can be the name of a labeled branch or special label like `HEAD`.

### Treeish Operators

You can combine treeishes into ranges or apply operators to move backwards in commit history from a specific commit.

* **^** The carrot operator `^` applied on the end of any treeish results in a treeish which is one commit furthur back. I.e. `HEAD^` is the commit before the current `HEAD`.
* **~** The tilde operator `~` applied on the end of any treeish with a number is the commit that number of commits furthur back from the specified commit. i.e. `HEAD^^` is equivalent to `HEAD~2`.
* **..** The double dot operator `..` between two commits creates a commit range, which is useful for some git commands.

## Checking out a specific file from a specific branch or commit.

```
git checkout <treeish> -- <path/to/file1> <path/to/file2> etc..
```

https://stackoverflow.com/questions/215718/reset-or-revert-a-specific-file-to-a-specific-revision-using-git

## Viewing a specific diff for a specific file from anywhere in git (any branch)

```
git diff <commit> <commit> -- [<path>...]
```

or

```
git diff <commit_range> -- [<path>...]
```

https://stackoverflow.com/questions/3338126/how-to-diff-the-same-file-between-two-different-commits-on-the-same-branch
