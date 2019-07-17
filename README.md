# git_colors
Add colored branches on your terminal

1. Locate your .bashrc
```bash
# Yes I use nano...
nano ~/.bashrc 
```
2. Between the lines:
```bash
if [ "$color_prompt" = yes ]; then
    PS1='${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w\[\033[00m\]\$ '
     # INSERT HERE <----------------------------------------------------------
else
    PS1='${debian_chroot:+($debian_chroot)}\u@\h:\w\$ '
fi
```
3. Insert this.
 
 ```bash
  export GIT_PS1_SHOWDIRTYSTATE=1 GIT_PS1_SHOWSTASHSTATE=1 GIT_PS1_SHOWUNTRACKEDFILES=1
  export GIT_PS1_SHOWUPSTREAM=verbose GIT_PS1_DESCRIBE_STYLE=branch
  GIT_PS1_SHOWCOLORHINTS=1
  PROMPT_COMMAND='__git_ps1 "${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w" "\[\033[00m\]\$ "'
 ```
4. Save and source your bashrc.
```bash
source ~/.bashrc
```

5. Try it out
