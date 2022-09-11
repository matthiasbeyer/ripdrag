# What is ripdrag?
![Crates.io](https://img.shields.io/crates/d/ripdrag?style=for-the-badge)
![GitHub top language](https://img.shields.io/github/languages/top/nik012003/ripdrag?color=dea584&style=for-the-badge)
![Crates.io](https://img.shields.io/crates/v/ripdrag?style=for-the-badge)

ripdrag is an application that lets you drag and drop files from and to the terminal.

It's designed to be feature to feature* compatible with [dragon](https://github.com/mwh/dragon), while being written in modern Rust and GTK4.

![Example](/docs/example.gif)

*some features like --on-top can't be ported over because of limitations in gtk4
# Use cases

Many applications expect files to be dragged into them. Normally you would have to put your beloved terminal aside and open a file manager to that, but now you can just type ```ripdrag FILENAME``` and be done.

Used in combination with a fuzzy finder like [fzf](https://github.com/junegunn/fzf) - e.g. ```ripdrag $(fzf)``` - can make for an amazingly quick and painless terminal experience.

# How to install
```
cargo install ripdrag
```
# Usage
```
USAGE:
    ripdrag [OPTIONS] [PATHS]...

ARGS:
    <PATHS>...    Paths to the files you want to drag

OPTIONS:
    -a, --all                                Drag all the items together
    -A, --all-compact                        Show only the number of items and drag them together
    -h, --content-height <CONTENT_HEIGHT>    Height of the main window [default: 360]
        --help                               Print help information
    -i, --icons-only                         Only display icons, no labels
    -I, --from-stdin                         Accept paths from stdin
    -r, --resizable                          Make the window resizable
    -s, --thumb-size <THUMB_SIZE>            Size of icons and thumbnails [default: 32]
    -w, --content-width <CONTENT_WIDTH>      Width of the main window [default: 360]
    -x, --and-exit                           Exit after first successful drag or drop      
```
# TODO
There are still lots of thing to be done! Mainly:
- drag files from other apps to the terminal
- clean up code
- pacman, deb, rpm, windows and macos build scripts
- automated builds

Feel free to contribute ;)