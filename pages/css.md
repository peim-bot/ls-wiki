---
title: CSS
tags: 前端
published: false
permalink: css
---

- 多行省略号
  ```CSS
  .text {
    overflow: hidden;
    text-overflow: ellipsis;
    display: -webkit-box;
    -webkit-line-clamp: 2;
    -webkit-box-orient: vertical;
  }
  ```