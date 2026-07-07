---
title: Calling PAPI from Python in 2026
description: ""
date: 2026-07-07
tags:
  - english
---

I tried calling the PAPI high-level API from Python for [one of my projects](/blog/2025/energy-efficiency).
Naturally, I looked if someone else has done this before and found [PyPAPI](https://flozz.github.io/pypapi/), developed by [Fabien / FLOZz](https://www.flozz.fr).
It took me a bit too long to realize that 
1. [he had stopped maintaining it](https://github.com/flozz/pypapi#end-of-life-notice) and
2. this was the reason for me getting output files that had some unexpected structure (compared to instrumenting some C++ code on the same machine).

I confirmed this with him: python-papi "is shipped with its own copy of PAPI", "you may find a `_papi.abi3.so` file in the wheel package".
(Thanks for being so responsive, Fabien!)
The PAPI version in PyPAPI is outdated, which was causing the unexpected structure of the output files.

Anyway, at the start of this year I had learned how to call shared libraries from Python using [ctypes](https://docs.python.org/3/library/ctypes.html), so I actually managed to quickly fix this myself.
Here is how you can call PAPI's high-level API by directly loading `libpapi.so` in Python:

```py
import ctypes

libpapi = ctypes.cdll.LoadLibrary("libpapi.so")

# convert the string to bytes so that it is represented correctly
region_name = "test"
region_name_buffer = ctypes.create_string_buffer(region_name.encode())

libpapi.PAPI_hl_region_begin(region_name_buffer)

# do your thing

libpapi.PAPI_hl_region_end(region_name_buffer)
```

For other PAPI functions, [check their Wiki](https://github.com/icl-utk-edu/papi/wiki/).
Passing integers should work without problems, and for strings as above, just use `encode()` and `create_string_buffer()`.
