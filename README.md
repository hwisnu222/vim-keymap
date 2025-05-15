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

## 🔥 Text Objects
| Key       | Action                          | Example                     |
|-----------|---------------------------------|-----------------------------|
| `ci"`     | Change inside quotes            | `ci"` → edit "text"         |
| `ci(`     | Change inside parentheses       | `ci(` → edit (text)         |
| `ci[`     | Change inside brackets          | `ci[` → edit [text]         |
| `ci{`     | Change inside braces            | `ci{` → edit {text}         |
| `cit`     | Change inside HTML tag          | `cit` → edit `<p>text</p>`  |
| `yiw`     | Yank inner word                 | `yiw` → copy 'word'         |
| `diw`     | Delete inner word               | `diw` → delete 'word'       |
| `da"`     | Delete around quotes            | `da"` → delete "text"       |

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
| `:%s/old/new/g`    | Replace all in file            |
| `:%s/old/new/gc`   | Replace with confirmation      |
| `:s/old/new/g`     | Replace in current line        |
| `*`                | Search word under cursor       |

## 📦 Window Management
| Key        | Action                       |
|------------|------------------------------|
| `:sp`      | Horizontal split             |
| `:vsp`     | Vertical split               |
| `Ctrl+w+h` | Move to left window          |
| `Ctrl+w+j` | Move to window below         |
| `Ctrl+w+k` | Move to window above         |
| `Ctrl+w+l` | Move to right window         |
| `Ctrl+w=`  | Equalize window sizes        |
| `Ctrl+w_`  | Maximize current window      |

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

## 🛠️ Useful Commands
| Command            | Action                          |
|--------------------|---------------------------------|
| `:w`              | Save file                       |
| `:q`              | Quit                            |
| `:wq`             | Save and quit                   |
| `:e!`             | Reload file (discard changes)   |
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


### Wrap Up

