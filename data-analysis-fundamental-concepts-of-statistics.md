# Data analysis: fundamental concepts of statistics

{% hint style="danger" %}
This content is not yet complete. In the meantime, see this presentation: [Data analysis: fundamental concepts of statistics](https://docs.google.com/presentation/d/e/2PACX-1vR7OYZauaLDOFf3M2ACynBcW77Ezx7SDSh5heLEzxOdc0ExMujU5t7GpksgdHpXbQKE9mpYPxlWT6c-/pub?start=false\&loop=false\&delayms=3000) ([pdf](http://docs.google.com/presentation/d/1LYYXZJ3WOHCThv\_i4fA\_anx\_s0LkYxFQ0wzJpC8KaSk/export/pdf), [gd](https://docs.google.com/presentation/d/1LYYXZJ3WOHCThv\_i4fA\_anx\_s0LkYxFQ0wzJpC8KaSk/edit?usp=sharing))
{% endhint %}

Statistics is about:

1. Understanding and describing groups
2. Comparing groups
3. Understanding relationships

Let's tackle these in turn:

## Understanding and describing groups

Consider [this dataset](https://pxnet2.stat.fi/PXWeb/pxweb/en/StatFin/StatFin\_\_vrm\_\_kuol/statfin\_kuol\_pxt\_12ag.px/) of the age at death of the two million Finns (2 027 385 to be exact) who died between 1980 to 2020. While aggregated in the original, the data essentially contains the following information:

<table><thead><tr><th>Sex</th><th data-type="number">Year of death</th><th data-type="number">Age at death</th></tr></thead><tbody><tr><td>Male</td><td>1980</td><td>86</td></tr><tr><td>Male</td><td>1980</td><td>76</td></tr><tr><td>Male</td><td>1980</td><td>76</td></tr><tr><td>Female</td><td>1980</td><td>75</td></tr><tr><td>Male</td><td>1981</td><td>96</td></tr><tr><td>...</td><td>null</td><td>null</td></tr></tbody></table>

As a table, this tells us information about each individual. Further, we might order the two million rows by for example Age at death to find out the longest-living people for this time period:

<table><thead><tr><th>Sex</th><th data-type="number">Year of death</th><th data-type="number">Age at death</th></tr></thead><tbody><tr><td>Female</td><td>2000</td><td>112</td></tr><tr><td>Female</td><td>2005</td><td>111</td></tr><tr><td>Male</td><td>2009</td><td>111</td></tr><tr><td>Female</td><td>2015</td><td>111</td></tr><tr><td>...</td><td>null</td><td>null</td></tr></tbody></table>

However, what if we want to look at the data as a whole, to see what it tells us about the lifespans of Finns as a whole? For this, we need to turn to statistics. Let us start with a simple visualization that just takes all two million people and plots their ages at death in increasing order:&#x20;

![Ages at death of two million Finns, ordered by age at death](<.gitbook/assets/9795e3a8-c993-4487-a8be-92663c60d479 (1).png>)

While this is not the way these types of data are usually presented, what does this visualization tell us? First, one can read proportions out of it. Because the people are ordered by age at death, looking at the midpoint of the graph (around the 1st millionth person) and looking at the age recorded there (around 77), we can say that 50% of Finns live to be older than 77. This works for any percentage: looking at around 200 000 (10% of 2 000 000) and finding the number 52, we can say that only 10% of Finns die before reaching that age, while looking at 1 800 000, we can conclude that only 10% of Finns live longer than 90 years.&#x20;

This works the other way around as well. For example, looking at age 40 and finding the number 100 000 (5% of 2 000 000), we can say that only 5% of Finns die before reaching 40. If we want to know the proportion of Finns who die between 40 and 80, we look up 80 (at about 1 200 000 or 60% of 2 000 000) and can calculate that 60%-5%(the proportion from 0 to 40)=55 per cent of Finns die in that time period.&#x20;

To make these calculations easier, we can replace the person number with their position in percentage of the dataset. Further, let's switch the X and Y axes with each other. In this format, the ensuing graph has a term associated with it: the empirical cumulative distribution function.

![The empirical cumulative distribution function of our data](<.gitbook/assets/image (17).png>)

So, only 5% of Finns die within the first 40 years of their lives, while 55% die in their next 40. Projecting this information back into the graphs, we can see that in the first graph arranged by people, in the horizontal bands where the graph moves up quickly, there are few people. In the bands where it moves up slowly, there are many more people. In the graph arranged by age at death on the other hand this is reversed. Where the graph moves up slowly, there are few people, and where it moves quick, there are many.&#x20;

While these graphs are good for dividing the data into percentages, from them it is still difficult to get a good idea of when exactly people are likely to die. To get a better overview of this, we need to move from cumulative graphs to ones showing local density. For this, we need to calculate the distribution of the data over the Age at death. What this means is that we take each Age at death, and count how many people die at that age. The resulting table looks like this:

<table><thead><tr><th>Age at death</th><th data-type="number">Number of peoplle</th></tr></thead><tbody><tr><td>112</td><td>1</td></tr><tr><td>111</td><td>3</td></tr><tr><td>110</td><td>6</td></tr><tr><td>109</td><td>10</td></tr><tr><td>...</td><td>null</td></tr></tbody></table>

Plotted visually, this table looks as follows:

![The number of people dying at each age](.gitbook/assets/d1a37eea-94ff-4dc4-a5b4-c88490980c2c.png)

Here, the height of each bar corresponds directly to the number of people dying at that age. This allows immediate look up and comparison of exact ages (e.g. that about 10 000 people died aged 50, while about double that many people died aged 60). Comparing ranges on the other hand now requires comparing the geometric area of the different regions in the graph. This is not something that humans are good at doing accurately, but general notions are still available.&#x20;

For example, from this visualization we can immediately see the following things:

1. Many people die in the first year of their lives
2. After that, there is only a small chance of dying before reaching 30, which seems to be very low between 1-15 and then increase somewhat in the late teen years.
3. After 30, the probability of death slowly increases. The average age at death by natural causes seems to be somewhere around 80 years, but there is a large variation of 10-20 years around that as well.

This last observation takes us to a side path on summary statistics.

### What is average

{% hint style="info" %}
Assignment

Before reading on, consider for a moment what you could infer if you were told that the average height for adult Finns is 173 centimetres? Really - stop for a moment and think what could you intuitively infer from this information.
{% endhint %}

Perhaps you inferred that about half of Finns would be over 173cm tall and half under and that 173cm would itself be the most common height? You'll also have an inbuilt ideation of the variance - that there will probably be quite many people 160cm or 180cm in height, but much fewer people less than 150cm or over 190cm. All of these ideations depend on the fact that [height is normally distributed](https://ourworldindata.org/human-height#height-is-normally-distributed), i.e. the distribution of heights looks something like this:&#x20;

![Height distribution of Finns](.gitbook/assets/dde9c4c1-38de-4420-b0a2-71e2b4265c45.png)

With such data, summing it up in terms of an average value and the breadth of variation around it tells us everything we need to know about the data, and yields our intuitive understanding of what they mean in practice.&#x20;

Note that even when not often explicitly given, an understanding of the breadth of variation is still crucial to be able to draw inferences from data. For example, currently we're more than ten times likely to meet a person who is about 170-180cm in height than to meet someone who is less than 160cm. However, if there was double the amount of variation in how tall people are, we'd only be twice as likely to meet someone between 170-180cm as someone less than 160cm (compare the black and red graphs below):

![The amount of people between 170-180cm as compared to those less than 160cm with the actual height variation](.gitbook/assets/fb2e5d16-82a5-4b77-8a7a-d22b652cdad0.png)

![The amount of people between 170-180cm as compared to those less than 160cm if the variation in heights were double](<.gitbook/assets/image (20).png>)

Okay, before I wrote that usually, our intuition on averages is that that is the most common value, as well as that 50% of values are larger and 50% smaller than the average. Before that, from the distribution plot of ages at death, I wrote that the average age at death by natural causes seemed to be somewhere around 80 years. However, if I calculate the arithmetic mean for the whole data, it turns out to be 73,82 years. And remember, from already the original plot we deduced that half of the people die by age 77, while half live longer. Only by looking at which exact age most people died do we come close to 80, by getting 83 (67 943 people died aged 83). What does this all mean?

It means that **because our age at death data is not completely normally distributed**, there is no longer a single neat average that would sum it up nicely. Instead, we are left with multiple numbers that measure different things. Formally, these are called different measures of central tendency:

* The median of 77 tells us that 50% of people live at least to that age.
* The mode of 83 tells us that that is the most common age of death.
* The arithmetic mean of 73,82 tells us that if we removed all the variation and distributed lifetimes equally, each Finn would live 73,82 years.

When data is normally distributed, all of these measures point to the same number, yielding our intuition of what an average is. However, with non-normally distributed data, none of these measures anymore (even with a measure of variation added) sums up the whole truth of what goes on in the distribution. Below, you will find each of these measures overlaid on top of the original density plot:

![Measures of central tendency and the distribution](.gitbook/assets/c1719449-6a27-4899-9fe2-054965b8c9d7.png)

Interpreted visually, the measures show the following:

* the mean shows the balance point of the distribution. If the distribution were to be hinged upon this point, it would stay level. For this distribution, this means that because there is a large mass of deaths at zero years far away from the bulk of the distribution, the mean is less than the other measures.
* the median shows the point which divides the geometric area of the distribution in half (here showing again how hard it is for people to compare areas of different shapes)
* the mode merely shows the singular point where the distribution is highest. Here this works out well, but the mode is volatile. For example, if the central mass of the distribution was much more spread out and the outlier at zero years was higher, that might end up being the mode of the whole distribution, even if the general shape of it stayed otherwise the same.



## Yie olde stupfh

Population <-> sample & representativeness

Understanding data / understanding patterns: Distribution <-> summarization: average, variability + confidence intervals

Comparing data / are two distributions different?: Statistical tests

Modeling data / understanding relationships: Variables - independent/dependent/control/confounding/mediating/moderating & correlationConsider [this dataset](https://docs.google.com/spreadsheets/d/154ShU7S8ykod5XU7N4zgygZOzXY4ztLCO\_KBD7U6zxI/edit?usp=sharing) describing the gender, lifespans, social ranks, education and number of letters written by a bunch of people (taken from metadata of the [Corpus of Early English Correspondence](http://www.helsinki.fi/varieng/CoRD/corpora/CEEC/index.html)), the first five rows of which are reproduced below:&#x20;

| Name                                | Sex    | Lifespan | Rank         | Education | NumberOfLetters |
| ----------------------------------- | ------ | -------- | ------------ | --------- | --------------- |
| Mary Wortley Montagu née Pierrepont | Female | 73       | Nobility     | High      | 189             |
| JOHN HOLLES                         | Male   | 72       | Nobility     | High      | 136             |
| Samuel Pepys                        | Male   | 70       | Professional | High      | 136             |
| Daniel Fleming                      | Male   | 68       | Gentry       | High      | 122             |
| Walter Ralegh                       | Male   | 64       | Gentry       | High      | 119             |

What can one do with such data? First of all, one can look at the individuals. To see how they compare against each other with regard to all the axes, it may make sense to order or sort the data according to an axis of interest, such as [lifespan](https://docs.google.com/spreadsheets/d/154ShU7S8ykod5XU7N4zgygZOzXY4ztLCO\_KBD7U6zxI/edit#gid=1232246814) or [number of letters](https://docs.google.com/spreadsheets/d/154ShU7S8ykod5XU7N4zgygZOzXY4ztLCO\_KBD7U6zxI/edit#gid=1253333531). One can also visualize the data graphically, similarly ordered by [lifespan ](https://plot.ly/\~jiemakel/39/#/)or [number of letters](https://plot.ly/\~jiemakel/41/#/).

However, what if one is interested in not just individuals, but groups in the data, or alternatively the data as a whole? What can one say about the lifespans, or the number of letters written as a whole in this set of data? Looking at the [lifespan graph](https://plot.ly/\~jiemakel/39/#/) for example, one can say that the highest lifespan in the data is 95, while the lowest is 16. Also by finding the centrepoint of the graph and looking up the lifespan there, it seems that about half of the people live at least 65 years, while about half live less than that. However, from this view it is quite hard to say for example what the most common lifespans are. For this, it helps to _aggregate _the data by lifespan. In practice, this is done by taking all the lifespans appearing in the data, and counting how many times they appear. The result of this calculation is a [new table and visualization](https://docs.google.com/spreadsheets/d/154ShU7S8ykod5XU7N4zgygZOzXY4ztLCO\_KBD7U6zxI/edit#gid=904052074) describing the _distribution _of the lifespans.



* the average height for Finns is 172,74 centimetres
* the average height for Finnish males is 179,59cm
* the average height for Finnish females is 165,89cm

## Archetypes of data from the viewpoint of statistics

* categorical
* ordinal
* numerical / interval (/ ratio)
  * continuous, discrete

|   |   |   |   |   |
| - | - | - | - | - |
|   |   |   |   |   |

## Terminology: representativeness

“The British National Corpus (BNC) is a 100 million word collection of samples of written and spoken language from a wide range of sources, designed to represent a wide cross-section of British English, both spoken and written, from the late twentieth century.”

* 90% written, 10% speech
* Written:&#x20;
  * 70-80% informative, 20-30% imaginative
  * 60% books, 30% periodicals, 10% miscellaneous
  * Informative: 5% natural and pure science, 5% applied science, 15% social and community, 15% world and current affairs, 10% commerce and finance, 10% arts, 5% belief and thought, 10% leisure
  * High, low and middle-level language
* Spoken: demographic sample of discussions, event-based sample of educational, business, public/institutional and leisure speech (60% dialogue, 40% monologue)

## Terminology: average

“The average life expectancy at birth is 63 years for males and 64 years for females”

What does this mean?



![Anscombe's quartet, a set of datasets that have identical descriptive statistics (means, variances, correlation)](<.gitbook/assets/image (3).png>)

[https://en.wikipedia.org/wiki/Anscombe%27s\_quartet](https://en.wikipedia.org/wiki/Anscombe's\_quartet)

[https://statistics.laerd.com/statistical-guides/measures-central-tendency-mean-mode-median.php](https://statistics.laerd.com/statistical-guides/measures-central-tendency-mean-mode-median.php)&#x20;

1. Reading assignment: [The civilizing process in London’s Old Bailey](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4084475/pdf/pnas.201405984.pdf)
   * Try to answer the questions given under the "Reading material" heading
2. [Explore bootstrapping](http://www.lock5stat.com/StatKey/bootstrap\_1\_quant/bootstrap\_1\_quant.html)
3. Check out the [Explained Visually](http://setosa.io/ev/) site, and especially [PCA explained visually](http://setosa.io/ev/principal-component-analysis/)

##
