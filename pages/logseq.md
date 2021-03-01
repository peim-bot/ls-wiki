---
title: Logseq
tags: tool
---

## 自定义查询，字符串变量要全部转成小写
## 使用 ``
#+BEGIN_QUERY
{:title "All block about tool"
 :query [:find (pull ?b [*])
  :where
  [?t :page/name "tool"]
  [?p :page/tags ?t]
  [?p :page/name ?name]
  [?b :block/page ?p]
  [(missing? $ ?b :block/pre-block?)]
]
}
#+END_QUERY
## 使用的技术
- 快捷键绑定：[Mousetrap - Keyboard shortcuts in Javascript](https://craig.is/killing/mice)
- 浏览器内存数据库：[[datascript]]
  [tonsky/datascript: Immutable database and Datalog query engine for Clojure, ClojureScript and JS](https://github.com/tonsky/datascript)
