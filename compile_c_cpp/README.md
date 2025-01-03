# zig compiling C/C++ code

Yeah, it is possible to compile C/C++ code with zig itself.

Notice the size and the libraries that are linked with the corresponding binaries too! On Fedora 41 zig 0.13 I get:

    -rwxr-xr-x. 1 dgunchev dgunchev  15232 2025-01-04 00:12 hello_c
    -rwxr-xr-x. 1 dgunchev dgunchev   4096 2025-01-04 00:12 hello_c_zig

and

    -rwxr-xr-x. 1 dgunchev dgunchev  15232 2025-01-04 00:12 hello_cpp
    -rwxr-xr-x. 1 dgunchev dgunchev 267504 2025-01-04 00:13 hello_cpp_zig

And the libraries linked:

    $ ldd hello_c
        linux-vdso.so.1 (0x00007f3255d15000)
        libc.so.6 => /lib64/libc.so.6 (0x00007f3255ae7000)
        /lib64/ld-linux-x86-64.so.2 (0x00007f3255d17000)
    $ ldd hello_c_zig
        linux-vdso.so.1 (0x00007f4362598000)
        libc.so.6 => /lib64/libc.so.6 (0x00007f436236a000)
        /lib64/ld-linux-x86-64.so.2 (0x00007f436259a000)
    $ ldd hello_cpp
        linux-vdso.so.1 (0x00007f5be8eb7000)
        libstdc++.so.6 => /lib64/libstdc++.so.6 (0x00007f5be8c00000)
        libm.so.6 => /lib64/libm.so.6 (0x00007f5be8b1a000)
        libgcc_s.so.1 => /lib64/libgcc_s.so.1 (0x00007f5be8aeb000)
        libc.so.6 => /lib64/libc.so.6 (0x00007f5be88f7000)
        /lib64/ld-linux-x86-64.so.2 (0x00007f5be8eb9000)
    $ ldd hello_cpp_zig
        linux-vdso.so.1 (0x00007f550e4f7000)
        libc.so.6 => /lib64/libc.so.6 (0x00007f550e2c9000)
        /lib64/ld-linux-x86-64.so.2 (0x00007f550e4f9000)
