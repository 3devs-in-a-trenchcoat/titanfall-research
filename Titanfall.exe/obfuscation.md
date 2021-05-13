# Origin launch obfuscation
The entrypoint of the executable does an instantaneous (ignoring the nop) jump into the origin `activation64.dll`.
``` asm
jmp qword [rel Ordinal_Core/Activation64_100@IAT]
```
Strings for the binary hint that it promptly calls `launcher.dll` and `tier0.dll`:
```
Failed to load the launcher DLL at \"%s\":\n\n%s\x00\x00\x00\x00%s\\bin\\x64_retail\\tier0.dll\x00\x00\x00\x00\x00%s\\bin\\x64_retail\\launcher.dll
```

Ultimately I don't really want to disable this unless I have to.
