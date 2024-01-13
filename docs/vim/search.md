## Search

`/foo` - search forward for foo<br>
`?foo` - search backward for foo<br>
`*` `#` - search forward/backward for the word under cursor<br>
`n` `N` - next/prev occurrence

`:s/old/new/g` - replace old with new in the line<br>
`:%s/old/new/gc` - replace old with new in the file with confirmation


### Search for the selected text

1.  `y` - yank selected text into the default register `"`<br>
1.  <code>:/\V<C-r\>"</code> - `/` for search; `\V` to enter *a very nomagic* mode; <code><C-r\>"</code> for pasting yanked text from the register `"`

