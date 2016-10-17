---
title: "Motivation"
teaching: 10
exercises: 0
questions:
- "Why should I care about clear data visualisations?"
objectives:
- "Explain how certain plots can obscure patterns in data."
- "Explain how data visualisation and exploration can provide more clarity and understanding."
keypoints:
- "Common plot types obscure experimental variation."
- "Clarity comes from carefully choosing plot type."
---


## Variability in measurements

Variability in measurements is a thing that happens as a natural consequence of working with complex systems that are affected by many variables in stochastic ways. Biological systems are some of the most variable we know. The variability could be a function of the behaviour of the system yet it is common practice to hide that variability when we start to analyse our data by using summary plots like box-plots.  Ultimately, that's bad news for our science, because the variability could be telling us something.


## Summarising your data can lead to wrong conclusions

We all know that when you create a bar chart and put some error bars on it, you're really only representing two numbers, usually a mean and standard deviation. People create bar plots instinctively, and in doing so can miss important stuff. Look at this figure:  

![Weissgerber et al](http://journals.plos.org/plosbiology/article/figure/image?size=large&id=info:doi/10.1371/journal.pbio.1002128.g001)
_source:_ [Weissgerber et al ](http://journals.plos.org/plosbiology/article/figure/image?size=large&id=info:doi/10.1371/journal.pbio.1002128.g001) 	

The bar chart in panel A is one that came out of all those sets of numbers in the other panels. But it really hides some important stuff, like the fact the numbers are clearly separating into two groups in panel D, or that the two samples have different sizes in panel E.

Worse than any of these is that the significant difference in the t-test is coming from just one point in panel C. From this data set you might be tempted to conclude that there is a significant difference in the two samples and if you relied on the bar chart as a visualisation then you'd never suspect there was something funny.  

Some enthusiastic young science communicators have even started a Kickstarter to lobby journals to stop using, in particular, bar charts! These people, calling themselves Bar Barplots, have a nice video on one of the main problems with  bar charts.

<video controls >
	<source src="https://ksr-video.imgix.net/projects/2453455/video-665338-h264_high.mp4" type="video/mp4">
		Your browser does not support the video tag
</video>


_source:_ [Kickstarter - Barbarplots](https://www.kickstarter.com/projects/1474588473/barbarplots)

So ignoring your data visualisation and just making bar plots could be an error! It's important that you spend a little time getting to know, and presenting your data as clearly and thoroughly as possible. 


## _ggplot2_ An R package for beautiful visualisations

In this tutorial we are going to use _ggplot2_ to make some clear, informative, thorough visualisations. Here's an example:

![ggplot 2 iris data](http://dl.dropbox.com/u/10506/blog/r/ggplot2/sepal-vs-petal-specied.png)

_ggplot2_ is a library in the R statistical programming language - but we won't be learning to program here. The _gg_ part stands for 'grammar of graphics', _ggplot2_ is a small grammar that describes plots that should be built on top of data - effectively allowing a user to write their own plot description and have the computer work out what to do.
