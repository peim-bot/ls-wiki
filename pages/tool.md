---
title: 工具
alias: tool
---
## {{query (page-tags tool)}}
##
#+BEGIN_QUERY
#+BEGIN_QUERY
{:title "All tasks"
 :query [:find (pull ?b [*])
         :where
         [?b :block/marker ?m]
         [(not= ?m "nil")]]}
#+END_QUERY
#+END_QUERY
