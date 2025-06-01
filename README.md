# Ultimate Vim Keymap Cheatsheet for Coding
## Essential Editing

`x`: Delete character under cursor  
- example: `x` → delete 'a'  

`dw`: Delete word  
- example: `dw` → delete 'word'  

`dd`: Delete line  
- example: `3dd` → delete 3 lines  

`D`: Delete to end of line  
- example: `D` → delete rest of line  

`u`: Undo  
- example: `u` → undo last change  

`Ctrl+r`: Redo  
- example: `Ctrl+r` → redo  

`.`: Repeat last command  
- example: After `dw`, `.` → delete next word  

## Navigation
`h`: Move left  
- mnemonic: Left  

`j`: Move down  
- mnemonic: Down  

`k`: Move up  
- mnemonic: Up  

`l`: Move right  
- mnemonic: Right  

`w`: Next word start  
- mnemonic: **w**ord  

`b`: Previous word start  
- mnemonic: **b**ack  

`e`: Next word end  
- mnemonic: **e**nd  

`0`: Start of line  
- mnemonic: Zero position  

`^`: First non-blank char  
- mnemonic: (none)  

`$`: End of line  
- mnemonic: (none)  

`gg`: Top of file  
- mnemonic: (none)  

`G`: Bottom of file  
- mnemonic: (none)  

`H`: Top of screen  
- mnemonic: **H**igh  

`M`: Middle of screen  
- mnemonic: **M**iddle  

`L`: Bottom of screen  
- mnemonic: **L**ow  

`Ctrl+u`: Scroll up half page  
- mnemonic: (none)  

`Ctrl+d`: Scroll down half page  
- mnemonic: (none)  

`Ctrl+o`: Jump back to previous location  
- mnemonic: (none)  

`Ctrl+i`: Jump forward to next location  
- mnemonic: (none)  

`[{`: Previous block bracket  
- mnemonic: (none)  

`]}`: Next block bracket  
- mnemonic: (none)  

`[(`: Previous block curly  
- mnemonic: (none)  

`])`: Next block curly  
- mnemonic: (none)  

## Text Objects
`ci"`: Change inside quotes  
- mnemonic: **c**hange **i**nside "quotes"
- example: `ci"` → edit "text" between quotes

`ci'`: Change inside single quotes
- mnemonic: **c**hange **i**nside 'quotes'
- example: `ci'` → edit 'text' between single quotes

`ci(`: Change inside parentheses
- mnemonic: **c**hange **i**nside (parens)
- example: `ci(` → edit (text) inside parentheses

`ci[`: Change inside brackets
- mnemonic: **c**hange **i**nside [brackets]
- example: `ci[` → edit [text] inside brackets

`ci{`: Change inside braces
- mnemonic: **c**hange **i**nside {braces}
- example: `ci{` → edit {text} inside curly braces

`cit`: Change inside HTML tag
- mnemonic: **c**hange **i**nside <tag>
- example: `cit` → edit `<p>text</p>` within tags

`ciw`: Change inside word
- mnemonic: **c**hange **i**nner **w**ord
- example: `ciw` → edit 'word' under cursor

`yiw`: Yank inner word
- mnemonic: **y**ank **i**nner **w**ord
- example: `yiw` → copy 'word' to register

`diw`: Delete inner word
- mnemonic: **d**elete **i**nner **w**ord
- example: `diw` → remove 'word' under cursor

`vi{`: Visual/select inside braces
- mnemonic: **v**isual **i**nside {braces}
- example: `vi{` → visual/select {text} inside curly braces


`da"`: Delete around quotes
- mnemonic: **d**elete **a**round "quotes"
- example: `da"` → delete "text" including quotes

`dat`: Delete around HTML tag
- mnemonic: **d**elete **a**round <tag>
- example: `dat` → delete `<p>text</p>` entirely

## Visual Mode
`v`: Enter character-wise visual mode
- mnemonic: **v**isual
- example: Select characters by moving cursor

`V`: Enter line-wise visual mode
- mnemonic: **V**isual-line
- example: Select entire lines by moving up/down

`Ctrl+v`: Enter block visual mode
- mnemonic: Visual-**b**lock (Ctrl+v looks like block selection)
- example: Select vertical columns of text

`>`: Indent selection
- mnemonic: Right angle = increase indent
- example: `>j` indents current and next line

`<`: Unindent selection
- mnemonic: Left angle = decrease indent
- example: `<k` unindents current and previous line

`y`: Yank (copy) selection
- mnemonic: **y**ank
- example: `y` then `p` to paste selection

