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

### Undefined symbols for architecture x86_64: "_libintl_textdomain"

* add "-lintl" to LDFLAGS
