- for linux, install libsdl3 using your package manager
- for windows, download sdl3-mingw (e.g. [sdl3-devel-mingw-3.2.8](https://github.com/libsdl-org/SDL/releases/download/release-3.2.8/SDL3-devel-3.2.8-mingw.tar.gz) ) in github release,
then place SDL3.dll and libSDL3.dll.a under third_party/SDL3

```shell
# build project
cmake -B build

# build project, but with vscode clangd completions
cmake -B build -DCMAKE_EXPORT_COMPILE_COMMANDS=1
mv build/compile_commands.json .vscode
```

```shell
# if Makefile in build
make -C build -j
# else if build.ninja
ninja -C build -j 0
```

```shell
# imgui test demo
./build/demo_imgui{.exe}

# ohmyplot using implot
./build/ohmyplot{.exe}
```
