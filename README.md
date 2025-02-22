# MEMZ Nyan MBR

## Debugging
I have extracted the bootloader portion of the malware and would want to debug the initial bootloader.

Furthermore, [https://astralvx.com/debugging-16-bit-in-qemu-with-gdb-on-windows/](https://astralvx.com/debugging-16-bit-in-qemu-with-gdb-on-windows/) contains really helpful three helper scripts to let us debug the MBR! 
```
gdb -ix "gdb_init_real_mode.txt" -ex "set tdesc filename target.xml" -ex "target remote localhost:1234" -ex "br *0x7c00" -ex "c"
```

