# GitAdvancedCheatSheet
A Cheat Sheet of advanced command tricks and tips to make git usage a bit more fluid.

## Git components

### Treeish

The treeish is how git represents positions in its version control tree. There are several variants which can be used as treeishes

* **commit id**: `abcdef7489` Can be the actual commit id you want to checkout
* **branch label**: `branch-name`, `HEAD`, `origin/branch-name-2` Can be the name of a labeled branch or special label like `HEAD`.

## Checking out a specific file from a specific branch or commit.

```
git checkout <treeish> -- <path/to/file1> <path/to/file2> etc..
```

https://stackoverflow.com/questions/215718/reset-or-revert-a-specific-file-to-a-specific-revision-using-git
