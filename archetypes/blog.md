---
date: "{{ .Date }}"
draft: true
title: '{{ replace .File.ContentBaseName "-" " " | title }}'
tags:
  -
cascade:
  type: blog
  params:
    reversePagination: false
authors:
  - name: ""
    image: ""
    link: ""
summary:
featured:
comments: true
image: ""
---