`d`: Delete selection
- mnemonic: **d**elete
- example: `d` removes highlighted text

`~`: Toggle case of selection
- mnemonic: ~ looks like a tilde/wave for switching
- example: `~` changes "Text" to "tEXT"

`gv`: Reselect last visual selection
- mnemonic: **g**o **v**isual
- example: After escape, `gv` re-highlights previous area

## Search & Replace
### Search Command
`/pattern`: Search forward
- mnemonic: / leans forward → forward search
- example: /hello finds next "hello"

`?pattern`: Search backward
- mnemonic: ? leans backward → backward search
- example: ?error finds previous "error"

`n`: Next match
- mnemonic: **n**ext
- example: After /search, press n to find next

`N`: Previous match
- mnemonic: **N**ot-next (opposite of n)
- example: After /search, press N to go back

`*`: Search word under cursor (forward)
- mnemonic: * is a wildcard → expand current word
- example: Over "text", * finds next "text"

`#`: Search word under cursor (backward)
- mnemonic: # is shift+3 (opposite of *)
- example: Over "text", # finds previous "text"

### Replace command
`:%s/old/new/g`: Replace all in file
- mnemonic: **s**ubstitute **g**lobally
- example: :%s/cat/dog/g changes all "cat" to "dog"

`:%s/old/new/gc`: Replace with confirmation
- mnemonic: **c**onfirm each change
- example: :%s/foo/bar/gc asks before each replace

`:s/old/new/g`: Replace in current line
- mnemonic: No % → current line only
- example: :s/yes/no/g changes on current line

## Window Management
`Ctrl+w c`: Close current window
- mnemonic: **c**lose
- example: Closes current pane (buffer stays loaded)

`Ctrl+w o`: Close other windows
- mnemonic: **o**nly
- example: Keeps only current pane open

`Ctrl+w =`: Equalize window sizes
- mnemonic: **=** (equals sign for balance)
- example: Makes all panes equal size

`Ctrl+w _`: Maximize current window
- mnemonic: **_** (underscore = expand height)
- example: Current pane takes full height

### Window splitting
`:sp`: Horizontal split
- mnemonic: **sp**lit horizontally
- example: :sp file.txt opens file in pane below

`:vsp`: Vertical split
- mnemonic: **v**ertical **sp**lit
- example: :vsp file.txt opens file in pane to the right

`Ctrl+w s`: Split window horizontally
- mnemonic: **s**plit (same as :sp)
- example: Splits current buffer horizontally

`Ctrl+w v`: Split window vertically
- mnemonic: **v**ertical (same as :vsp)
- example: Splits current buffer vertically

`:res +20` : Resize horizontal window

`:vert res +80` : Resize vertical


`Ctrl+w o` : Close all window except active window\

`Ctrl+w r` : Rotate window

`gt` : Go to next tab

`gT` : Go to previous tab

`2gt` : Go to tab number 2

