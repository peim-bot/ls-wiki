---
title: Babel
tags: 前端
---

- babel-plugin-bulk-import 插件
  用于批量 import，语法类似[[glob]]
  ```
  import * as Features from './features/*.js'
  /* Features would be
      {
          featureA: {feature: 'A'}, // featureA.js
          featureB: {feature: 'B'} // featureB.js
      }
  */
  ```