## Buffers

Buffer = File

`:enew` - opens new (empty) buffer<br>
`:e <filename>` - opens existing file in buffer

`:ls` - lists all buffers<br>
<code>:b**#**</code> - go to buffer by its number **#**<br>
`:bn` - next buffer<br>
`:bp` - previous buffer

`<C-^>` - toggle between current and previous buffer

`:bd` - delete (close) current buffer, remove it from buffer list<br>
`:bun` - unload (close) current buffer, keep it in buffer list


## Windows

Window = Viewport

`:sp`, `:split` - divide current window on top and bottom parts<br>
`:vs`, `:vsplit` - divide current window on left and right parts

`<C-w>-<hjkl>` - navigate windows

`:q` - closes current window; if its the only window, then exit vim

