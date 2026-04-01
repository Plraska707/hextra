---
title: ISO su USB
type: docs
weight: 9
---

Per scrivere una ISO su una penna USB così da lanciare un OS da pennetta, il comando è:

`dd if=linux_distro.iso of=/dev/sdX bs=4M status=progress`
