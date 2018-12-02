---
layout: default
---

# *ld: warning: ignoring file xxx.a, file was built for archive which is not the architecture being linked (x86_64)

Please check which nm/ar/ranlib is used in MacOS.
*DO NOT* use any other nm/ar/ranlib except /usr/bin/nm ar ranlib.
If you install binutils/gcc, please double check its ar NOT in your PATH.
