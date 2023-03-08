## Challenge 55.  

This one is pretty simple, so I started with it.

Compiled with `cl /O2 /nologo challenge_55.c`

The resulting exe was then opened in radare2 with `r2 -w challenge_55.exe`

At `0x00401011` the `i` variable is moved into `$esi`.  The bytes representing 2 was incremented to 6.

At `0x0040102f` the compare test for ending the `for` loop is done.  The bytes holding `10` were incremented to `20`.

After exiting r2 the patched program gave correct output.
