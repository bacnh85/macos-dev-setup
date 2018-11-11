# Introduction

This is based on MacOs Mojave 

# Steps

1. Install homebrew

```
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```


2. Install needed packages

```

$ brew install coreutils diffutils findutils gawk gnu-getopt gnu-tar grep wget quilt xz

```

Config .bash_config as below:

```
PATH="/usr/local/opt/coreutils/libexec/gnubin:$PATH"
PATH="/usr/local/opt/gnu-getopt/bin:$PATH"


. /Applications/Xcode.app/Contents/Developer/usr/share/git-core/git-completion.bash
. /Applications/Xcode.app/Contents/Developer/usr/share/git-core/git-prompt.sh

export GIT_PS1_SHOWDIRTYSTATE=1
export GIT_PS1_SHOWSTASHSTATE=1
export GIT_PS1_SHOWCOLORHINTS=1
#export GIT_PS1_SHOWUNTRACKEDFILES=1
export GIT_PS1_SHOWUPSTREAM="auto"

# Watch the escapes for " in the following
export PROMPT_COMMAND="${PROMPT_COMMAND:+$PROMPT_COMMAND;} __git_ps1 \"\[\033[0;33m\]\u@\h \[\033[1;34m\]\w\[\033[0m\]\" \"\[\033[1;34m\] \$\[\033[0m\] \""

```
