---
title: 工具
alias: tool
---
##
#+BEGIN_QUERY
{:title "All block about tool"
 :query [:find ?name
         :in $ ?tag
         :where
         [?t :page/name ?tag]
         [?p :page/tags ?t]
         [?p :page/name ?name]]
 :inputs ["tool"]
 :view (fn [result]
         [:div.flex.flex-col
          (for [page result]
            [:a {:href (str "/page/" page)} (clojure.string/capitalize page)])])}
#+END_QUERY
