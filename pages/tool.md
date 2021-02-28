---
title: 工具
alias: tool
---
## {{query (page-tags tool)}}
##
#+BEGIN_QUERY
{:title "All pages have a *programming* tag"
 :query [:find ?name
         :in $ ?tag
         :where
         [?t :tag/name ?tag]
         [?p :page/tags ?t]
         [?p :page/name ?name]]
 :inputs ["tool"]
}
#+END_QUERY
## [[工具]]
