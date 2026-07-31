---
date: "2026-07-31T06:32:40+06:00"
draft: false
title: "Linux Plymouth Boot Screen"
tags:
  - linux
  - boot-screen
  - plymouth
cascade:
  type: blog # docs | blog
  params:
    reversePagination: false
authors:
  - name: "Abid"
    image: "/images/hrabid.jpg"
    link: "https://github.com/hrabid"
featured: true
comments: true
image: "images/plymouth.png"
summary: Fancy Animation on linux startup
---

![](/images/plymouth.png)

# `plymouth` configuration

## installtion

```bash
sudo pacman -S plymouth cantarell-fonts ttf-dejavu
```

## configuring `mkinitcpio`

Edit the `/etc/mkinitcpio.conf`

```conf
...
MODULES=(i915)
...
HOOKS=(base systemd plymouth autodetect microcode modconf kms keyboard sd-vconsole block filesystems fsck)
...
```

Rebuild `mkinitcpio`

```bash
sudo mkinitcpio -P
```

## configure `kms`

edit `MODULES=()` in `/etc/mkinitcpio.conf`

```conf
MODULES=(i915) # for intel
MODULES=(amdgpu) # for amd
MODULES=(nvidia nvidia_modeset nvidia_uvm nvidia_drm) # for nvidia
```

Rebuild `mkinitcpio`

```bash
sudo mkinitcpio -P
```

See the preparation section of this article for more info: https://wiki.archlinux.org/title/Plymouth

## configure kernel parameters

add this line in `/etc/kernel/cmdline`

```cmdline
root=UUID=YOUR-ROOT-UUID rw quiet splash loglevel=3 rd.udev.log_level=3 vt.global_cursor_default=0
```

Rebuild `mkinitcpio `

```bash
sudo mkinitcpio -P
```

## set up the `plymouth` theme of you choice

```bash
sudo plymouth-set-default-theme -l # list themes

sudo plymouth-set-default-theme -R lone
```

more `plymouth` themes can be installed from `aur` or this repo: https://github.com/adi1090x/plymouth-themes

Refs:

- https://github.com/adi1090x/plymouth-themes
- https://wiki.archlinux.org/title/Plymouth
- https://xdaforums.com/t/bootanimations-collection.3721978/
