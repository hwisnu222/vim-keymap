# Vim

set keymap on `.vimrc` by default vim use format 

```vim
" Format dasar:
:[mode]map <combination-keyboard> <command>
```

**Mode:**
- nmap - Normal mode
- imap - Insert mode
- vmap - Visual mode
- xmap - Visual mode saja
- cmap - Command-line mode
- tmap - Terminal mode

## Basic Mapping
Example:
```vim
" F2 for save file
nmap <F2> :w<CR>

" Ctrl+s for save file in insert mode
imap <C-s> <Esc>:w<CR>a

" Leader key (default: \)
let mapleader = ","  " Ubah leader key ke koma

" Leader mapping
nmap <leader>w :w<CR>\
```


## Method mapping

```vim
" Ctrl+n untuk toggle line number
nnoremap <C-n> :set invnumber<CR>

" Format JSON dengan =j
nnoremap =j :%!python -m json.tool<CR>
```


## Complex mapping

```vim
" Pindah antara buffer
nnoremap <silent> <C-right> :bnext<CR>
nnoremap <silent> <C-left> :bprevious<CR>

" Resize window dengan Ctrl+arrow
nnoremap <C-Up> :resize +2<CR>
nnoremap <C-Down> :resize -2<CR>
```

Create new keymap with `leader` so default vim keymap not override with custom keymap

for create leader button you put code in `.vimrc`

```vim
let mapleader = " "
nnoremap <leader>ff :find<Space>
```



## Show keymaps

if you want to see all keymap, you can run this command

```vim
:map  " semua mapping
:nmap " normal mode mapping
```