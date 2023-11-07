# Vim

## Modes

`<Esc>` - normal
`i` `I` `a` `A` `o` `O` - insert mode  
   `i` = before cursor, `a` = after cursor, `I` = `^i`, `A` = `$a`  
   `o` = line after, `O` = line before  
`R` - replace mode  
`v` `V` ``<C-v>`` - visual mode  
   `V` = line-granular, `<C-v>` = vertical block mode


## Cursor commands

`d` `c` `y` - delete, cut, yank; followed by [motion](motion.md); works in visual mode  
`dd` `cc` `yy` - for the whole line  
`D` `C` `Y` - till the end of line

`x` `X` - delete char under/before cursor  
`r`*a* - replace char under cursor with *a*

`gu` `gU` - to lower/upper case; followed by [motion](motion.md); works in visual mode  
`~` - toggle case of char under cursor

`>>` `<<` - indent for the current line  
`>` `<` - indent for visual mode selection

`p` `P` - paste after/before cursor  
`gp` `gP` - paste and put cursor before  
`]p` - paste after cursor and fix indenting  
`[p` - paste before cursor and fix indenting

`J` - join the next line

`.` - repeat the last command  
`u` - undo the last change  
`U` - undo all changes to the line  
`<C-r>` - redo


## Text objects
**\<command\>\<i|a\>\<text object\>**

`i` - “inside”, does not include the text object surrounding  
`a` - “around”, includes the text object surrounding

`w` - word; surrounding are trailing spaces  
`s` - sentence; surrounding are trailing spaces  
`p` - paragraph; surrounding are trailing lines  
`"` `'` `` ` `` - double-/single-/back-quoted string  
`(` `)` `b` - parentheses  
`{` `}` `B` - curly brackets  
`[` `]` `<` `>` - square/corner brackets  
`t` - markup language tag
