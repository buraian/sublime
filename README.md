# Sublime Text 3 Settings Sync

## Important Files

### The Settings Git Folder
```
~/.config/sublime
```

### Sublime Text 3 Settings Folder
```
~/Library/Application Support/Sublime Text 3/Packages/User
```

### The Symbolic Link
```
~/Library/Application Support/Sublime Text 3/Packages/User -> ~/.config/sublime/User
```

## Tasks

- [Setup Git Repo For Sync](#setup-git-repo-for-sync)
- [Export Plugin List](#export-plugin-list)
- [Install Plugins](#install-plugins)

### Setup Git Repo For Sync

Install Sublime Text 3.

Move settings folder for Git sync

```shell
$ mkdir -p ~/.config/sublime/User
$ mv -v ~/Library/Application\ Support/Sublime\ Text\ 3/Packages/User ~/.config/sublime/User
```

Create Symlink

```shell
$ ln -s ~/.config/sublime/User ~/Library/Application\ Support/Sublime\ Text\ 3/Packages/User
```

Setup Git Repo

```shell
$ cd ~/.config/sublime
$ git remote add origin https://github.com/buraian/sublime.git
```

Pull from remote and overwrite any local files.

### Export Plugin List

```shell
$ code --list-extensions > extensions.list
```

### Install Plugins

```shell
$ cat extensions.list | xargs -L 1 code --install-extension
```

[Note: Make sure `code` is available to `PATH`.](https://code.visualstudio.com/docs/setup/mac#_launching-from-the-command-line)
