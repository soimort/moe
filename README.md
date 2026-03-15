# moe

A fork of the [eom](https://github.com/mate-desktop/eom/tree/1.26) image viewer (1.26).

## How to build

```
$ ./autogen.sh
$ ./configure \
    --prefix=/usr \
    --localstatedir=/var \
    --with-librsvg \
$ make
$ src/eom -n
```
