## Registers

`q`*a* - record macro into register *a*
`@`*a* - run macro from register *a*
`@@` - re-run most recent macro

**\<register\>\<copying command\>**
copying commands: `d` `c` `y` `x` etc

`"`*a* - store result in register *a*
`"`*A* - append result to register *a*

`"`*a*`P` - paste content of register *a*

`""` - unnamed default register
`"*` - system clipboard
`"+` - system selection
`"0` - last yanked text
`"1` .. `"9` - last block deletions
`"-` - last char deletion
`"_` - 'black hole'

`:reg` - content of all registers

`Ctrl-R`*a* - paste from register *a* in _insert_ mode

