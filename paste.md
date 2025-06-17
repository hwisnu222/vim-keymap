# Vim Keymaps for Pasting Inside HTML Tags

Here are several effective ways to paste content inside HTML tags using Vim:

## 1. Normal Mode Visual Selection
```
vitp
```
- `v` - Enter visual mode
- `i` - Select "inner" (inside tag)
- `t` - Target HTML tag
- `p` - Paste after entering visual mode

## 2. Using Text Objects
```
ci<paste>
```
- `c` - Change command
- `i<` - Inner HTML tag content
- Then paste with `Ctrl+Shift+v` or `"+p`

## 3. Pasting Around Tags
```
yatp
```
- `y` - Yank (copy)
- `a` - "Around" (including tag)
- `t` - HTML tag
- `p` - Paste

## 4. With Surround Plugin (if using vim-surround)
```
ysst<paste_text>
```
- `yss` - Surround entire line
- `t` - With HTML tag
- Enter tag name, then paste content

## 5. Pasting Inside Existing Tags
```
cit
```
- Position cursor inside tag
- `cit` - Change inner tag
- Paste content
- `Esc` to exit insert mode

## 6. Selective Pasting in Visual Mode
1. Enter visual mode with `v`
2. Select area inside tag
3. `d` to delete or `y` to yank
4. `p` to paste

## Additional Tips:
- For system clipboard paste: `"+p`
- For multiple pasting: `"0p` (paste from register 0)
- Use `:set paste` before large pastes to avoid auto-indentation

## Practical Example:
If you have:
```html
<div>|</div>
```
(with | as cursor position)

1. Type `cit`
2. Paste text (`Ctrl+Shift+v`)
3. Result:
```html
<div>pasted text</div>
```