## Search

`/foo` - search forward for foo
`?foo` - search backward for foo
`*` `#` - search forward/backward for the word under cursor
`n` `N` - next/prev occurrence

`:s/old/new/g` - replace old with new in the line
`:%s/old/new/gc` - replace old with new in the file with confirmation


### Search for the selected text

1.  `y` - yank selected text into the unnamed register
1.  `:/\V`Ctrl-R`"` - `/` for search; `\V` to enter *a very nomagic* mode; `Ctrl-R"` for pasting yanked text from the register

