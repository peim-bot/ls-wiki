---
title: 工具
alias: tool
---
## {{query (page-tags tool)}}
##
#+BEGIN_QUERY
{:title "All tool block"
 :query [:find (pull ?b [*])
         :where
         [? pa]
         [(not= ?m "nil")]]}
#+END_QUERY
## [[工具]]
