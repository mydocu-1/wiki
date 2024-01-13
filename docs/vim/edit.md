# Edit

## Modes

`<Esc>` - normal

`i` `I` `a` `A` `o` `O` - insert mode<br>
 `i` = before cursor, `a` = after cursor, `I` = `^i`, `A` = `$a`<br>
`o` = line after, `O` = line before

`R` - replace mode; `r` - replace a single character

`v` `V` ``<C-v>`` - visual mode<br>
`V` = line-granular, `<C-v>` = vertical block mode


## Cursor commands

`d` `c` `y` - delete, cut, yank; followed by [motion](motion.md); works in visual mode<br>
`dd` `cc` `yy` - for the whole line<br>
`D` `C` `Y`[^1] - till the end of line

[^1]: Reasonable override of the default behavior with `nnoremap Y y$`.

`x` `X` - delete char under/before cursor<br>
`r`*a* - replace char under cursor with *a*<br>

`gu` `gU` - to lower/upper case; followed by [motion](motion.md); works in visual mode<br>
`~` - toggle case of char under cursor

`>>` `<<` - indent for the current line<br>
`>` `<` - indent for visual mode selection

`p` `P` - paste after/before cursor<br>
`gp` `gP` - paste and put cursor before<br>
`]p` - paste after cursor and fix indenting<br>
`[p` - paste before cursor and fix indenting

`J` - join the next line

`.` - repeat the last command<br>
`u` - undo the last change<br>
`U` - undo all changes to the line<br>
`<C-r>` - redo


## Text objects

**<command\><i|a\><text object\>**

`i` - “inside”, does not include the text object surrounding<br>
`a` - “around”, includes the text object surrounding

`w` - word; surrounding are trailing spaces<br>
`s` - sentence; surrounding are trailing spaces<br>
`p` - paragraph; surrounding are trailing lines<br>
`"` `'` `` ` `` - double-/single-/back-quoted string<br>
`(` `)` `b` - parentheses<br>
`{` `}` `B` - curly brackets<br>
`[` `]` `<` `>` - square/corner brackets<br>
`t` - markup language tag