### Window navigation
`Ctrl+w h`: Move to left window
- mnemonic: **h** (vim's left movement key)
- example: Move cursor to left pane

`Ctrl+w j`: Move to window below
- mnemonic: **j** (vim's down movement key)
- example: Jump to lower pane

`Ctrl+w k`: Move to window above
- mnemonic: **k** (vim's up movement key)
- example: Jump to upper pane

`Ctrl+w l`: Move to right window
- mnemonic: **l** (vim's right movement key)
- example: Move cursor to right pane

`:tabn`: Switch to next tab  
mnemonic: **Tab Next**

`:tabp`: Switch to previous tab  
mnemonic: **Tab Previous**

`:tabfirst`: Switch to first tab  
mnemonic: -

`:tablast`: Switch to last tab  
mnemonic: -

`2gt`: Switch to tab number 2  
mnemonic: **G**o to **T**ab 2



## Advanced Operations
### Macro command
`q[a-z]`: Start recording macro
- mnemonic: **q**ueue recording in register [a-z]
- example: `qa` starts recording to register 'a'

`q`: Stop recording macro
- mnemonic: **q**uit recording
- example: Press `q` to finish macro recording

`@[a-z]`: Execute macro
- mnemonic: **@**tack (run) from register [a-z]
- example: `@a` plays back macro from 'a'

`@@`: Repeat last macro
- mnemonic: Double **@** = repeat last action
- example: After `@a`, `@@` runs 'a' again

### Number operations
`Ctrl+a`: Increment number
- mnemonic: **+a** (think addition)
- example: On `42`, becomes `43`

`Ctrl+x`: Decrement number
- mnemonic: **-x** (think subtraction)
- example: On `42`, becomes `41`

### Text formatting
`gq`: Format text
- mnemonic: **g**ood **q**uote (for text wrapping)
- example: `gqip` reformats current paragraph

`==`: Auto-indent line
- mnemonic: **=** (equals for alignment)
- example: Fixes indentation on current line

`gg=G`: Auto-indent entire file
- mnemonic: **gg** (start) **=** (indent) **G** (end)
- example: Properly indents whole file



## Useful Commands
### File operation
`:w` - Save file
- mnemonic: **w**rite
- example: :w myfile.txt saves to myfile.txt

`:q` - Quit
- mnemonic: **q**uit
- example: :q closes current window

`:wq` - Save and quit
- mnemonic: **w**rite + **q**uit
- example: :wq saves changes and exits

`:q!` - Force quit without saving
- mnemonic: ! means "force"
- example: :q! discards all changes

`:e` file - Open file
- mnemonic: **e**dit
- example: :e ~/.vimrc opens vim config

`:e!` - Reload file (discard changes)
- mnemonic: ! means "discard current"
- example: :e! reverts to saved version


### File management
`:saveas` - Save as new file
- mnemonic: literal meaning
- example: :saveas backup.txt creates copy

`:set nu` - Show line numbers
- mnemonic: **nu**mbers
- example: :set nu displays line numbers

`:set nonu` - Hide line numbers
- mnemonic: **no** **nu**mbers
- example: :set nonu hides numbering

`:set paste` - Enable paste mode
- mnemonic: literal
- example: Before pasting external text

`:set nopaste` - Disable paste mode
- mnemonic: **no**paste
- example: After pasting to resume formatting


## Help & Discovery
### Help system
`:help [topic]` - Open help
- mnemonic: Literal
- example: 
  - `:help w`       - Show help for 'w' command
  - `:help :w`      - Show help for :w command
  - `:help options` - Learn about configuration

`:options` - Open interactive options window
- mnemonic: Literal
- example: Browse/change settings with GUI-like interface

### Key mapping inspections
`:map` - Show all custom key mappings
- mnemonic: Literal
- example: 
  - `:map`        - Shows normal mode mappings
  - `:vmap`       - Shows visual mode mappings
  - `:imap`       - Shows insert mode mappings

`:verb map <key>` - Show key's definition and origin
- mnemonic: **verb**ose mapping
- example: 
  - `:verb map <Leader>f`  - Shows where <Leader>f was defined
  - `:verb map <C-Space>` - Debug complex key combinations

### System information
`:reg` - Show register contents
- mnemonic: **reg**isters
- example: 
  - `:reg`      - Shows all registers
  - `:reg a`    - Show only register 'a'
  - `"ap`       - Paste from register 'a'

`:marks` - Show all marks
- mnemonic: Literal
- example: 
  - `:marks`    - List all marks
  - `a`        - Jump to mark 'a'
  - `.`        - Jump to last edit position


## Special Operations
### Code navigation
`gd`: Go to definition
- mnemonic: **g**o **d**efinition
- example: Hover over function → `gd` jumps to its definition

`K`: Show documentation
- mnemonic: **K**now (like man pages)
- example: Cursor on function → `K` shows its docs

`Ctrl+]`: Jump to tag definition
- mnemonic: ] looks like arrow pointing in
- example: Jump to function/variable declaration

`Ctrl+t`: Jump back from tag
- mnemonic: **t**ag back
- example: Return from definition jump

### Diff tool
`do`: Diff obtain (get changes)
- mnemonic: **d**iff **o**btain
- example: In diff view, pull changes from other file

`dp`: Diff put (send changes)
- mnemonic: **d**iff **p**ut
- example: In diff view, push changes to other file

`]c`: Next diff
- mnemonic: ] moves forward
- example: Jump to next changed block

`[c`: Previous diff
- mnemonic: [ moves backward
- example: Jump to previous changed block

### Folding controls
`zc`: Close fold
- mnemonic: **z**ip **c**lose
- example: Collapse current code block

`zo`: Open fold
- - mnemonic: **z**ip **o**pen
- - example: Expand current collapsed block

`za`: Toggle fold
- - mnemonic: **z**ip **a**lternate
- - example: Toggle current fold state

`zR`: Open all folds
- mnemonic: **R**ecursively open
- example: Expand all nested folds

`zM`: Close all folds
- mnemonic: **M**aximally close
- example: Collapse entire file structure



> **Pro Tip**: Combine motions with commands for powerful editing:
> - `d3w` → Delete 3 words forward
> - `c$` → Change to end of line
> - `yG` → Yank to end of file
> - `>j` → Indent current and next line




