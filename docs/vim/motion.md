# Motion

## Moving cursor

`<C-g>` - show location and file status

`h` `j` `k` `l` - left, up, down, right<br>
`0` `^` `$` - start / end of line<br>
`gj` `gk` `g^` `g$` - movements for wrapped lines

`w` `b` - to next/prev beginning of the word<br>
`W` `B` - with respect to spaces<br>
`e` `ge` - to next/prev end of the word<br>
`E` `gE` - with respect to spaces

`(` `)` - to prev/next sentence beginning<br>
`{` `}` - to prev/next paragraph beginning

`fa` `Fa` - to next/prev a occurrence<br>
`ta` `Ta` - before next/prev a occurrence<br>
`;` `'` - repeat last f/t command in forward/backward direction<br>
`%` - to matching parentheses ( ) [ ] { }

`gg` `G` - start / end of file<br>
`123G` `:123` - to line 123<br>
`H` `M` `L` - to high/middle/low visible line<br>
`zt` `zz` `zb` - scroll line under cursor to be top/middle/bottom visible line<br>
`<C-f>` `<C-b>` - page forward/backward<br>
`<C-d>` `<C-u>` - half-page down/up

` `` `  `''` - back/forth between prev/current locations / to the first non-blank char of the line<br>
`<C-o>` `<C-i>` - back/forth by location history<br>
`:jumps` - list locations history


## Marks

`ma` - set mark a<br>
`` `a `` - go to mark a<br>
`'a` - go to to the first non-blank char of the line with mark a<br>
`` [` `` `` ]` `` - to the prev/next lowercase mark<br>
`:marks` - list marks


### Special marks

`'` - position before the last jump<br>
`.` - last edit location<br>
`[` `]` - first/last char of previously yanked text<br>
`<` `>` - first/last character of the last selected visual mode text

