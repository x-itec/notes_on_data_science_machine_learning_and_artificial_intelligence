Title: Convert Strings To Objects
Slug: convert-strings-to-objects
Summary: Convert Strings To Objects
Date: 2016-05-01 12:00
Category: R Stats
Tags: Basics
Authors: Chris Albon

Want to learn more? I recommend working through: [R for Data Science](http://amzn.to/2myxnhi), [R Cookbook](http://amzn.to/2lF6hkb), and [R Graphics Cookbook](http://amzn.to/2m0fcPL).


```R
# Create a vector of strings
name <- c("John", "Jason", "Sarah")
```


```R
# Create a variable from the first element of the "name" variable, called that element's string and give that variable from values.
assign(name[1], c(23,24,33,46,65,86))
```


```R
# Display the variable "John"
John
```




    [1] 23 24 33 46 65 86
