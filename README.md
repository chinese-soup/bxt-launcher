![image](https://user-images.githubusercontent.com/1794388/76060644-c862bf00-5f92-11ea-9603-849f02753bc1.png)

# Bunnymod XT Launcher

GUI launcher for [Bunnymod XT](https://github.com/YaLTeR/BunnymodXT) on Linux.

## Usage

1. Download the latest [release](https://github.com/YaLTeR/bxt-launcher/releases).
1. Extract all files from the archive.
1. Open bxt-launcher.

## Building

You will need the Vala compiler and GTK libraries (GIO, GTK, libgtop).

The launcher expects to find its GSettings schema and `libBunnymodXT.so` alongside its binary.
Installing into a prefix without `DESTDIR` sets everything up:

```sh
meson -Dprefix=$PWD/install build
ninja -C build install
# Copy libBunnymodXT.so into install/bin/ manually.
# Then start the launcher:
install/bin/bxt-launcher
```
