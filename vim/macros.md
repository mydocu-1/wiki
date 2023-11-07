# Vim

## Macros

### Record
1.  `q`*a* - record macro in register *a*
1.  `q` - stop recording

### Play
`@`*a* - play macro from register *a*

`@@` - repeat last executed macro

`:normal @`*a* - play macro from register *a* on visual selection

### View
`:reg `*a* - view macro in register *a*

### Edit
1.  `"`*a*`p` - paste the contents of the register *a* at cursor
1.  Edit
1.  `"`*a*`yy` - yank edited macro into register
1.  `dd` - delete line
