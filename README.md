# kmod
## A Linux kernel module written in Rust

# How to Build
First you want to install nightly build of Rust,
```
$ rustup install nightly
info: syncing channel updates for 'nightly'
info: downloading toolchain manifest
info: downloading component 'rustc'
info: downloading component 'rust-std'
info: downloading component 'rust-docs'
info: downloading component 'cargo'
info: installing component 'rustc'
info: installing component 'rust-std'
info: installing component 'rust-docs'
info: installing component 'cargo'

  nightly installed: rustc 1.9.0-nightly (02310fd31 2016-03-19)
```
Then, you want to switch to the nightly buid:
```
rustup run nightly rustc --version
rustup default nightly
```

Dependency are the current Linux headers for your running kernel. To build the module simply execute in the root
directory:
```
make
```

To build a release execute:
```
make RELEASE=1
```

The kernel module can be found in `./target/kernel/kmod.ko`.

