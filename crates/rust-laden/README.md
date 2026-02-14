<!--
     Copyright 2023, Colias Group, LLC

     SPDX-License-Identifier: CC-BY-SA-4.0
-->

# Laden

`laden-rust` is based on ['sel4-kernel-loader'](https://github.com/seL4/rust-sel4/tree/main/crates/sel4-kernel-loader), and is intended to be a multiboot loader for the sel4
kernel and a multiboot compatible root task.

Currently, it's just a fork of sel4-kernel-loader, but together with other parts should form part of a multiboot2 boot chain for aarch64 devices into seL4.

Usage is similar to sel4-kernel-loader.

