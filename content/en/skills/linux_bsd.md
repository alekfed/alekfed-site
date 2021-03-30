+++
title = "System administration"
subtitle = "Experience: 4 years"
tags = ['System']
date = 2020-03-26

# For description meta tag
description = "Operating systems and systems programming."

# Comment next line and the default banner wil be used.
banner = 'img/linux_bsd.svg'

+++

Understanding of operating systems and shell scripting are essential skills when you work with back-end and DevOps.

# Linux

For a long time, Arch Linux was my day-to-day system, and Debian was the typical choice for servers. Recently I got interested in ideas of stateless operating systems based on functional declarative configurations, which led me to [NixOS](https://nixos.org/) ([my config](https://git.sr.ht/~alekfed/nix-config)) and [Guix](https://guix.gnu.org/).

From system administration perspective, it's interesting that NixOS may eliminate the hassle of fiddling with [Ansible](https://www.ansible.com/) when upgrading servers and ensure that they will work at any upgrade, but the lack of NixOS-based boot images from cloud providers at the moment limits the applicability of these ideas. As for Guix: despite the all Scheme attractiveness, its time has not yet come (and may not come at all): even if the system can be started on real hardware (there are difficulties), kernel recompilation on every update due to the use of non-free drivers is just too much—thanks, Gentoo was enough...

Talking about Linux these days, you cannot get around the topic of containerization: in addition to writing and optimizing Dockerfiles, I have an experience in deploying systems with Docker inside [LXC](https://linuxcontainers.org/)-containers with restricted rights (oh, those wonderful multi-admin situations).

As for [systemd](https://systemd.io/): I have a little experience in writing units, no allergies.

# FreeBSD, OpenBSD

Some time ago I was interested in the BSD world.

[FreeBSD](https://www.freebsd.org/): quite a viable option for any task (even [Wayland](https://wayland.freedesktop.org/) is working... somewhat), and it's interesting to follow the development of FreeBSD's answer to Docker Hub: [Bastille](https://bastillebsd.org/). However, the rationale for using FreeBSD in production systems today is not so clear.

[OpenBSD](https://www.openbsd.org/): A perfect example of a well-documented and well-thought-out system (no kidding). It's unfortunate that, due to eternal problems with real hardware and an experimental status of kernel-level virtualization ([vmm](http://man.openbsd.org/vmm.4) - Theo gaved up), the prospects for the applicability of this system are even more vague than FreeBSD.

Nevertheless, I acquired love and respect for [ZFS](https://en.wikipedia.org/wiki/ZFS) from this experience, which is quite reliably ported to Linux ([OpenZFS](https://openzfs.org/wiki/Main_Page)). Better than native [Btrfs](https://btrfs.wiki.kernel.org/index.php/Main_Page) for sure.

# Shell Scripting

Despite the fact that Python can be found on almost any machine now (especially when Python is the main working language in your company), sometimes it is much easier and faster to glue together separate programs using shell scripts. Usually, I write scripts using bashisms, but depending on the task (Debian-based system on the server, busybox-based image...), I can write in a `POSIX sh`-compatible form as well.

# RTOS

In the field of embedded systems, I have an experience in real-time operating system development using C++, as well as experience with FreeRTOS. RTOS in C++ is used in UAV autopilot, FreeRTOS is used in power converters. See also the [C++](/skills/cpp/) section.

___
# Illustration

- Composition: O'Reilly book covers before rebranding. This illustration is inspired primarily by Arnold Robbins' books on [sed & awk](https://www.amazon.com/sed-awk-Dale-Dougherty/dp/1565922255/), two primary tools for shell scripts, and just [awk](https://www.amazon.com/Effective-awk-Programming-Universal-Processing/dp/1491904615/), which could be a good scripting language, if it wouldn't force (unlike Lua) a global variable visibility.

- Green plant: the Linux programming must-have by [Michael Kerrisk](https://www.amazon.com/Linux-Programming-Interface-System-Handbook/dp/1593272200/). I can't say that I know this book by heart, but I regularly refer to it when I am interested in something about the internals of Linux. The **POSIX** subtitle is also in the colors of this book's cover.

- Blue lambdas and red sphere with horns: [NixOS](https://nixos.org/) and [FreeBSD](https://www.freebsd.org/) logos respectively.
