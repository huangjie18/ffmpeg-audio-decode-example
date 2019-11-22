ffmpeg audio decode example
===========================

This repository shows how to decode audio with ffmpeg in C code.

Requirement
===========

- ffmpeg
  - libavcodec     58. 35.100 / 58. 35.100
  - libavformat    58. 20.100 / 58. 20.100
- gcc/clang

Build
=====

```
gcc main.c -o main \
    -I/usr/local/Cellar/ffmpeg/4.1_1/include \
    -L/usr/local/Cellar/ffmpeg/4.1_1/lib \
    -lavformat -lavcodec
```

One needs to make sure that `-I` and `-L` points to the local installation
of ffmpeg and the link `-lavformat -lavcodec` matches what is in the library.

Run
===

```
$ ./main sample.wav
extract sum(data[320000]) = -19955
```