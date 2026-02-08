---
date: '2026-02-08T14:48:23Z'
draft: false
title: 'Content Addressed Storage'
tags: 
  - git
  - cas
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
summary: "Content Addressed Storage or CAS in short is used to store git objects, let's understand what it is?"
---

## Content-Addressed Storage(CAS)

In traditional Data Storage System files are rely on Hierarchical file system or location based Addresses. 

In Content-Addressed Storage or CAS Data is Addressed based on their Contents rather than the location. 
- Every data is assigned a unique identifier (in this case a SHA-1 Hash __ Basically a 40-character hexadecimal storage)
- The Hash Value is derived from the contents of the file means any altercation in content changes the hash Value( the unique identifier)

## Facilities of CAS
### Data Integrity & Security 
Since the Hash value or unique identifier is derived from the Contents of the data or file, any altercation or changes are easily detected. 

### Efficient Retrieval
No Complex file path needed, just referring to the unique identifier or hash value is enough for data retrieval.

### Use Case 
- Achieving data backup in CDNs
- In Git for storing objects.

