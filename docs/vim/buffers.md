## Buffers

Buffer = File

`:enew` - opens new (empty) buffer
`:e <filename>` - opens existing file in buffer

`:ls` - lists all buffers
`:b`*#* - go to buffer by its number
`:bn` - next buffer
`:bp` - previous buffer

`Ctrl-^` - toggle between current and previous buffer

`:bd` - delete (close) current buffer, remove it from buffer list
`:bun` - unload (close) current buffer, keep it in buffer list


## Windows

Window = Viewport

`:sp`, `:split` - divide current window on top and bottom parts
`:vs`, `:vsplit` - divide current window on left and right parts

`Ctrl-W-<hjkl>` - navigate windows

`:q` - closes current window

