Title: Density Curve Plot
Slug: density-plot
Summary: Density Curve Plot
Date: 2016-05-01 12:00
Category: R Stats
Tags: Data Visualization
Authors: Chris Albon

Want to learn more? I recommend working through: [R for Data Science](http://amzn.to/2myxnhi), [R Cookbook](http://amzn.to/2lF6hkb), and [R Graphics Cookbook](http://amzn.to/2m0fcPL).

```R
# load the gcookbook package for the data
library(gcookbook)

# load the ggplot2 package
library(ggplot2)

# reset the graphing device
dev.off()
```




    null device
              1




```R
# create the ggplot2 data for the faithful$waiting variable
ggplot(faithful, aes(x=waiting)) +
  # add a sensity line
  geom_line(stat="density") +
  # zoom out the plot a little bit
  expand_limits(y=0)
```









![png]({filename}/images/density-plot_files/density-plot_2_1.png)



```R
# create the ggplot2 data for three lines of different levels of smoothing
ggplot(faithful, aes(x=waiting)) +
  # "adjust" determines the level of smoothing, larger the number, the more smoothing
  geom_line(stat="density", adjust=.25, colour="red") +
  geom_line(stat="density") +
  geom_line(stat="density", adjust=2, colour="blue")
```









![png]({filename}/images/density-plot_files/density-plot_3_1.png)
