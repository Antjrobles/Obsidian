---
title: Neovim Config
description: How to install and config Neovim
created: 12-10-2022
tags:
- neovim
- plugins
---
## CONFIGURATION FILE

- `~/.config/nvim/init.vim` - If don't exist there, create it
  - `sudo mkdir -p ~/.config/nvim/` and then `sudo touch init.vim'

## INSTALLATION ON RPI

- `sudo apt update`
- `sudo apt install -y neovim`
- `nvim --version`

#### INSTALLING THE LATEST VERSION ON RPI

```bash
sudo apt update
sudo apt install snapd
sudo snap install nvim --classic
# Then create a symkink. Becaue nvim is now installed in /snap/bin/nvim
sudo ln -s /snap/bin/nvim /usr/bin/nvim
nvim --version
```

## UNISTALLING NEOVIM

- `sudo apt purge --autoremove -y neovim`
- `rm -rf ~/.local/share/nvim`
- `sudo rm -rf /root/.local/share/nvim`

## INSTALLING PLUGINS

- [Guide](https://www.linode.com/docs/guides/how-to-install-neovim-and-plugins-with-vim-plug/)
-   Para instalar vim-plug ejecuta el siguiente comando en la terminal:
```bash
curl -fLo ~/.local/share/nvim/site/autoload/plug.vim --create-dirs https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```

1. `sudo apt-get install fuse libfuse2 git python3-pip ack-grep -y`
2. `pip3 install --user neovim`
3. Add the following lines at the bottom of your `~/.config/nvim/init.vim` file to install Plugin Manager:

```bash
call plug#begin()

 Plugins Here

call plug#end()
```

## MY CONFIGURATION FILE

```bash
" CONFIGURATION "
set title  " Muestra el nombre del archivo en la ventana de la terminal
set number  " Muestra los números de las líneas
set mouse=a  " Permite la integración del mouse (seleccionar texto, mover el cursor)
set cursorline  " Resalta la línea actual
set tabstop=2 " Identacion a dos espacios 
set textwidth=140
set noshowmode  " No mostrar el modo actual (ya lo muestra la barra de estado)
set shiftround
set expandtab  " Insertar espacios en lugar de <Tab>s
set hidden  " Permitir cambiar de buffers sin tener que guardarlos
set ignorecase  " Ignorar mayúsculas al hacer una búsqueda
set smartcase  " No ignorar mayúsculas si la palabra a buscar contiene mayúsculas
set spelllang=en,es  " Corregir palabras usando diccionarios en inglés y español
color torte
set showmatch               " show matching 
set ignorecase              " case insensitive 
set mouse=v                 " middle-click paste with 
set hlsearch                " highlight search 
set incsearch               " incremental search
set softtabstop=4           " see multiple spaces as tabstops so <BS> does the right thing
set expandtab               " converts tabs to white space
set shiftwidth=4            " width for autoindents
set autoindent              " indent a new line the same amount as the line just typed
set wildmode=longest,list   " get bash-like tab completions
set cc=140                  " set an 80 column border for good coding style                                                                
filetype plugin indent on   "allow auto-indenting depending on file type
syntax on                   " syntax highlighting
set clipboard=unnamedplus   " using system clipboard
filetype plugin on
set cursorline              " highlight current cursorline
set ttyfast                 " Speed up scrolling in Vim
" set spell                 " enable spell check (may need to download language package)
```

## MY PLUGINS CONFIG

```bash
" Directorio de plugins
call plug#begin('~/.local/share/nvim/plugged')
Plug 'scrooloose/nerdtree' " file system explorer for the Vim editor 
Plug 'vim-airline/vim-airline' " Lean & mean status/tabline for vim that's light as air.
Plug 'vim-airline/vim-airline-themes'  " Temas para vim-airline
Plug 'Yggdroot/indentLine'  " Displaying thin vertical lines at each indentation level for code indented with spaces
Plug 'github/copilot.vim'  " Copilot Plugin for Neovim
Plug 'ryanoasis/vim-devicons'
Plug 'SirVer/ultisnips'
Plug 'honza/vim-snippets'
Plug 'preservim/nerdcommenter'
Plug 'mhinz/vim-startify'
" DEOPLETE (Auto completado asíncrono para Neovim)
Plug 'Shougo/deoplete.nvim', { 'do': ':UpdateRemotePlugins' }
Plug 'Shougo/neco-syntax'  " Fuente general de auto completado
call plug#end()


" Luego de esta línea puedes agregar tus configuraciones y mappings

let g:NERDTreeChDirMode = 2  " Cambia el directorio actual al nodo padre actual (NERDTree)

" vim-airline configuraciones 
let g:airline#extensions#tabline#enabled = 1  " Mostrar buffers abiertos (como pestañas)
let g:airline#extensions#tabline#fnamemod = ':t'  " Mostrar sólo el nombre del archivo
let g:airline#extensions#tabline#left_sep = ' '
let g:airline#extensions#tabline#left_alt_sep = '|'
let g:airline#extensions#tabline#formatter = 'unique_tail_improved'
let g:airline_powerline_fonts = 1 " Cargar fuente Powerline y símbolos

" No mostrar en ciertos tipos de buffers y archivos (indentLine)
"let g:indentLine_fileTypeExclude = ['text', 'sh', 'help', 'terminal']
"let g:indentLine_bufNameExclude = ['NERD_tree.*', 'term:.*']
let g:indentLine_setColors = 0
"let g:indentLine_color_term = 39
"let g:indentLine_char_list = ['|'] 


" DEOPLETE CONFIG
let g:deoplete#enable_at_startup = 1

" Cerrar automaticamente la ventana de vista previa (donde se muestra documentación, si existe)
augroup deopleteCompleteDoneAu
  autocmd!
  autocmd CompleteDone * silent! pclose!
augroup END




" Abrir/cerrar NERDTree con F2
map <F2> :NERDTreeToggle<CR>
```
