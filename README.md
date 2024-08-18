# C 

## c_01

```bash

gcc c01.c -o c01
./c01

```

### static link

···bash
gcc -static c01.c -o c01_static

```


gcc -static c01.c -o c01_static -lSystem -macosx_version_min=10.7 -stdlib=libstdc++ -syslibroot `xcrun --show-sdk-path` -lc -lm

### c_01 shared objects

```bash
(base) ➜  cbook git:(main) ✗ otool -L c01
c01:
	/usr/lib/libSystem.B.dylib (compatibility version 1.0.0, current version 1345.100.2)

nm /usr/lib/system/libsystem_kernel.dylib | grep printf

(base) ➜  cbook git:(main) ✗ nm /usr/lib/system/libsystem_kernel.dylib | grep printf
0000000000012a94 T __mach_snprintf
0000000000012920 T __mach_vsnprintf
0000000000011ea4 t _fprintf_stderr
0000000000040200 S _vprintf_stderr_func

```
