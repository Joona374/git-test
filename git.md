## Git Version
```
git -v
```

## Getting Help

Three ways to open the manual page for any Git command:
```
git help <command>
git <command> --help
man git-<command>
```

## Configuring Git Username, Email, and Editor

Locally (stored in the repository at ./git/config):
```
git config user.name "Your Name"
git config user.email "your@email.com"
git config core.editor "your editor"
```

## Globally (stored in your home directory at ~/.gitconfig):
```
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
git config --global core.editor "your editor"
```

You can also set these system-wide with the --system flag.

## Set Default Branch Name to main
```
git config --global init.defaultBranch main
```

## Show Config Settings
```
git config --list
git config --list --show-origin
```

## Initialize a Git Repository
```
git init
```

## Staging Changed Files
```
git add <file-name>
```

### Or stage all files:
```
git add .
```

## Checking File Status
```
git status
```

## Short output:
```
git status -s
git status --short
```

## Show Unstaged Changes
```
git diff
```

## Show Staged Changes for Next Commit
```
git diff --staged
git diff --cached
```

## Committing Changes
```
git commit
```

This command will open the selected text editor, which contains the commented result of the work of the ```git status``` and another empty line from above. You can delete these comments and dial your message or leave them to reminder that you are fixing.
For an even more detailed reminder, you can get the argument ```-v``` in the command```git comit```, which will lead to the comment to the Delta/DIFF changes and you can definitely see all the changes that have been made.

## Include diff in the commit editor:
```
git commit -v
```

## Or commit with an inline message:
```
git commit -m "Fix benchmarks for speed"
```

Each time a commit is created, a picture of the snapshot of the entire project is created, which you can recover later or with which you can compare the current state.
