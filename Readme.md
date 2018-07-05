# Clang Static Analyzer Example Plugin

This project shows how to build the example
static analyzer plugin from the Clang sources
(`examples/analyzer-plugin/MainCallChecker.cpp`)
out of tree with Meson instead of the LLVM cmake
based build system.

To build:
```.sh
mkdir build
cd build
meson ..
ninja
```

To run with `clang`:
```
```
