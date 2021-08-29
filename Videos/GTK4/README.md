## Building Dependencies

**GLib**:

1. Download `glib-2.68.4.tar.xz` file from https://download.gnome.org/sources/glib/2.68/?C=M&O=D.
2. Extract using `tar -xf glib-2.68.4.tar.xz` and `cd` into the directory.
3. Go to `INSTALL.in` file and follow the instructions:

```
meson _build  # Configure project
ninja -C _build  # Compile
ninja -C _build install  # If permission denied error, try using sudo;
```
