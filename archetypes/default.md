---
date: "{{ .Date }}"
draft: true
title: '{{ replace .File.ContentBaseName "-" " " | title }}'
tags:
  -
cascade:
  type: # docs | blog
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
