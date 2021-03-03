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
         [(missing? $ ?b :block/pre-block?)]]
 :collapsed? true
}
#+END_QUERY
###
