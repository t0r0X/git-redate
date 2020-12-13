# git-redate
### Made by [Potato Labs](http://taterlabs.com) and [eXtronis](https://extronis.com)

Interactively change the dates of several git commits in current branch with a single command. Improved and updated fork.

![alt tag](https://i.stack.imgur.com/yE4cQ.gif)

# Installation

When using Linux/BSD/Unix or macOS: you can clone this repo or download the `git-redate` file and copy it into any folders in your $PATH. Restart your terminal afterwards and you're good to go!

If you're using Homebrew please note that the available version (1.0.2) is outdated.

For Windows users: you copy the `git-redate` file into `${INSTALLATION_PATH}\mingw64\libexec\git-core\`. If you used the default Git installation settings, `INSTALLATION_PATH` should be `C:\Program Files\Git`.

See also this Stackoverflow answer: https://stackoverflow.com/a/40095055/265954.

# Usage

**Make sure to run this on a clean working directory otherwise you'll lose your uncommitted changes, or it won't work.**

* Redate a number of commits: `git redate [--commits|-c <number of commits>]`. If the redated commits have been previously pushed to a Git server, you'll have to force push in order for your commit history to be rewritten on the Git server.
The `--commits` (short `-c`) argument is optional, and defaults to 5 if not provided. \
Examples: \
`git redate` : last 5 commits (default) of current branch\
`git redate -c 7`: last 7 commits of current branch\
`git redate --commits 25` : last 25 commits of current branch
* Redate all commits of current branch at once: `git redate --all|-a`.\
Examples: \
`git redate -a` : all commits of current branch\
`git redate --all` : all commits of current branch
* Specify block size ("chunks") of commits to process: `--limit | -l <block size>`.
* Enable debug output: `--debug | -d`.

## CLI arguments
```
Parameters:
  -a| --all       Process all commits. Use this if number of commits is 1 or -c would reach to first commit.
  -c| --commits N Process last N commits, default=5.
  -d| --debug     Enable debug output.
  -h| --help      Show this help message.
  -v| --version   Show the version (v1.0.4) of git-redate
  -l| --limit N   Process commits in chunks/batches of size N, default=20.
```
