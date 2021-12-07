# Comparing groups

![​​Age at death distributions for Finnish males and females](https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LPB0-GYwxbJd7xOS0FD%2Fuploads%2F40q4PyUzBdojzGivyxok%2Fimage.png?alt=media\&token=449d7db5-0243-45ea-83d2-63a3477f5843)

Picking up where we left off and jumping straight into analysis, from the measures of central tendency depicted above, we can infer that in general, female Finns seem to live quite a bit longer than male Finns, with for example 50% of females living to at least 81 years old (their median age at death), while only 25% of male Finns live that long (3rd quartile). For male Finns, the median age at death is only 73. Further, from the shape of the distribution and the quartiles (25% and 75% equivalents of the 50% median), it can be inferred that the lifespans of Finnish males vary more than those of females. Particularly the first 25% quartile for males is very much to the left of that of females, meaning that a much larger proportion of men die young.

In the case of data describing complete populations, this is basically all there is to comparing them: one may plot the distributions and compare visually, and then verify any insights numerically, by calculating e.g. proportions, averages and variances and comparing them. However, in practice again things get a lot more complicated due to needing to compare groups based on smaller samples.

## Uncertainty in comparing groups based on samples

In the above for the complete distribution, we could know for sure that the difference in proportions of females and males surviving to 81 is 25 percentage points, and that the difference between the median age for females and males is 8 years, and the difference in mean ages is 8.7 (for evaluating differences, calculating differences in means are often also good, and they have also some benefits in how their sampling error is distributed, as well as in how calculating them makes better use of sparse data. We don't have the space to go into those details, but it is good to know that this is the case).&#x20;

For samples, we have to again include in our assessment the possibility that the differences we observe are caused just by sampling error, when in truth no such difference exists. One way to do this is again through bootstrapping



