## Installing/Building Dependencies

**Basic Dependencies**:

- CMake: `sudo apt install cmake`
- `pkg-config`: `sudo apt install pkg-config`
- GCC Compiler: `sudo apt install gcc`

**Meson and Ninja**:

- Prefer installing using `pip`: `pip install meson ninja`.

**GLib**:

1. Download `glib-2.68.4.tar.xz` file from https://download.gnome.org/sources/glib/2.68/?C=M&O=D.
2. Extract using `tar -xf glib-2.68.4.tar.xz` and `cd` into the directory.
3. Go to `INSTALL.in` file and follow the instructions:

```bash
meson _build  # Configure project
ninja -C _build  # Compile
ninja -C _build install  # If permission denied error, try using sudo;
```

**GdkPixbuf**:

I needed to install following dependencies first for `GdkPixbuf`:

```bash
sudo apt install xorg-docs docbook-xsl
```

1. Download `gdk-pixbuf-2.42.6.tar.xz` file from https://download.gnome.org/sources/gdk-pixbuf/2.42/.
2. Extract using `tar xf gdk-pixbuf-2.42.6.tar.xz` command and `cd` into the directory.
3. Follow the instructions given in `README.md`.

```
meson setup _build
meson compile -C _build
meson install -C _build
```

**GObject**:

Install the following dependencies first:

```
sudo apt install flex bison
```

1. Download `gobject-introspection-1.69.0.tar.xz` from https://download.gnome.org/sources/gobject-introspection/1.69/.
2. Extract using `tar xf https://download.gnome.org/sources/gobject-introspection/1.69/` and `cd` into the directory.
3. Follow these instructions:

```
meson setup _build .
meson compile -C _build
meson install -C _build
```
