<!--
     Copyright 2023, Colias Group, LLC

     SPDX-License-Identifier: CC-BY-SA-4.0
-->

# sel4-rust-hurd

A continuation of my pointless efforts to:

- Get a Multiboot2 compatible boot chain on arm64
- Explore Rust
- Explore GNU Hurd

This is currently a simple fork of [sel4-root-task-demo](https://github.com/rel4team/rust-root-task-demo),
but should build over time into:

- Patch for grub to add a new target arm64-efi-multiboot
- A multiboot loader for the sel4 kernel (rust-laden)
- A root task (sigma0)
- Other servers as needed to create a GNU Hurd compatible interface

It is targeted at arm64/aarch64, in QEMU for now, but with the intention of targeting a simple 
generation of Raspiberry PI.

### Quick start

The only requirements for getting started are Git, Make, and Docker.

First, clone this respository:

```
git clone https://github.com/chunky125/sel4-rust-hurd.git
cd sel4-rust-hurd
```

Next, build, run, and enter a Docker container for development:

```
make -C docker/ run && make -C docker/ exec
```

Finally, inside the container, build and emulate a simple seL4-based system with a root task written
in Rust:

```
make run
```
