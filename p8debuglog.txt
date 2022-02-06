
 gcc -g p8original.c
 gdb a.out
GNU gdb (Ubuntu 8.1.1-0ubuntu1) 8.1.1
Copyright (C) 2018 Free Software Foundation, Inc.
License GPLv3+: GNU GPL version 3 or later <http://gnu.org/licenses/gpl.html>
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.  Type "show copying"
and "show warranty" for details.
This GDB was configured as "x86_64-linux-gnu".
Type "show configuration" for configuration details.
For bug reporting instructions, please see:
<http://www.gnu.org/software/gdb/bugs/>.
Find the GDB manual and other documentation resources online at:
<http://www.gnu.org/software/gdb/documentation/>.
For help, type "help".
Type "apropos word" to search for commands related to "word"...
Reading symbols from a.out...done.
(gdb) b main
Breakpoint 1 at 0xa3f: file p8original.c, line 66.
(gdb) r
Starting program: /home/runner/pps-IA1-practice-6/a.out 
warning: Error disabling address space randomization: Operation not permitted

Breakpoint 1, main () at p8original.c:66
66  {
(gdb) n
67    int n = get_n();
(gdb) n
Enter the number of complex numbers:2
68    complex c[n], res;
(gdb) n
69    input_n_complex(n,c);
(gdb) n
Enter the real part:2
Enter the imaginary part:3
Enter the real part:4
Enter the imaginary part:5
70    res = add_n_complex(n,c);
(gdb) n
71    output(n, c, res);
(gdb) n
2.00 + 3.00i
+ 4.00 + 5.00i is
6.00 + 8.00i
72    return 0;
(gdb) c
Continuing.
[Inferior 1 (process 186) exited normally]
(gdb) 