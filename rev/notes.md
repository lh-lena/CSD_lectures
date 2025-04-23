Static Analysis
- ELF101 a Linux executable walkthrough
- anatomy of the file

1. install ida or ghidra
2. web tool:
    dogbolt https://dogbolt.org/ 

/demos
$ gcc main.c
$ file a.out 
a.out: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, BuildID[sha1]=f9c2e988d67dd1ecfb234a48ef3672f1252b60a9, for GNU/Linux 3.2.0, not stripped

- not stripped means that binary still has its symbols. Symbols means you can see the functions signatures
- stripped means you're no gonna be able to see this

$ strip --strip-all a.out
-- if to decompile stpipped binary, no function will be visible, but main()

