# Git Branch in Your Bash Prompt

**download the `git-prmopt.sh` script and save it to your root directory:**

```
curl https://raw.githubusercontent.com/git/git/master/contrib/completion/git-prompt.sh -o ~/.git-prompt.sh
```

**Add the following to your `~/.bash-profile`**

```
# Load in the git branch prompt script.
source ~/.git-prompt.sh
```


Now add `\$(__git_ps1)` to your prompt declaration (line that starts with `PS1`).

My declaration looks like this:

**example with colors: **

`PS1="\[$BLUE\]\u\[$YELLOW\]\[$YELLOW\]\w\[\033[m\]\[$MAGENTA\]\$(__git_ps1)\[$WHITE\]\$ "`

