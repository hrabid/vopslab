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
featured:
comments: true
image: ""
summary:
---
