---
date: '2026-02-08T14:22:57Z'
draft: false
title: 'Flags vs Options'
tags: 
  - 
cascade:
  type: blog
  params:
    reversePagination: false 
authors:
  - name: "Abid"
    image: "/images/hrabid.jpg"
    link: ""
comments: true
featured: true
summary: "As command line folks we often face flag and option. Let's demestify the differences."
---

## _Flags_
Flags are work like boolean value. By adding a flag, a feature is enabled or disabled.

**Flags don't take any value**,
**Flags Usually a single letter**

Like `-a` flag with `ls` command lists all files & directories including hidden ones. `-a` enables the feature of listing hidden files & directories.

## _Options_
Basically options are long (can be short sometime). Generally Options take a value & change the behaviour of command according to the value.

**Option takes a value**,
**Option Usually long form**

```shell
fzf --preview='cat {}'
```

The `--preview` option take `cat` as value and change behaviour accordingly.

