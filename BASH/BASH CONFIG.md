---
title: "Bashrc Config"
description: "A copy of ~/.bashrc with some configurations ans Aliases"
created: 02-11-2022
tags:
- Config
- Bash
---
## LINKS TO COURSES AND TUTORIALS
- [Starship](https://starship.rs/)
- [Oh My Zsh](https://ohmyz.sh/)
## PROGRAMS TO INSTALL
- `exa` - `sudo apt-get install exa`
- `neofetch` - `sudo apt-get install neofetch`
- `oh-my-zsh` and `starship` 
- `shellcheck` - `sudo apt install shellcheck` [Shellcheck](https://github.com/koalaman/shellcheck#from-your-terminal)
- `whiptail` - 


***
## INSTALL AND CONFIG ZSH
- `sudo apt-get update`
- `sudo apt-get install zsh`
- `zsh`
- `touch ~/.zshrc`
#### INSTALL OH-MY-ZSH
```bash
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
- `nvim .zshrc`  - mdify to add themes and plugins
- exit zsh and enter again (for plugins and themes to take effect)
#### PLUGINS 
 (autosuggestions)
- `cd ~/.oh-my-zsh/custom/plugins`
- `git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions`
- add  `zsh-autosuggestions`  to `~/.zshrc` inside `plugins=()`

(zsh-syntax-highlighting)
- `git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting`
- add `zsh-syntax-highlighting` to `~/.zshrc` inside `plugins=()`
***
## INSTALL AND CONFIG STARSHIP
- `curl -sS https://starship.rs/install.sh | sh` - This is for Linux (Check others systems in the Url). 
- `eval "$(starship init zsh)"` - Add the following to the end of `~/.zshrc`
- To [`pastel powerline`](https://starship.rs/es-es/presets/pastel-powerline.html): 
    - `mkdir -p ~/.config && touch ~/.config/starship.toml`
    - `starship preset pastel-powerline > ~/.config/starship.toml
***

## ~/.BASHRC (sample)
- Copy this config at the end of any ~/.bashrc 
``` bash title="~/.bashrc"
# aliases (definidos por mi)
		
alias mm="rclone mount --allow-other --allow-non-empty --daemon gdrive:/home/antjrobles/gdrive/"
alias upd="sudo apt update && sudo apt dist-upgrade"
alias mem10="ps auxf | sort -nr -k 4 | head -10"
alias cpu10="ps auxf | sort -nr -k 3 | head -10"
alias freeswap="swapoff -a && swapon -a"
alias dc="docker-compose down && docker-compose up -d"
alias ll="ls"
alias nn="sudo nano docker-compose.yml"
alias vv="sudo nvim"
alias i="sudo apt-get install "
alias ..="cd .."  
alias gs="git status"
alias ga="git add ."
alias gca="git commit -m \" added\""
alias gp="git push"  
# EXA aliases
alias ls='exa --icons --group-directories-first'
alias ll='exa -lg --icons --group-directories-first --time-style long-iso'
alias la='exa -lag --icons --group-directories-first --time-style long-iso'

# First neofetch must be installed
neofetch

# Open OhMyZsh!!
zsh

# Starship 
eval "$(starship init zsh)"
```
