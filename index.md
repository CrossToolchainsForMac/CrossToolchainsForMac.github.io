---
layout: default
title: "Hotfixes"
author: jerzha@qq.com
---

### ld: warning: ignoring file xxx.a, file was built for archive which is not the architecture being linked (x86_64)

* Please check which nm/ar/ranlib is used in MacOS.
* *DO NOT* use any other nm/ar/ranlib except /usr/bin/nm ar ranlib.
* If you install binutils/gcc, please double check its ar/nm NOT in your PATH.

### fatal error: bracket nesting level exceeded maximum of 256

* add "-fbracket-depth=512" to CFLAGS & CXXFLAGS

### gcc/as: line xxx: exec: -E: invalid option

* It is because there is no default as/ld binary in host-x86_64-apple-darwin18.2.0/gcc/as
* Workaround way: set host-x86_64-apple-darwin18.2.0/gcc/as ORIGINAL_AS_FOR_TARGET & ORIGINAL_LD_FOR_TARGET manually.
