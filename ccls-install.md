Commands to install ccls from source (Ubuntu 20.04, build agains `llvm-13`):

```
sudo apt install clang-13 cmake libclang-13-dev llvm-13-dev rapidjson-dev
```

```
cd /tmp && mkdir ccls-make && cd ccls-make
```

```
git clone --depth=1 --recursive https://github.com/MaskRay/ccls && cd ccls
```

```
$ cmake -H. -BRelease -DCMAKE_BUILD_TYPE=Release \
    -DCMAKE_PREFIX_PATH=/usr/lib/llvm-13 \
    -DLLVM_INCLUDE_DIR=/usr/lib/llvm-13/include \
    -DLLVM_BUILD_INCLUDE_DIR=/usr/include/llvm-13/
```

```
$ cmake --build Release
```
