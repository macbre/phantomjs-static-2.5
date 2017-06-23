# phantomjs-static-2.5

Static build of [PhantomJS 2.5 beta](https://github.com/ariya/phantomjs/issues/14458)

```bash
$ wget http://ftp.pl.debian.org/debian/pool/main/libj/libjpeg8/libjpeg8_8d1-2_amd64.deb && sudo dpkg -i libjpeg8_8d1-2_amd64.deb
$ ldd phantomjs25-static 
	linux-vdso.so.1 (0x00007ffef47ce000)
	libfontconfig.so.1 => /usr/lib/x86_64-linux-gnu/libfontconfig.so.1 (0x00007f84e042d000)
	libfreetype.so.6 => /usr/lib/x86_64-linux-gnu/libfreetype.so.6 (0x00007f84e0183000)
	libjpeg.so.8 => /usr/lib/x86_64-linux-gnu/libjpeg.so.8 (0x00007f2c462ae000)
	libssl.so.1.0.0 => /usr/lib/x86_64-linux-gnu/libssl.so.1.0.0 (0x00007f84dff21000)
	libz.so.1 => /lib/x86_64-linux-gnu/libz.so.1 (0x00007f84dfd06000)
	libdl.so.2 => /lib/x86_64-linux-gnu/libdl.so.2 (0x00007f84dfb01000)
	librt.so.1 => /lib/x86_64-linux-gnu/librt.so.1 (0x00007f84df8f9000)
	libpthread.so.0 => /lib/x86_64-linux-gnu/libpthread.so.0 (0x00007f84df6dc000)
	liblzma.so.5 => /lib/x86_64-linux-gnu/liblzma.so.5 (0x00007f84df4b8000)
	libm.so.6 => /lib/x86_64-linux-gnu/libm.so.6 (0x00007f84df1b7000)
	libc.so.6 => /lib/x86_64-linux-gnu/libc.so.6 (0x00007f84dee0c000)
	/lib64/ld-linux-x86-64.so.2 (0x000055c6df940000)
	libexpat.so.1 => /lib/x86_64-linux-gnu/libexpat.so.1 (0x00007f84debe2000)
	libpng12.so.0 => /lib/x86_64-linux-gnu/libpng12.so.0 (0x00007f84de9bb000)
	libcrypto.so.1.0.0 => /usr/lib/x86_64-linux-gnu/libcrypto.so.1.0.0 (0x00007f84de5bf000)
$ ./phantomjs25-static --version
2.5.0-development

phantomjs> phantom.version
{
   "major": 2,
   "minor": 5,
   "patch": 0
}
```

```bash
$ ldd phantomjs211-static 
	linux-vdso.so.1 (0x00007ffe2a360000)
	libz.so.1 => /lib/x86_64-linux-gnu/libz.so.1 (0x00007f8f82c88000)
	libfontconfig.so.1 => /usr/lib/x86_64-linux-gnu/libfontconfig.so.1 (0x00007f8f82a4b000)
	libfreetype.so.6 => /usr/lib/x86_64-linux-gnu/libfreetype.so.6 (0x00007f8f827a0000)
	libdl.so.2 => /lib/x86_64-linux-gnu/libdl.so.2 (0x00007f8f8259c000)
	librt.so.1 => /lib/x86_64-linux-gnu/librt.so.1 (0x00007f8f82394000)
	libpthread.so.0 => /lib/x86_64-linux-gnu/libpthread.so.0 (0x00007f8f82176000)
	libstdc++.so.6 => /usr/lib/x86_64-linux-gnu/libstdc++.so.6 (0x00007f8f81e6b000)
	libm.so.6 => /lib/x86_64-linux-gnu/libm.so.6 (0x00007f8f81b6a000)
	libgcc_s.so.1 => /lib/x86_64-linux-gnu/libgcc_s.so.1 (0x00007f8f81953000)
	libc.so.6 => /lib/x86_64-linux-gnu/libc.so.6 (0x00007f8f815a8000)
	/lib64/ld-linux-x86-64.so.2 (0x0000555c95463000)
	libexpat.so.1 => /lib/x86_64-linux-gnu/libexpat.so.1 (0x00007f8f8137f000)
	libpng12.so.0 => /lib/x86_64-linux-gnu/libpng12.so.0 (0x00007f8f81157000)
```
