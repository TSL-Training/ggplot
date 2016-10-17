---
layout: page
title: Setup
permalink: /setup/
---
You need to install the following stuff for this lesson 

1. R
2. RStudio
3. Some R packages: _ggplot2_, _ddply_, _psych_, _effsize_, _bioconductor_ and _ggtree_
4. You will need to download these files and save them to somewhere on your computer: [example_ros_data_flg22.xlsx](../files/example_ros_data_flg22.xlsx), [pinf_mtDNA.newick](../files/pinf_mtDNA.newick) 


## Installing R
Follow this link and install the right version for your operating system [https://www.stats.bris.ac.uk/R/](https://www.stats.bris.ac.uk/R/)

## Installing RStudio
Follow this link and install the right version for your operating system [https://www.rstudio.com/products/rstudio/download/](https://www.rstudio.com/products/rstudio/download/)

## Installing R packages in RStudio.


### Standard packages
For _ggplot2_, _ddply_, _psych_ and _effsize_ start RStudio and use the `Packages` tab in lower right panel. Click the install button (top left of the panel) and enter the package name, then click install as in this picture

![Installing Packages](../fig/package_install.png)

### Bioconductor
For the _Bioconductor_ and _ggtree_ package, first install _bioconductor_ using its special script. 

1. Copy and paste this into the RStudio 'Console' panel on the bottom left. `source("https://bioconductor.org/biocLite.R")`. Press enter. 
2. Copy and paste this into the 'Console' panel: `biocLite()`. 
3. Wait (go for a tea-break, this bit takes ages).
3. Copy and paste this into the 'Console' panel: `biocLite("ggtree")`
