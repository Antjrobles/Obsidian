---
title: "Vim & NeoVim"
description: Cheatsheet for Neovim
created: 12-10-2022
tags:
- neovim
- cheatsheet
---
## INSTALLATION (Neovim)
- Para instalar vim-plug ejecuta el siguiente comando en la terminal:
```
curl -fLo ~/.local/share/nvim/site/autoload/plug.vim --create-dirs https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```
## SHORTCUTS
- Skipping To Empty Lines   `“}”` - Way better than jumping up and down using CTRL-d and CTRL-u you can jump to empty lines using “}“ for forwards and “{” for backwards.
- Go To Opening Curly Brace `“[{”` - If you’re inside a pair of curly braces you can press “[{“ to jump to the opening brace from any position. Similarly you can use “]}” to jump to the closing one.
- `g` Jumps to the firs word of the document
  
- `G`  : Jumps to the last word of the document
## TABS
- `:tabe # Open new tab`
- `:tabc # Close current tab`
- `:tabo # Close all but current tab`
