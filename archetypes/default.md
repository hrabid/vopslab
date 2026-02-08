---
date: '{{ .Date }}'
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
comments: true
featured: 
summary:
---
