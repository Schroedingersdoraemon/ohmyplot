- for linux, install libsdl3 using your package manager
- for windows, download sdl3-mingw

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
