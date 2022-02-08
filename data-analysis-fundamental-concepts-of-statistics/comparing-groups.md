# Comparing groups



{% hint style="info" %}
Context note: this is a sub-part of the [fundamental concepts of statistics](./) section of the [computational literacy for humanities and social sciences course](../). You can use this to teach yourself some fundamental concepts of statistics. However, if you want to understand more broadly when you might want to use them, you're better off going through the whole course.
{% endhint %}

![​​Age at death distributions for Finnish males and females](https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LPB0-GYwxbJd7xOS0FD%2Fuploads%2F40q4PyUzBdojzGivyxok%2Fimage.png?alt=media\&token=449d7db5-0243-45ea-83d2-63a3477f5843)

Picking up where we left off and jumping straight into analysis, from the measures of central tendency depicted above, we can calculate that female Finns seem to live quite a bit longer than male Finns, with for example 50% of females living to at least 81 years old (their median age at death), while only 25% of male Finns live that long (3rd quartile). For male Finns, the median age at death is only 73. Further, from the shape of the distribution and the quartiles (25% and 75% equivalents of the 50% median), it can be inferred that the lifespans of Finnish males vary more than those of females. Particularly the first 25% quartile for males is very much to the left of that of females, meaning that a much larger proportion of men die young.

Here, in the case of data describing complete populations, all of the above are facts. The difference in proportions of females and males surviving to 81 is 25 percentage points, and the difference between the median age at death for females and males is 8 years, while the difference in mean age at death is 8.7 years (for evaluating differences, means often work as well as medians, and they have also some benefits in how their sampling error is distributed, as well as in how calculating them makes better use of sparse data. We don't have the space to go into those details, but it is good to know that this is the case). However, strictly speaking, this still doesn't give us a definitive answer to whether females live longer than males. For that, we still need to know how unlikely it would be to see such differences just due to random chance in the situation where, in truth, for example the mean ages of death for men and women would not differ.&#x20;

## Significance testing

Restated, to really be certain that there is a difference between for example the median age of death for women and men, we need to disprove the alternate neutral explanation for the observed difference, where the true median age of death for men and women would actually be the same, and the observed difference we are seeing would be caused purely by random variation in how long individual people live, which has just happened to cluster so that women have lived longer.

To rule out this alternative explanation (often called the null hypothesis), we will calculate how unlikely it would be that if it were true, we'd see as big a difference as we're really seeing. While there are many standard statistical formulas for calculating this, often they only work for normal distributions or have other limitations. A nice non-committal approach to this problem are permutation tests, which, similarly to bootstrap methods, rely on resampling the data we have. In essence, what we do here is put all our data into a single pool, and then randomly split the pool into "female" and "male" parts in the same proportion as in our actual data. This way, no inherent structure between the two groups remain, and instead any difference we measure between their medians is caused by pure random chance.&#x20;

Doing this for example 10 000 times, we get a distribution of the random variation. Then, we can see how large a portion of this distribution we need to include before our measured difference is included in it.&#x20;

Doing so for our complete data which is huge, we easily come to the conclusion that the difference between the median age of men and women is real. In 10 000 random shuffles of the original data, the largest mean difference that randomly appeared was 0.09 years. Extrapolating from the normally distributed errors, the chance that a difference of 8.7 would randomly appear is one to a number with 27 212 zeros (a trillion has 12 zeros).&#x20;

As an aside, such is the law of large numbers - with this data, even a difference of 0.05 years in either direction would show up as statistically significant at the 5% cutoff often used (and stated p<0.05), meaning that with this data, in less than 5% of cases would random variation cause a difference in group means of at least 0.05 years. On the other hand, what would a difference in mean age at death of 0.05 years mean in practice? Particularly if that was the only thing we know, and did not know whether the distributions giving rise to that mean looked otherwise different? The important takeaway from this is that a difference being statistically significant means nothing in itself, without a deeper understanding of the size of the difference, as well as what aspects of the overall phenomenon the comparison (often of means) might miss completely.

While in this instance due to the size of the difference and the size of the data, testing for significance yielded a foregone conclusion, when looking at either smaller differences or smaller datasets, ensuring the difference cannot be caused by just random chance is important.

## Uncertainty in comparing groups based on samples

While significance testing is appropriate for even complete sets of data, trying to discern differences from samples adds the complexity of random variation caused by sampling errors. Thus, here one often wants to both 1) calculate a confidence interval for the quantity of interest (e.g. the difference in means), which will account for sampling variation, as well as 2) do a test for significance, which will tell whether the difference might have been caused just by chance.

