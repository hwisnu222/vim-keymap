# Custom keymap

## Init config vim keymap

create file config

```
# vim
vim ~/.vimrc


# neovim 
nvim ~/.config/nvim/init.lua
```

and puth config vim to this file for example like this

```vim
" ~/.vimrc
" Set leader key
let mapleader = " "

" Custom keymaps
nnoremap <leader>w :w<CR>
inoremap jk <Esc>
vnoremap <C-c> "+y
```

or if you use *.lua file you can set keymap with keymap method useing lua

```lua
-- ~/.config/nvim/init.lua
vim.g.mapleader = " "

-- Normal mode
vim.keymap.set('n', '<leader>ff', ':Telescope find_files<CR>')
vim.keymap.set('n', '<C-s>', ':w<CR>')

-- Insert mode
vim.keymap.set('i', 'jk', '<Esc>')
```



## Complete Guide to `vim.keymap.set()` with Modifier Keys For Lua Neovim Config

## Modifier Key Syntax
| Modifier | Syntax       | Example       | Description              |
|----------|-------------|--------------|--------------------------|
| Ctrl     | `<C-...>`   | `<C-a>`      | Control key combination  |
| Shift    | `<S-...>`   | `<S-Tab>`    | Shift key combination    |
| Alt/Meta | `<A-...>`   | `<A-n>`      | Alt/Option key (Meta)    |
|          | `<M-...>`   | `<M-n>`      | Alternative Meta syntax  |

## Basic Usage Examples

### 1. Essential Mappings
```lua
-- Save file with Ctrl+s
vim.keymap.set("n", "<C-s>", ":w<CR>", { desc = "Save file" })

-- New tab with Ctrl+t
vim.keymap.set("n", "<C-t>", ":tabnew<CR>", { desc = "New tab" })

-- Toggle line numbers with Alt+n
vim.keymap.set("n", "<A-n>", function()
  vim.opt.number = not vim.opt.number._value
end, { desc = "Toggle line numbers" })
```

### Advanced Combinations

```lua
-- Save all and quit with Ctrl+Shift+q
vim.keymap.set("n", "<C-S-q>", ":wqa<CR>", { desc = "Save all and quit" })

-- Format code with Alt+Shift+f
vim.keymap.set("n", "<A-S-f>", vim.lsp.buf.format, { desc = "Format code" })

```


### Practical Configuration Snippet

```lua
-- Set leader key
vim.g.mapleader = " "

-- Window navigation with Alt+arrow keys
vim.keymap.set("n", "<A-Left>", "<C-w>h", { desc = "Move left window" })
vim.keymap.set("n", "<A-Down>", "<C-w>j", { desc = "Move down window" })
vim.keymap.set("n", "<A-Up>", "<C-w>k", { desc = "Move up window" })
vim.keymap.set("n", "<A-Right>", "<C-w>l", { desc = "Move right window" })

-- Buffer management
vim.keymap.set("n", "<leader>bd", ":bdelete<CR>", { desc = "Delete buffer" })
vim.keymap.set("n", "<leader>bn", ":bnext<CR>", { desc = "Next buffer" })
```

### Troubleshooting Tips
- Terminal Conflicts: Some terminals intercept shortcuts like <C-s> (flow control)

- Fix: Run stty -ixon in your shell

Key Verification:

```lua
:verbose map <key>  " Check if key is already mapped
```

#### Special Cases:

Use <M-...> if <A-...> doesn't work

Some terminals require special configuration for Alt/Meta keys
