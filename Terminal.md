[Go Back](./README.md)

# Terminal

Recommended terminal of choice: `Ghostty`

> Why? There isn't really a huge difference between the default terminal and Ghostty. Ghostty just works better with terminal animations(?). Idk, it doesn't matter that much.

## Ghostty Config

```
command = /bin/zsh

shell-integration-features = no-title
macos-titlebar-style = tabs
macos-titlebar-proxy-icon = hidden
window-subtitle = false
clipboard-paste-protection = false

shell-integration-features = ssh-terminfo

background = 1e1e2e
foreground = cdd6f4
```

# Shell

Recommended terminal of choice: `zsh`

> Why? Shell choice is more important than terminal choice. Different shells come with different scripting languages, with different levels of compatibility to bash, which is the standard shell most OSs ship with. `zsh` strikes a good balance between features and compatibility, can be customized, and has good eco-system.

## `~/.zshrc`

```
export PATH="$HOME/.local/bin:$PATH"

PROMPT='%F{blue}%1~%f %(?.%F{green}.%F{red})❯%f '
precmd() {
  print -Pn "\e]2;%n@%m\a"
}

print
print "Welcome, $USER."
print "> wtf: helpful commands"
print

wtf() {
  print
  print "> cmatrix: MATRIX"
  print "> tldr <cli command>: better man page"
  print "> j <journal entry>: simple journal"
  print "> tmux -s <name>: start persisted shell session"
  print "> rg <search>: faster grep"
  print "> micro <file>: better nano"
  print
}

alias j='jrnl'

autoload -Uz compinit
compinit

zmodload zsh/complist
setopt AUTO_MENU
```

# Packages

```
# Cool matrix style screen-saver animation in terminal
cmatrix

# Better man page
tldr

# Simple journal
jrnl

# ripgrep: like grep but much faster
rg

# like nano but more convenient
micro

# Decouples shell sessions from terminal sessions
tmux
```
