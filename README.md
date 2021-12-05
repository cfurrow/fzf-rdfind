# fzf-rdfind
Using `rdfind` to find duplicates in the current directory, use `fzf` to select files for deletion.

## Prerequisites
- Install [`rdfind`](https://rdfind.pauldreik.se/) (`brew install rdfind`)
- Install [`fzf`](https://github.com/junegunn/fzf) (`brew install fzf`)

## Install
Copy `fzf-rdfind` to a directory that is part of your PATH. I use `~/bin/` and put this in my `~/.zshrc` or `~/.bashrc` file:

```shell
export PATH=$HOME/bin:$PATH
```

Then you can run `fzf-rdfind` from any directory you'd like to find and mark duplicates for deletion. When the file list appears, you can press ENTER on any line to delete that single file, or, you can press SHIFT+TAB to add that file to a list of files you want to delete. To add more files to that list, simply find another file in the list, and press SHIFT+TAB again. Once done, press ENTER and the selected list of files will be passed to `rm` for deletion.
