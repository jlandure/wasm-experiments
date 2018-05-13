# WASM Experiments

# Pre-requisites

You need Git, Python and Emscripten
On Mac, in the `$HOME/.emscripten` file, set 
`LLVM_ROOT = '/usr/local/opt/emscripten/libexec/llvm/bin'`

## hello - How to

See the `Hello.c` file

```
#include <stdio.h>
int main(int argc, char ** argv) {
  printf("Hello, world!\n");
}
```

Then, use this command to generate the `ìndex.html`

```
emcc hello.c -s WASM=1 -o hello.html
```



## ball - How to

Configre

Compile using
```
emcc -s WASM=1 \
     -O3 -s EXTRA_EXPORTED_RUNTIME_METHODS='["cwrap"]' \
     -o ball.js ball.cpp 
```
