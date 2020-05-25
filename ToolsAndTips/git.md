# Source Control Systems
## GIT
1. GIT bash does not show branch name in ubuntu?

Ans: Append the following to bashsrc file:
```
	update_PS1 () {
	  PS1="\[\033]0;$TITLEPREFIX:${PWD//[^[:ascii:]]/?}\007\]\n\[\033[32m\]\u@\h \[\033[35m\]$MSYSTEM \[\033[33m\]\w\[\033[36m\]`__git_ps1`\[\033[0m\]\n$ "
	}
	shopt -u promptvars
	PROMPT_COMMAND=update_PS1
```