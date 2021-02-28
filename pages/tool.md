---
title: 工具
alias: tool
---
##
#+BEGIN_QUERY
{:title "All pages have a *programming* tag"
 :query [:find (pull ?p [*]) :where [?p :page/tags ?t] [?t :page/name ?tag] [(contains? #{"tool"} ?tag)]]
 :inputs ["tool"]
 :view (fn [result]
         [:div.flex.flex-col
          (for [page result]
            [:a {:href (str "/page/" page)} (clojure.string/capitalize page)])])}
#+END_QUERY
