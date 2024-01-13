## Registers

<code>q**a**</code> - record macro into register **a**

<code>@**a**</code> - run macro from register **a**

`@@` - re-run most recent macro

<code>**<register\><copying command\>**</code>, where copying commands are: `d` `c` `y` `x` etc

<code>"**a**</code> - store result in register **a**<br>
<code>"**A**</code> - append result to register **a**

<code>"**a**p</code> - paste content of register **a** at cursor

Registers:<br>
`""` - unnamed default register<br>
`"*` - system clipboard<br>
`"+` - system selection<br>
`"0` - last yanked text<br>
`"1` .. `"9` - last block deletions<br>
`"-` - last char deletion<br>
`"_` - 'black hole'<br>

`:reg` - content of all registers

<code><C-r\>**a**</code> - paste from register **a** in _insert_ mode
