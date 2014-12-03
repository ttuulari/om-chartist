#Om component for chartist.js charts

##Arguments
You need to pass to your component two input arguments:

1. Input data
Input data must be a map with :labels and :series keys.

2. Options
Om component options (with :opts key) must be a map, having the keys
  :constructor – The Chartist chart constructor, e.g. (.-Line js/Chartist)
  :js – javascript attributes of the chart
  :graph-opts – See http://gionkunz.github.io/chartist-js/api-documentation.html
  :responsive-opts – See http://gionkunz.github.io/chartist-js/api-documentation.html


##Usage example
`
(def input-data
     {:labels   ['Mon' 'Tue' 'Wed' 'Thu' 'Fri']
      :series   [[1 2 3 4 5]]})

(om/build graph-view
  input-data
  {:opts
    {:constructor (.-Line js/Chartist)
     :js          {:className   "ct-chart"}
     :graph-opts  {:width 500
                   :height 300}}})
`


