---
title: 工具
alias: tool
---
##
#+BEGIN_QUERY
{:title "All block about tool"
 :query [:find (pull ?b [*])
  :where
  [?t :page/name "tool"]
  [?p :page/tags ?t]
  [?p :page/name ?name]
  [?b :block/page ?p]
]
 :inputs ["tool"]
 :view (fn [result]
         [:div.flex.flex-col
          (for [page result]
            [:a {:href (str "/page/" page)} (clojure.string/capitalize page)])])}
#+END_QUERY
