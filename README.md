# m1-utm-linux

A step-by-step guide on how to run Linux in [UTM](https://mac.getutm.app) on M1 Macs

Currently supported guides:

| guest architecture | guest Linux flavour |
| ------------------ | ------------------- |
| native (arm64) | [Arch Linux](https://archlinux.org) |

_Skip the pleasantries and send me to the [instructions](#how-instructions)!_

# What

So you've obtained an M1 Mac, and you'd like to harness the power of Linux by
way of virtualization.

Maybe you're doing work that involves syscalls, maybe you prefer a distinct
boundary between your browsing software and your devving software, or maybe you
want to try it because you can.

This guide will help you set up a Linux VM using UTM, in a way that should be
stable for in-band guest OS updates.

# Why

You could download a version of Linux from the [UTM
gallery](https://mac.getutm.app/gallery/), but:

  * some gallery images (e.g. [ArchLinux
    ARM](https://mac.getutm.app/gallery/archlinux-arm)) contain multiple drives
    * these gallery images make it difficult to upgrade the VM in-band via
      `pacman -Syu` and the like
    * the method of installation listed below emulates a real OS install on one
      disk file, thus hopefully making the upgrade procedure smoother and more
      future-proof
  * you're trusting the gallery image hasn't been tampered with
    * while I have full faith in the developers to not trojan horse anything
      (after all, we _are_ using the emulation software they developed), I
      would prefer to see through my OS' genesis, allowing for both
      customization and inspection; the same may apply to you

# How (instructions)

## Prerequisites

  * macOS with an M1 processor
    * if you're on a Mac, typing `uname -m` into the terminal should show you `arm64`
  * UTM
    * get it from their website at https://mac.getutm.app

## Per-flavour Linux instructions

Please visit the following sub-pages for guides on each supported flavour.

  * [arm64 Arch Linux](arm64-arch/README.md)
