# Data analysis: fundamental concepts of statistics

{% hint style="danger" %}
This content is not yet complete. In the meantime, see this presentation: [Data analysis: fundamental concepts of statistics](https://docs.google.com/presentation/d/e/2PACX-1vR7OYZauaLDOFf3M2ACynBcW77Ezx7SDSh5heLEzxOdc0ExMujU5t7GpksgdHpXbQKE9mpYPxlWT6c-/pub?start=false\&loop=false\&delayms=3000) ([pdf](http://docs.google.com/presentation/d/1LYYXZJ3WOHCThv\_i4fA\_anx\_s0LkYxFQ0wzJpC8KaSk/export/pdf), [gd](https://docs.google.com/presentation/d/1LYYXZJ3WOHCThv\_i4fA\_anx\_s0LkYxFQ0wzJpC8KaSk/edit?usp=sharing))
{% endhint %}

Consider [this dataset](https://docs.google.com/spreadsheets/d/154ShU7S8ykod5XU7N4zgygZOzXY4ztLCO\_KBD7U6zxI/edit?usp=sharing) describing the gender, lifespans, social ranks, education and number of letters written by a bunch of people (taken from metadata of the [Corpus of Early English Correspondence](http://www.helsinki.fi/varieng/CoRD/corpora/CEEC/index.html)), the first five rows of which are reproduced below:&#x20;

| Name                                | Sex    | Lifespan | Rank         | Education | NumberOfLetters |
| ----------------------------------- | ------ | -------- | ------------ | --------- | --------------- |
| Mary Wortley Montagu née Pierrepont | Female | 73       | Nobility     | High      | 189             |
| JOHN HOLLES                         | Male   | 72       | Nobility     | High      | 136             |
| Samuel Pepys                        | Male   | 70       | Professional | High      | 136             |
| Daniel Fleming                      | Male   | 68       | Gentry       | High      | 122             |
| Walter Ralegh                       | Male   | 64       | Gentry       | High      | 119             |

What can one do with such data? First of all, one can look at the individuals. To see how they compare against each other with regard to all the axes, it may make sense to order or sort the data according to an axis of interest, such as [lifespan](https://docs.google.com/spreadsheets/d/154ShU7S8ykod5XU7N4zgygZOzXY4ztLCO\_KBD7U6zxI/edit#gid=1232246814) or [number of letters](https://docs.google.com/spreadsheets/d/154ShU7S8ykod5XU7N4zgygZOzXY4ztLCO\_KBD7U6zxI/edit#gid=1253333531). One can also visualize the data graphically, similarly ordered by [lifespan ](https://plot.ly/\~jiemakel/39/#/)or [number of letters](https://plot.ly/\~jiemakel/41/#/).

However, what if one is interested in not just individuals, but groups in the data, or alternatively the data as a whole? What can one say about the lifespans, or the number of letters written as a whole in this set of data? Looking at the [lifespan graph](https://plot.ly/\~jiemakel/39/#/) for example, one can say that the highest lifespan in the data is 95, while the lowest is 16. Also by finding the centrepoint of the graph and looking up the lifespan there, it seems that about half of the people live at least 65 years, while about half live less than that. However, from this view it is quite hard to say for example what the most common lifespans are. For this, it helps to _aggregate _the data by lifespan. In practice, this is done by taking all the lifespans appearing in the data, and counting how many times they appear. The result of this calculation is a [new table and visualization](https://docs.google.com/spreadsheets/d/154ShU7S8ykod5XU7N4zgygZOzXY4ztLCO\_KBD7U6zxI/edit#gid=904052074) describing the _distribution _of the lifespans.



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
