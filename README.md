# git-cheatsheet

I find myself often looking up the same things, so this is a personnal cheatsheet for anything git.

## Colors:

Add to `~/.gitconfig`

```
[color]
  ui = auto
[color "branch"]
  current = yellow reverse
  local = yellow
  remote = green
[color "diff"]
  meta = yellow bold
  frag = magenta bold
  old = red bold
  new = green bold
[color "status"]
  added = yellow
  changed = green
  untracked = cyan
```

## Improved git log:

This creates an alias for `git lg`

```
git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit"
```

## Only add part of a file

`git add --patch filename`

With each options:

- <kbd>y</kbd> stage this hunk for the next commit
- <kbd>n</kbd> do not stage this hunk the next commit
- <kbd>q</kbd> quit; do not stage this hunk or any of the remaining ones
- <kbd>a</kbd> stage this hunk and all later hunks in the file
- <kbd>d</kbd> do not stage this hunk or any of the later hunks in the file
- <kbd>g</kbd> select a hunk to go to
- <kbd>/</kbd> search for a hunk matching the given regex
- <kbd>j</kbd> leave this hunk undecided, see next undecided hunk
- <kbd>J</kbd> leave this hunk undecided, see next hunk
- <kbd>k</kbd> leave this hunk undecided, see previous undecided hunk
- <kbd>K</kbd> leave this hunk undecided, see previous hunk
- <kbd>s</kbd> split the current hunk into smaller hunks
- <kbd>e</kbd> manually edit the current hunk
- <kbd>?</kbd> print help
