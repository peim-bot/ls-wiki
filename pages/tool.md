---
title: 工具
alias: tool
---
###
#+BEGIN_QUERY
{:title "All block about tool"
 :query [:find ?p
  :where
  [?t :page/name "tool"]
  [?p :page/tags ?t]
  [?p :page/name ?name]
  [?b :block/page ?p]
]
}
#+END_QUERY