| Key       | Action                          | Mnemonic                   |
|-----------|--------------------------------|---------------------------|
| ci"       | Change inside double quotes     | Change Inside "           |
| ci'       | Change inside single quotes     | Change Inside '           |
| ci(       | Change inside parentheses       | Change Inside (           |
| ci{       | Change inside curly braces      | Change Inside {           |
| ci[       | Change inside square brackets   | Change Inside [           |
| cit       | Change inside HTML/XML tag      | Change Inside Tag         |
| ciw       | Change inside word              | Change Inside Word        |
| cip       | Change inside paragraph         | Change Inside Paragraph   |
| yi"       | Yank inside double quotes       | Yank Inside "            |
| ya"       | Yank around double quotes       | Yank Around "            |
| diw       | Delete inside word              | Delete Inside Word        |
| dat       | Delete around HTML/XML tag      | Delete Around Tag         |
| x         | Delete character under cursor   | eXterminate              |
| X         | Delete character before cursor  | Backspace (X marks spot)  |
| D         | Delete to end of line           | Delete to end            |
| C         | Change to end of line           | Change to end            |
| s         | Substitute character            | Substitute               |
| S         | Substitute entire line          | Substitute line          |
| r         | Replace single character        | Replace                  |
| J         | Join lines                      | Join                     |
| gJ        | Join lines without space        | Greedy Join              |
| cc        | Change entire line              | Change line              |
| dd        | Delete entire line              | Delete line              |
| yy        | Yank (copy) entire line         | Yank line                |
| p         | Paste after cursor              | Paste                    |
| P         | Paste before cursor             | Paste Before             |
| u         | Undo                            | Undo                     |
| Ctrl+r    | Redo                            | Redo                     |
| .         | Repeat last command             | Repeat                   |
| h         | Move left                       | Left                     |
| j         | Move down                       | Down                     |
| k         | Move up                         | Up                       |
| l         | Move right                      | Right                    |
| w         | Move forward by word            | Word                     |
| b         | Move backward by word           | Back                     |
| e         | Move to end of word             | End                      |
| 0         | Move to start of line           | Start of line            |
| ^         | Move to first non-blank char    | First non-blank          |
| $         | Move to end of line             | End of line              |
| gg        | Go to first line of file        | Go to start              |
| G         | Go to last line of file         | Go to end                |
| :n        | Go to line number n             | Number                   |
| Ctrl+o    | Jump back to previous location  | Out                      |
| Ctrl+i    | Jump forward to next location   | In                       |
| /pattern  | Search forward for pattern      | Search                   |
| ?pattern  | Search backward for pattern     | Reverse search           |
| n         | Next search result              | Next                     |
| N         | Previous search result          | Previous                 |
| *         | Search word under cursor        | Star                     |
| #         | Search word under cursor back   | Hash                     |
| :%s/old/new/g | Replace all occurrences      | Substitute               |
| :%s/old/new/gc | Replace with confirmation   | Substitute Confirm       |
| Ctrl+w s  | Split window horizontally       | Window Split             |
| Ctrl+w v  | Split window vertically         | Window Vertical          |
| Ctrl+w h/j/k/l | Move between windows      | Window navigation        |
| Ctrl+w c  | Close current window            | Window Close             |
| Ctrl+w o  | Close other windows             | Window Only              |
| :tabe     | Open new tab                    | Tab Edit                |
| gt        | Go to next tab                  | Go Tab                  |
| gT        | Go to previous tab              | Go Previous Tab         |
| :tabn     | Next tab                        | Tab Next                |
| :tabp     | Previous tab                    | Tab Previous            |
| v         | Enter visual mode (char)        | Visual                  |
| V         | Enter visual line mode          | Visual Line             |
| Ctrl+v    | Enter visual block mode         | Visual Block            |
| >         | Indent selection                | Indent                  |
| <         | Unindent selection              | Unindent                |
| y         | Yank selection                  | Yank                    |
| d         | Delete selection                | Delete                  |
| ~         | Toggle case of selection        | Toggle case             |
| "ay       | Yank to register a              | Yank to register        |
| "ap       | Paste from register a           | Paste from register     |
| "+y       | Yank to system clipboard        | System Yank             |
| "+p       | Paste from system clipboard     | System Paste            |
| :reg      | Show all registers              | Registers               |
| qa        | Start recording macro to a      | Record macro            |
| q         | Stop recording macro            | Quit recording          |
| @a        | Execute macro in register a     | Execute macro           |
| @@        | Repeat last executed macro      | Repeat macro            |
| ma        | Set mark at position 'a'        | Mark                    |
| 'a        | Jump to mark 'a'                | Go to mark              |
| :marks    | List all marks                  | List marks              |
| g~        | Toggle case of motion           | Toggle case             |
| gu        | Lowercase motion                | Lowercase               |
| gU        | Uppercase motion                | Uppercase               |
| gqq       | Format current line             | Format line             |
| gqgq      | Format selected text            | Format selection        |
| ==        | Auto-indent current line        | Auto-indent             |
| gg=G      | Auto-indent entire file         | Auto-indent all         |
| :e file   | Open file                       | Edit                    |
| :w        | Save file                       | Write                   |
| :wq       | Save and quit                   | Write Quit              |
| :q        | Quit                            | Quit                    |
| :q!       | Quit without saving             | Quit force              |
| :saveas   | Save as new file                | Save As                 |
| gd        | Go to definition                | Go Definition           |
| K         | Show documentation              | Documentation           |
| Ctrl+]    | Jump to tag definition          | Tag jump                |
| Ctrl+t    | Jump back from tag definition   | Tag back                |
| Ctrl+a    | Increment number under cursor   | Add                     |
| Ctrl+x    | Decrement number under cursor   | Subtract                |
| :!cmd     | Execute shell command           | Shell command           |
| :r !cmd   | Insert command output           | Read command            |
| do        | Diff obtain                     | Diff Obtain             |
| dp        | Diff put                        | Diff Put                |
| ]c        | Next diff                       | Next diff               |
| [c        | Previous diff                   | Previous diff           |
| zc        | Close fold                      | Close fold              |
| zo        | Open fold                       | Open fold               |
| za        | Toggle fold                     | Toggle fold             |
| zR        | Open all folds                  | Open all folds          |
| zM        | Close all folds                 | Close all folds         |
| ]s        | Next spelling error             | Next spelling           |
| [s        | Previous spelling error         | Previous spelling       |
| z=        | Show spelling suggestions       | Spelling suggestions    |
| zg        | Add word to spellfile           | Add to spellfile        |
| Ctrl+g    | Show file status                | Get info                |
| g Ctrl+g  | Show detailed file status       | Detailed info           |
| %         | Jump to matching bracket        | Match bracket           |
| ``        | Jump to last position           | Last position           |

> **Pro Tip**: Combine motions with commands for powerful editing:
> - `d3w` → Delete 3 words forward
> - `c$` → Change to end of line
> - `yG` → Yank to end of file
> - `>j` → Indent current and next line




