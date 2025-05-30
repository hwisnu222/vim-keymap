# Ultimate Vim Keymap Cheatsheet for Coding
## 🚀 Essential Editing
| Key       | Action                          | Example                     |
|-----------|---------------------------------|-----------------------------|
| `x`       | Delete character under cursor   | `x` → delete 'a'            |
| `dw`      | Delete word                     | `dw` → delete 'word'        |
| `dd`      | Delete line                     | `3dd` → delete 3 lines      |
| `D`       | Delete to end of line           | `D` → delete rest of line   |
| `u`       | Undo                            | `u` → undo last change      |
| `Ctrl+r`  | Redo                            | `Ctrl+r` → redo             |
| `.`       | Repeat last command             | After `dw`, `.` → delete next word |

## 🧭 Navigation
| Key       | Action                          | Mnemonic                   |
|-----------|---------------------------------|----------------------------|
| `h`       | Move left                       | Left                       |
| `j`       | Move down                       | Down                       |
| `k`       | Move up                         | Up                         |
| `l`       | Move right                      | Right                      |
| `w`       | Next word start                 | **w**ord                   |
| `b`       | Previous word start             | **b**ack                   |
| `e`       | Next word end                   | **e**nd                    |
| `0`       | Start of line                   | Zero position              |
| `^`       | First non-blank char            |                            |
| `$`       | End of line                     |                            |
| `gg`      | Top of file                     |                            |
| `G`       | Bottom of file                  |                            |
| `H`       | Top of screen                   | **H**igh                   |
| `M`       | Middle of screen                | **M**iddle                 |
| `L`       | Bottom of screen                | **L**ow                    |
| `Ctrl+u`  | Scroll up half page             |                            |
| `Ctrl+d`  | Scroll down half page           |                            |
| `Ctrl+o`  | Jump back to previous location  |                            |
| `Ctrl+i`  | Jump forward to next location   |                            |
| `[{`      | Previos block bracket           |                            |
| `]}`      | Next block bracket              |                            |
| `[(`      | Previos block curly             |                            |
| `])`      | Next block curly                |                            |

## 🔥 Text Objects
| Key       | Action                          | Example                     |
|-----------|---------------------------------|-----------------------------|
| `ci"`     | Change inside quotes            | `ci"` → edit "text"         |
| `ci'`     | Change inside single quotes     | `ci'` → edit 'text'         |
| `ci(`     | Change inside parentheses       | `ci(` → edit (text)         |
| `ci[`     | Change inside brackets          | `ci[` → edit [text]         |
| `ci{`     | Change inside braces            | `ci{` → edit {text}         |
| `cit`     | Change inside HTML tag          | `cit` → edit `<p>text</p>`  |
| `ciw`     | Change inside word              | `ciw` → edit 'word'         |
| `yiw`     | Yank inner word                 | `yiw` → copy 'word'         |
| `diw`     | Delete inner word               | `diw` → delete 'word'       |
| `da"`     | Delete around quotes            | `da"` → delete "text"       |
| `dat`     | Delete around HTML tag          | `dat` → delete `<p>text</p>`|

## 🎯 Visual Mode
| Key        | Action                       | Mode                      |
|------------|------------------------------|---------------------------|
| `v`        | Character-wise visual        |                           |
| `V`        | Line-wise visual             |                           |
| `Ctrl+v`   | Block visual                 |                           |
| `>`        | Indent selection             |                           |
| `<`        | Unindent selection           |                           |
| `y`        | Yank selection               |                           |
| `d`        | Delete selection             |                           |
| `~`        | Toggle case                  |                           |
| `gv`       | Reselect last visual         |                           |

## 🔍 Search & Replace
| Command            | Action                          |
|--------------------|---------------------------------|
| `/pattern`         | Search forward                 |
| `?pattern`         | Search backward                |
| `n`                | Next match                     |
| `N`                | Previous match                 |
| `*`                | Search word under cursor       |
| `#`                | Search word under cursor back  |
| `:%s/old/new/g`    | Replace all in file            |
| `:%s/old/new/gc`   | Replace with confirmation      |
| `:s/old/new/g`     | Replace in current line        |

## 📦 Window Management
| Key        | Action                       |
|------------|------------------------------|
| `:sp`      | Horizontal split             |
| `:vsp`     | Vertical split               |
| `Ctrl+w s` | Split window horizontally    |
| `Ctrl+w v` | Split window vertically      |
| `Ctrl+w h` | Move to left window          |
| `Ctrl+w j` | Move to window below         |
| `Ctrl+w k` | Move to window above         |
| `Ctrl+w l` | Move to right window         |
| `Ctrl+w c` | Close current window         |
| `Ctrl+w o` | Close other windows          |
| `Ctrl+w =` | Equalize window sizes        |
| `Ctrl+w _` | Maximize current window      |

## 💎 Advanced Operations
| Key        | Action                       | Example                     |
|------------|------------------------------|-----------------------------|
| `q[a-z]`   | Start recording macro        | `qa` → start macro in 'a'   |
| `q`        | Stop recording               |                             |
| `@[a-z]`   | Execute macro                | `@a` → run macro 'a'        |
| `@@`       | Repeat last macro            |                             |
| `Ctrl+a`   | Increment number             | `Ctrl+a` on 5 → 6           |
| `Ctrl+x`   | Decrement number             | `Ctrl+x` on 5 → 4           |
| `gq`       | Format text                  | `gqip` → format paragraph   |
| `==`       | Auto-indent line             |                             |
| `gg=G`     | Auto-indent entire file      |                             |

## 🛠️ Useful Commands
| Command            | Action                          |
|--------------------|---------------------------------|
| `:w`              | Save file                       |
| `:q`              | Quit                            |
| `:wq`             | Save and quit                   |
| `:q!`             | Quit without saving             |
| `:e file`         | Open file                       |
| `:e!`             | Reload file (discard changes)   |
| `:saveas`         | Save as new file                |
| `:set nu`         | Show line numbers               |
| `:set nonu`       | Hide line numbers               |
| `:set paste`      | Enable paste mode               |
| `:set nopaste`    | Disable paste mode              |

## � Help & Discovery
| Command            | Action                          |
|--------------------|---------------------------------|
| `:help [topic]`    | Open help                       |
| `:map`             | Show all key mappings           |
| `:verb map <key>`  | Show what a key does            |
| `:options`         | Open options window             |
| `:reg`             | Show registers                  |
| `:marks`           | Show marks                      |

## 📌 Special Operations
| Key        | Action                       |
|------------|------------------------------|
| `gd`       | Go to definition             |
| `K`        | Show documentation           |
| `Ctrl+]`   | Jump to tag definition       |
| `Ctrl+t`   | Jump back from tag           |
| `do`       | Diff obtain                  |
| `dp`       | Diff put                     |
| `]c`       | Next diff                    |
| `[c`       | Previous diff                |
| `zc`       | Close fold                   |
| `zo`       | Open fold                    |
| `za`       | Toggle fold                  |
| `zR`       | Open all folds               |
| `zM`       | Close all folds              |
> **Pro Tip**: Combine motions with commands for powerful editing:
> - `d3w` → Delete 3 words forward
> - `c$` → Change to end of line
> - `yG` → Yank to end of file
> - `>j` → Indent current and next line




