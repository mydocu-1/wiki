# Vim

## Moving cursor

`<C-g>` - show location and file status

`h` `j` `k` `l` - left, up, down, right  
`0` `^` `$` - start / end of line  
`gj` `gk` `g^` `g$` - movements for wrapped lines

`w` `b` - to next/prev beginning of the word  
`W` `B` - with respect to spaces  
`e` `ge` - to next/prev end of the word  
`E` `gE` - with respect to spaces

`(` `)` - to prev/next sentence beginning  
`{` `}` - to prev/next paragraph beginning

`fa` `Fa` - to next/prev a occurrence  
`ta` `Ta` - before next/prev a occurrence  
`;` `'` - repeat last f/t command in forward/backward direction  
`%` - to matching parentheses ( ) [ ] { }

`gg` `G` - start / end of file  
`123G` `:123` - to line 123  
`H` `M` `L` - to high/middle/low visible line  
`zt` `zz` `zb` - scroll line under cursor to be top/middle/bottom visible line  
`<C-f>` `<C-b>` - page forward/backward  
`<C-d>` `<C-u>` - half-page down/up

` `` `  `''` - back/forth between prev/current locations / to the first non-blank char of the line  
`<C-o>` `<C-i>` - back/forth by location history  
`:jumps` - list locations history


## Marks
`ma` - set mark a  
`` `a `` - go to mark a  
`'a` - go to to the first non-blank char of the line with mark a  
`` [` `` `` ]` `` - to the prev/next lowercase mark
`:marks` - list marks

### Special marks
`'` - position before the last jump  
`.` - last edit location  
`[` `]` - first/last char of previously yanked text  
`<` `>` - first/last character of the last selected visual mode text
