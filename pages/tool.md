---
title: 工具
alias: tool
---
## {{query (page-tags tool)}}
##
#+BEGIN_QUERY
{:title "All tool block"
 :query ?b
         :where
         [?tid :tag/name "tool"]
         [?pid :page/tags ?tid]
         [?b :block/page ?pid]]}
#+END_QUERY
## [[工具]]
