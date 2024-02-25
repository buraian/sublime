# Sublime Text Settings Sync

## Important Files

### The Settings Git Folder
```
~/.config/sublime
```

### Sublime Text Settings Folder
```
~/Library/Application Support/Sublime Text/Packages/User
```

### The Symbolic Link
```
~/Library/Application Support/Sublime Text/Packages/User -> ~/.config/sublime/User
```

## Tasks

- [Setup Git Repo For Sync](#setup-git-repo-for-sync)

### Setup Git Repo For Sync

Install Sublime Text.

Move settings folder for Git sync

```shell
$ mkdir -p ~/.config/sublime/User
$ mv -v ~/Library/Application\ Support/Sublime\ Text/Packages/User ~/.config/sublime/User
```

Create Symlink

```shell
$ ln -s ~/.config/sublime/User ~/Library/Application\ Support/Sublime\ Text/Packages/User
```

Setup Git Repo

```shell
$ cd ~/.config/sublime
$ git remote add origin https://github.com/buraian/sublime.git
```

Pull from remote and overwrite any local files.
