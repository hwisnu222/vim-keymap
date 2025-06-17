# Vim Text Objects Documentation

## Yank Inner Text Objects (`yi`)

The following text objects can be used with `yi` (Yank Inside) command in Vim to select and copy specific portions of text:

### Basic Text Objects
- `h` + `GitSigns Select Hunk` - Selects a Git hunk (requires GitSigns plugin)
- `a` + `argument` - Selects an argument in a function call
- `b` + `)]) block` - Selects content inside (), [], or {} blocks
- `B` + `inner [(])` - Selects inner content of nested blocks
- `c` + `class` - Selects a class definition (works in OOP languages)
- `d` + `digit(s)` - Selects numbers/digits
- `e` + `CamelCase / snake_case` - Selects words with mixed case or underscores

### Code Structure Objects
- `f` + `function` - Selects a function body
- `g` + `entire file` - Selects all content in the file
- `i` + `indent` - Selects content at the same indent level
- `o` + `block, conditional, loop` - Selects code blocks (if/else, loops)
- `p` + `inner paragraph` - Selects a paragraph
- `q` + `quote '"'` - Selects content inside quotes (both single and double)
- `s` + `inner sentence` - Selects a sentence (for prose/text)

### Special Characters
- `t` + `tag` - Selects content inside HTML/XML tags
- `u` + `use/call` - Selects function calls (with dot notation)
- `U` + `use/call without dot` - Selects function calls (without dots)
- `w` + `inner word` - Selects a word (alphanumeric characters)
- `W` + `inner WORD` - Selects a WORD (including punctuation)

### String and Block Objects
- `"` + `" string` - Selects inside double quotes
- `%` + `matchup-i%)` - Selects inside matching pairs (requires matchup plugin)
- `'` + `' string` - Selects inside single quotes
- `(` + `() block` - Selects inside parentheses
- `)` + `() block with ws` - Selects inside parentheses including whitespace
- `<` + `<> block` - Selects inside angle brackets
- `>` + `<> block with ws` - Selects inside angle brackets including whitespace

### Special Commands
- `?` + `user prompt` - Prompts for custom text object
- `close % back D/ U scroll` - Navigation commands in help/documentation

## Usage Examples
1. To copy inside quotes: `yi"`
2. To copy a function body: `yif`
3. To copy an HTML tag content: `yit`

## Notes
- These text objects work with other operators too (like `ci` for change, `di` for delete)
- Some objects require specific plugins (like GitSigns or matchup)
- Combine with counts for multiple objects (e.g., `2yiw` yanks two words)