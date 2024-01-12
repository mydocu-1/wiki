## Registers

<code>q**a**</code> - record macro into register **a**

<code>@**a**</code> - run macro from register **a**

`@@` - re-run most recent macro

<code>**\<register\>\<copying command\>**</code>, where copying commands are: `d` `c` `y` `x` etc

<code>"**a**</code> - store result in register **a**
<code>"**A**</code> - append result to register **a**

<code>"**a**p</code> - paste content of register **a** at cursor

*  `""` - unnamed default register
*  `"*` - system clipboard
*  `"+` - system selection
*  `"0` - last yanked text
*  `"1` .. `"9` - last block deletions
*  `"-` - last char deletion
*  `"_` - 'black hole'

`:reg` - content of all registers

<code><b>\<Ctrl-R\></b>**a**</code> - paste from register **a** in _insert_ mode