To give some examples of this in practice, we will use the following historic sample of ages at death, derived from metadata of the [Corpus of Early English Correspondence](http://www.helsinki.fi/varieng/CoRD/corpora/CEEC/index.html):

![Ages at death for various groups in the CEEC metadata](../.gitbook/assets/668e82f8-363c-4123-ab7f-baa9d9368890.png)

Here, on the whole, we have age at death data for only 415 individuals, further unevenly distributed between groups as follows:

<table><thead><tr><th>Century</th><th>Sex</th><th>Rank</th><th data-type="number">Number of ages at death</th></tr></thead><tbody><tr><td>1500</td><td>Male</td><td>Clergy</td><td>35</td></tr><tr><td>1700</td><td>Male</td><td>Clergy</td><td>37</td></tr><tr><td>1500</td><td>Male</td><td>Nobility</td><td>159</td></tr><tr><td>1700</td><td>Male</td><td>Nobility</td><td>100</td></tr><tr><td>1500</td><td>Female</td><td>Nobility</td><td>41</td></tr><tr><td>1700</td><td>Female</td><td>Nobility</td><td>43</td></tr></tbody></table>

As can be seen from the distribution plots, this data is quite spotty. To get a slightly better overview of it, we can group the ages into decades:

![Ages at death for various groups in the CEEC metadata grouped by decade and overlaid with mean ages at death](../.gitbook/assets/edac5e92-7c3c-4b62-b78d-72fa5f00225f.png)

Wanting to compare like with like, let us start with seeing whether male clergy or nobles lived longer in the 18th century. In our sample, 18th-century clergymen outlive 18th-century nobles on average by 1.7 years. However, conducting a permutation test for significance, we come up with the following breadth of random variation in the case where no actual difference would exist:

![Distribution of random differences in means for the 18h century males in case of no difference between nobles and clergy](../.gitbook/assets/d2fb5d6b-a4a7-41a8-9489-f685ede4c69d.png)

As can be seen from this distribution, a difference of 1.7 in either direction would not be unexpected at all. In fact, a full 50% of the differences in random samples from the unified population are either below -1.7 or above 1.7. Therefore, we must conclude that we have no evidence for clergymen living longer than nobles in the 18th century.&#x20;

However, if we do the same comparison for male nobles and clergy in the 16th century, where the difference in means is 5.29 years to the advantage of clergymen, we see the following distribution for differences in means for the null hypothesis:

![Distribution of random differences in means for the 16h century males in case of no difference between nobles and clergy](../.gitbook/assets/9103681d-4739-4423-93ff-b41b226eda20.png)

Here, the observed difference of 5.29 years is so far to the right of the distribution of random differences that only 3% of the random differences are more than 5.29 years in either direction. Therefore, at the significance level of p<0.05, we can conclude that the difference isn't likely to arise just from random effects.

However, while we now know that the difference is statistically significant, we still don't know how large it is. 5.29 years is just our estimate from our sample. To get the probable range of the difference, we can construct confidence intervals for it. Through bootstrapping, we come up with the following probability distribution for the difference:

![Bootstrap probability distribution for the differnece in means for the 16th century males](../.gitbook/assets/c2c8c52a-bd2f-4d1d-976f-022069a2edf5.png)

Shaded is the area where 95% of the estimates appear, which translates to a 95% confidence interval of \[0.45,9.86], meaning that we're quite certain that 16th-century mare clergy outlived their noble counterparts on average by somewhere between one half and ten years.

Continuing our comparisons, for either the 16th or the 18th century, we find no statistically significant difference between the lifespans of female and male nobles (the observed differences are 1.09 years and 2.42 years, which happen 68% and 34% of the time in random samples).

However, pooling our data and comparing across centuries, we do find a significant increase in lifespan in the 18th century as compared to the 16th. In our sample, on average our 18th-century people live 5.32 years longer than their 16th-century counterparts. For the larger size of our pooled sample, this difference has a 1 in 10 000 chance of arising through pure chance and is therefore highly statistically significant. The 95% confidence interval for the size of this increase is from two and a half years to 8 years, while it is 50% likely to be between 4.5 and 6.5 years.

{% hint style="info" %}
Assignment

To further add to your understanding of statistical significance and p-values, have a look at this [interactive visualization](https://rpsychologist.com/pvalue/).&#x20;

1. Here, Cohen's d is essentially a normalized number representing the size of the difference in means between two groups, both of which here have equal variance. First, to get an understanding of this, drag around the d-slider a bit. and look at the second graph on the page.&#x20;
2. Leaving the d-slider at whatever point, click on +1 under "Draw samples" a couple of times. The visualization shows drawing a 5 observation sample from the true distribution (the blue graph) and summarizing this as a sample mean. This sample mean then falls down as a singular data point into the second graph.
3. Now, click on +500 under "Draw samples". You will end up with a little bit over 500 mean values calculated from +500 experiments, and you can see that they are spread in an approximately normal fashion around the true population mean for group 1 at μ1.&#x20;
4. Now, unless you dragged the d-slider very far to the right (meaning a very large difference existing between the groups), it is quite likely that a large number of the sample means from the +500 experiments lies within the central 95% (the area delimited by the dotted lines, with sample means falling into this region coloured in grey) of random variation around the population mean for group 0 at 100 (the solid black line). For example, for a true population mean of 110 for group 1, a full 68% of the sample means are within this central 95% region. Interpreted, what this means is that even if the difference of 10 was real, 68% of the time if we did this experiment (sampling 5 people and calculating their mean), we'd be unable to claim that any difference exists.
5. To get a better understanding of this, drag the d-slider again back and forth, and look at the text under "Power Analysis" to see how often you'd be able to reject the null hypothesis and state that a difference does actually exist for various true differences.
6. Now, for the default value of just 5 observations in a sample, the situation is not rosy at all for even quite large differences. To fix this, click multiple times on the + -icon under "Observations per sample". Notice how, if you increase the sample size to even just 25, your chance of confirming the significance of a difference in means increases considerably (for all possible differences). (And finally, recall that vice-versa, for very large samples, even a miniscule difference will show up as statistically significant. Therefore, statistical significance must always be just one part of the equation, with another being to evaluate the meaningfulness of the possible effect sizes estimated = evaluating whether a true difference in means of the size indicated as likely by the confidence intervals calculated actually affects anything in practice)
{% endhint %}

### On doing multiple comparisons

There is one final thing about hypothesis tests that bears mentioning, and that is the need to guard against the increasing probability to obtain at least one statistically significant result even from data where no differences really exist in case one is testing for multiple hypotheses.

Hypothesis tests guard against drawing false conclusions from data. If from a hypothesis test of difference, one gets a p<0.05 result, one can safely say that as large a difference as was measured has a chance of appearing at most 5 times purely due to chance if a) in reality there is no difference and b) the experiment was repeated a 100 times. Turned around, if there really was no difference, in taking 100 random samples from the population, in at least 95 of those samples, the difference measured would be lower than the one we now observed. Often, this is considered an adequate level of certainty to claim that the difference is real.&#x20;

However, what happens if we use the same data to test multiple hypotheses? Here, the laws of combining probabilities work against us. For example, if the probability of not observing at least a given difference by chance in any of the tests would be precisely 95%, in conducting multiple tests, the chance that none of them would show such a difference would be 95% to the nth power. For example, conducting just five tests on a population where no actual difference exists, the chance that none of the five tests yields a statistically significant result at p<0.05 is 0.95⁵≅77%. For fourteen tests, the chance that none of the tests yields a statistically significant result at p<0.05 is 0.95¹⁴≅49%. Turned around, if you conduct fourteen tests of significance on your data, you may have a more than 50% chance of at least one of your tests coming back with a statistically significant result, even if you conduct each test at the p<0.05 or 95% confidence level! Below, this problem is depicted in an instance of the XKCD comic:

![XKCD 882 "Significant"](<../.gitbook/assets/image (48).png>)

Take home message: in order to do multiple comparisons in a trustworthy manner, one must apply further statistical methods to [control](https://en.wikipedia.org/wiki/Multiple\_comparisons\_problem#Controlling\_procedures) for these problems.
