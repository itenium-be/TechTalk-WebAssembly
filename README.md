WebAssembly For Web Developers
==============================

Code for the [itenium blog post](TODO URL HERE) on the [Google I/O '19 talk](https://www.youtube.com/watch?v=njt-Qzw0mVY)
by Surma Surma and Deepti Gandluri.

HelloWorld example for running C in the browser using WebAssembly and Emscripten.


## Windows SDK Installation

[Install the Emscripten SDK](https://emscripten.org/docs/getting_started/downloads.html)

```ps1
git clone https://github.com/emscripten-core/emsdk.git
cd emsdk
.\emsdk.ps1 install latest
.\emsdk.ps1 activate latest
emsdk_env.bat
```


## Compilation

```bash
emcc HelloWorld.c -s WASM=1 -o HelloWorld.html
```


## Run generated wasm

```bash
npx http-server
```

And open browser:  
- `HelloWorld.html`: The initially generated Html file
- `HelloWorld-Minimal.html`: The minimal required Html file


Or with `emrun` which comes with the SDK:  
```
emrun HelloWorld.html
```
