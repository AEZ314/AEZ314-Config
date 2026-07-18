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
print "tldr > better man page"
print "j > simple journal"
print

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

```