---
title: 工具
alias: tool
---
###
#+BEGIN_QUERY
{:title "All block about tool"
 :query [:find (pull ?b [*])
  :where
  [?t :page/name "tool"]
  [?p :page/tags ?t]
  [?p :page/name ?name]
  [?b :block/page ?p]
  [?b :block/pre-block? "nil"]
]
}
#+END_QUERY
