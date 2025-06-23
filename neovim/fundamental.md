# Fundamental


### Keymap 


Here's the structure of `vim.keymap.set()`:

---

### **1. `{mode}` (Table/String, Optional)**

This specifies the **Neovim mode(s)** where the keymap will be active. You can provide it as:

* **A string:** For example, `"n"` for normal mode, `"i"` for insert mode, `"v"` for visual mode.
* **A table of strings:** For example, `{"n", "v"}` if you want the mapping active in both normal and visual modes.

**Commonly used modes:**

* `"n"`: Normal
* `"i"`: Insert
* `"v"`: Visual (includes visual-line and visual-block)
* `"x"`: Visual (same as "v")
* `"s"`: Select
* `"o"`: Operator-pending
* `"t"`: Terminal
* `"c"`: Command-line
* `""` (empty string): All modes

If you **omit** `{mode}`, Neovim will default to creating the mapping for **all appropriate modes** (typically normal, visual, select, and operator-pending).

---

### **2. `{lhs}` (String)**

This is the **"Left Hand Side"** or the **key combination** you want to map. Examples:

* `"<leader>w"`: Your `leader` key followed by `w`. The `leader` key is a special key you can configure (often `\` or `Space`).
* `"<C-s>"`: `Ctrl` + `s`.
* `"<A-f>"`: `Alt` + `f`.
* `"jk"`: Pressing `j` then `k`.
* `"q"`: Pressing `q`.

---

### **3. `{rhs}` (String/Function)**

This is the **"Right Hand Side"** or **what will be executed** when `{lhs}` is pressed.

* **String:** This can be a Vim command that will be executed. Examples:
    * `":w<CR>"`: Writes (saves) the file and presses Enter.
    * `"yy"`: Yanks (copies) the current line.
    * `"<C-o>"`: Neovim command to "go to previous position in jump list".
* **Function (Lua `function()`):** This is more powerful as you can write custom Lua logic. Example:
    ```lua
    function()
        print("Hello from a keymap!")
    end
    ```

---

### **4. `{opts}` (Table, Optional)**

This is a table of additional **options** that control the keymap's behavior. Some common options include:

* `desc` (String): A short description of the keymap's purpose. This is very useful for plugins like `which-key.nvim`.
* `silent` (Boolean): If `true`, Neovim won't display messages or flash the screen when the keymap is triggered. Defaults to `false`.
* `buffer` (Boolean/Number): If `true`, the mapping will be local to the current buffer. If you provide a buffer number, it will apply to that specific buffer ID. Defaults to `false` (global).
* `noremap` (Boolean): If `true`, the `{rhs}` will not be remapped recursively. This is a **highly recommended** practice for most keymaps to prevent unexpected behavior from other keymaps. Defaults to `false` (remapped). This is equivalent to `<Plug>` in Vimscript.
* `nowait` (Boolean): If `true`, Neovim will not wait for further input if `{rhs}` could be partially triggered by another keymap.
* `expr` (Boolean): If `true`, the `{rhs}` will be evaluated as a Vimscript expression.
* `unique` (Boolean): If `true`, the same mapping will not be created twice.

---

### **Usage Examples:**

```lua
-- Basic mapping: Press <leader>w to save the file in normal mode
vim.keymap.set("n", "<leader>w", ":w<CR>", { silent = true, desc = "Save current file" })

-- Mapping for multiple modes: Press <C-f> to scroll forward one screen
vim.keymap.set({"n", "v"}, "<C-f>", "<C-f>", { noremap = true, silent = true, desc = "Scroll half page forward" })

-- Mapping with a Lua function: Press <leader>t to open a new terminal
vim.keymap.set("n", "<leader>t", function()
    vim.cmd("term")
end, { silent = true, desc = "Open new terminal" })

-- Buffer-local mapping: Only applies to the current buffer
vim.keymap.set("n", "<leader>ll", function()
    print("This keymap is only for this buffer!")
end, { buffer = true, silent = true, desc = "Local buffer keymap" })
```

