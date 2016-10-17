---
layout: lesson
---
The primary purpose of this lesson is to show you how to create clear and informative plots in the R package _ggplot_. We will look at how _ggplot_ is structured, how to prepare datasets for use in _ggplot_ and how to customise plots. We will develop plots in R Markdown documents to aid reproducibility and re-use of plots. We will briefly look at the accessory _ggtree_ package for phylogenetic trees and at some standard R stats functions.  



> ## Prerequisites
>
> No specific knowledge prerequisites for this lesson but it will help if you are familiar with some common statistical tests, `t`, `ANOVA` and regression for the later parts.
> You will also find a knowledge of how to write computer file paths helpful.
>
> You need to install the following stuff for this lesson: 
>
> 1. R
> 2. RStudio
> 3. Some R packages: _ggplot2_, _ddply_, _psych_, _effsize_, _bioconductor_ and _ggtree_
> 4. You will need to download these files and save them to somewhere on your computer: [example_ros_data_flg22.xlsx](../files/example_ros_data_flg22.xlsx), [pinf_mtDNA.newick](../files/pinf_mtDNA.newick) 
{: .prereq}

>## Installing R
>Follow this link and install the right version for your operating system [https://www.stats.bris.ac.uk/R/](https://www.stats.bris.ac.uk/R/)
{: .callout}

>## Installing RStudio
>Follow this link and install the right version for your operating system [https://www.rstudio.com/products/rstudio/download/](https://www.rstudio.com/products/rstudio/download/)
{: .callout}

>## Installing R packages in RStudio.
>### Standard packages
>For _ggplot2_, _ddply_, _psych_ and _effsize_ start RStudio and use the `Packages` tab in lower right panel. Click the install button (top left of the panel) and enter the package name, then click install as in this picture
>
>![Installing Packages](../fig/package_install.png)
>
>### Bioconductor
>For the _Bioconductor_ and _ggtree_ package, first install _bioconductor_ using its special script. 
>
>1. Copy and paste this into the RStudio 'Console' panel on the bottom left. `source("https://bioconductor.org/biocLite.R")`. Press enter. 
>2. Copy and paste this into the 'Console' panel: `biocLite()`. 
>3. Wait (go for a tea-break, this bit takes ages).
>3. Copy and paste this into the 'Console' panel: `biocLite("ggtree")`
{: .callout}
