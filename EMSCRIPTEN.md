# Emscripten

## Build

```
mkdir build
cd build
emcmake cmake ..
emmake make
```

## Link

```
emcc -flto -O3 -fno-rtti -fno-exceptions *.o -o index.html -sUSE_SDL=2 -sUSE_SDL_MIXER=2 -sSDL2_MIXER_FORMATS='["wav","ogg"]' -sENVIRONMENT=web --preload-file ../../../../data/@data/ --closure 1 -sEXPORTED_RUNTIME_METHODS=['allocate']
```
