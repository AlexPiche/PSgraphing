# PSgraphing

##Installation

```R
install.packages('devtools') 
library(devtools)
install_github('AlexPiche/PSgraphing')
```

If you run into trouble installing “devtools” look at: https://github.com/hadley/devtools

##Minimal Example

```R
library(PSgraphing)
data(PSgraphing)
PSgraphing(count=Count_data3, estimate=Estimate_RR, text='(total n range: 3237 to 3245 per decile)', name='myPSgraph.pdf')
```

##TODO

* Use propensity package to generate count data from raw data.
* Options to add:
  * which estimate RR, OR, RD -> don't forget the scale e.g. log or linear
  * type of graphs: % events exposed
  * which annotation do we want on the graph
* Other modifications:
  * add propensity score decile to count data to be sure that they are not upside down
  * estimate C.I.
  * meta analysis estimate: $ \tau, I^2 $
  * range i.e. [min(n.e.+n.c.), max(n.e.+n.c.)]
