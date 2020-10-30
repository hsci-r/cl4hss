# Data

{% hint style="warning" %}
This content is not yet complete \(portions not complete marked separately below\).
{% endhint %}

![Data in the context of a computational human sciences research process](.gitbook/assets/image%20%287%29.png)

On this course, computational human sciences has been defined as **the application of computational and/or statistical techniques** to **data** in order to yield **results of interest to the human sciences**. In this part of the course, we will delve into what we mean by data and discuss the particular problems inherent in the types of data most often used in computational human sciences research. 

First, to get an intuitive understanding of what data is and how it can be used, we present multiple short glances into different viewpoints around archetypes, modes of engagement and ways to access data.  

## Archetypes of data

For the purposes of this course, data is defined as information in digital format. For practical purposes, it is useful to partition data into two archetypes: structured and unstructured. Examples of structured data include Excel sheets such as [this one](https://docs.google.com/spreadsheets/d/1t2GsvwAx-_gCd6QjmXcZ-x2aI7xBuOcstXP0GwLE3x0/edit?usp=sharing) containing information on ancient Greek books, and databases, such as[ this one](http://fbtee.uws.edu.au/stn/interface/query_books.php?t=sector&e=rawsales&id=Clergy&g=everywhere&d1=01&m1=01&y1=1769&d2=31&m2=12&y2=1794&d=table) containing information on books, places and people related to French book trade in Enlightenment Europe. Examples of unstructured data include raw texts \(like this [Complete Works of William Shakespeare](http://www.gutenberg.org/cache/epub/100/pg100.txt)\), sounds \(like this[ recording from 1906](https://archive.org/details/Edison_Blue_Amberol_2853-1720)\) and images \(like this[ image of a newspaper page from 1884](https://digi.kansalliskirjasto.fi/sanomalehti/binding/379556/image/1)\).

In the end, computers are really only good with structured data and numbers. They want to count explicit things, be they occurrences of certain gods in ancient Greek texts, or particular types of relationships between people involved in book trade. Thus, if starting with unstructured data, your first task will often be to extract structure out of that data \(for example, frequencies of certain words from text, or neural network -deduced keyword descriptions of images\)

![Visualisation of what different layers of a convolutional neural network identify from an image \(adapted from &quot;Convolutional deep belief networks for scalable unsupervised learning of hierarchical representations&quot;, Lee et al. 2009\)](.gitbook/assets/image%20%289%29.png)

So how do e.g. neural networks manage to extract structure from the "unstructured image", you might ask? Well, it is actually already structured for the computer. It just has structure on an extremely low level. What an image is to a computer is a a grid of numbers, each number describing the colour and brightness of one square in the grid. What a neural network does, is take this extremely low level information, and starts to build higher level features from it by combining information from multiple squares in the grid. For example, if there are multiple bright squares in a row while their other neighbours in the grid are dark, that indicates there may be a line there. Then, when the neural network knows where lines are, maybe it can combine certain patterns of lines into circles, certain patterns of circles into eyes, and finally certain patterns of eyes, mouths and noses into a guess that the image depicts a face.

This is also the way in which many of your analysis processes will proceed. You start with some data, and then apply various means by which you'll derive more involved and sophisticated features from that data, until you arrive at something which corresponds \(near enough\) to your object of interest. For example, given a set of digitised newspaper images, you may first apply one tool to detect illustrations, a second one to filter those to advertisement images, a third one to extract keyword descriptions out of those, add a manual step to filter and categorise those keywords into categories corresponding to your object of interest \(e.g. if you're interested in gender images in advertising, you map "woman" and "girl" to "female" and "man" and "boy" to "male", while grouping a whole slew of keywords either into categories such as "technical", "household", "outdoors" etc\). Only after this will you take this data and use your analytical and statistical tools to count the number of times each gender is associated with each category across source, place and time in order to answer your original question.

## Modes of engagement with data

Next, again for the purposes of this course, it is useful to delineate and contrast some archetypal modes of engaging with data \(all examples being different ways of interacting with the [Finnish national library collection of digitised newspapers](https://digi.kansalliskirjasto.fi/)\):

* [Non-digital / digital without any functionality](https://digi.kansalliskirjasto.fi/sanomalehti/titles/0785-398X?display=THUMB&year=1929&set_language=en) - both finding relevant sources as well as their analysis happens through manual work and reading
* [Search interfaces](https://digi.kansalliskirjasto.fi/search?query=Einstein&orderBy=RELEVANCE&set_language=en) - aid in finding, but analysis and understanding happens through reading
* Analytical interfaces - _transform_ and _aggregate_ the data in new ways to yield insight. For example:
  * [Keyword in context \(KWIC\) interfaces](https://korp.csc.fi/#?stats_reduce=word&cqp=%5B%5D&corpus=klk_fi_2000,klk_fi_1999,klk_fi_1998,klk_fi_1997,klk_fi_1996,klk_fi_1995,klk_fi_1994,klk_fi_1993,klk_fi_1992,klk_fi_1991,klk_fi_1990,klk_fi_1989,klk_fi_1988,klk_fi_1987,klk_fi_1986,klk_fi_1985,klk_fi_1984,klk_fi_1983,klk_fi_1982,klk_fi_1981,klk_fi_1980,klk_fi_1979,klk_fi_1978,klk_fi_1977,klk_fi_1976,klk_fi_1975,klk_fi_1974,klk_fi_1973,klk_fi_1972,klk_fi_1971,klk_fi_1970,klk_fi_1969,klk_fi_1968,klk_fi_1967,klk_fi_1966,klk_fi_1965,klk_fi_1964,klk_fi_1963,klk_fi_1962,klk_fi_1961,klk_fi_1960,klk_fi_1959,klk_fi_1958,klk_fi_1957,klk_fi_1956,klk_fi_1955,klk_fi_1954,klk_fi_1953,klk_fi_1952,klk_fi_1951,klk_fi_1950,klk_fi_1949,klk_fi_1948,klk_fi_1947,klk_fi_1946,klk_fi_1945,klk_fi_1944,klk_fi_1943,klk_fi_1942,klk_fi_1941,klk_fi_1940,klk_fi_1939,klk_fi_1938,klk_fi_1937,klk_fi_1936,klk_fi_1935,klk_fi_1934,klk_fi_1933,klk_fi_1932,klk_fi_1931,klk_fi_1930,klk_fi_1929,klk_fi_1928,klk_fi_1927,klk_fi_1926,klk_fi_1925,klk_fi_1924,klk_fi_1923,klk_fi_1922,klk_fi_1921,klk_fi_1920,klk_fi_1919,klk_fi_1918,klk_fi_1917,klk_fi_1916,klk_fi_1915,klk_fi_1914,klk_fi_1913,klk_fi_1912,klk_fi_1911,klk_fi_1910,klk_fi_1909,klk_fi_1908,klk_fi_1907,klk_fi_1906,klk_fi_1905,klk_fi_1904,klk_fi_1903,klk_fi_1902,klk_fi_1901,klk_fi_1900,klk_fi_1899,klk_fi_1898,klk_fi_1897,klk_fi_1896,klk_fi_1895,klk_fi_1894,klk_fi_1893,klk_fi_1892,klk_fi_1891,klk_fi_1890,klk_fi_1889,klk_fi_1888,klk_fi_1887,klk_fi_1886,klk_fi_1885,klk_fi_1884,klk_fi_1883,klk_fi_1882,klk_fi_1881,klk_fi_1880,klk_fi_1879,klk_fi_1878,klk_fi_1877,klk_fi_1876,klk_fi_1875,klk_fi_1874,klk_fi_1873,klk_fi_1872,klk_fi_1871,klk_fi_1870,klk_fi_1869,klk_fi_1868,klk_fi_1867,klk_fi_1866,klk_fi_1865,klk_fi_1864,klk_fi_1863,klk_fi_1862,klk_fi_1861,klk_fi_1860,klk_fi_1859,klk_fi_1858,klk_fi_1857,klk_fi_1856,klk_fi_1855,klk_fi_1854,klk_fi_1853,klk_fi_1852,klk_fi_1851,klk_fi_1850,klk_fi_1849,klk_fi_1848,klk_fi_1847,klk_fi_1846,klk_fi_1845,klk_fi_1844,klk_fi_1842,klk_fi_1841,klk_fi_1840,klk_fi_1839,klk_fi_1838,klk_fi_1837,klk_fi_1836,klk_fi_1835,klk_fi_1834,klk_fi_1833,klk_fi_1832,klk_fi_1831,klk_fi_1830,klk_fi_1829,klk_fi_1827,klk_fi_1826,klk_fi_1825,klk_fi_1824,klk_fi_1823,klk_fi_1822,klk_fi_1821,klk_fi_1820,reittidemo&lang=en&search=word%7CEinstein&page=0) show search results, but ordered around the word and its particular instances. Data is returned not in its original structure, but transformed to a view centred around the word and its appearances.
  * [Frequency graphs](https://digi.kansalliskirjasto.fi/search?query=Einstein&formats=NEWSPAPER&resultMode=CHART&set_language=en) _transform_ the data through _aggregation_, here counting how many times a keyword is found in the data, and projecting these counts through time. Through this presentation, large-scale trends can be seen.

## Ways of accessing data

{% hint style="danger" %}
This section not yet complete. In the meantime, please see [this presentation](https://docs.google.com/presentation/d/e/2PACX-1vSv9s1sY5NMfjnCKPU7NJZyB6zY3B7BMSNMXuWSDBi71uDkn6tq_u53qYbpnhJN3etf9n_oJgJrU7U8/pub?start=false&loop=false&delayms=3000)
{% endhint %}

* User interfaces provide access to pre-defined functionalities in a user-friendly manner
* APIs provide access to pre-defined functionalities for programmes
* Having access to the dataset _as data_ allows you yourself control over which tools to use, and how to tie the tools together into a workflow.
* Data dumps provide access to raw data. However, they may often be very large, and their format may also be complex in order to include all facets of the data. Thus, raw dumps may be difficult to process and use.
* Both user interfaces as well as APIs may allow subsets of the data to be selected and downloaded _as data_ for further analysis. Often these allow limiting both the size of the data, as well as its features, thus making the resulting data much easier to process and handle. However, very often APIs do not contain all facets of the original data, instead making a trade-off between richness and ease of use to serve the data in a simpler, easier format useful for a particular subset of use cases.

## Problems with non-standard data

{% hint style="danger" %}
This section not yet written. In the meantime, please see [this presentation](https://docs.google.com/presentation/d/e/2PACX-1vSv9s1sY5NMfjnCKPU7NJZyB6zY3B7BMSNMXuWSDBi71uDkn6tq_u53qYbpnhJN3etf9n_oJgJrU7U8/pub?start=false&loop=false&delayms=3000)
{% endhint %}

## Assignment

{% hint style="info" %}
**Assignment**

1. Find a dataset that could be of interest to you in your final project. Post a message on [\#datasets](https://slack.com/app_redirect?channel=datasets&team=T276JCMEU) on Slack giving:
   1. A link to the dataset
   2. A note on why you selected it
   3. A short description of what types of information the dataset contains, and 
   4. The structure, technical format and way of downloading the data
2. Find a potential source of bias in a dataset someone else picked. Reply to their message on Slack to let them know about it.
3. If you get a note of bias, respond back by thinking of ways of overcoming or surmounting it.
{% endhint %}

Potential datasets/APIs are for example:

* [CLARIN corpora](https://www.clarin.eu/portal)
* [Korp API](https://kitwiki.csc.fi/twiki/bin/view/FinCLARIN/KielipankkiHelpKorpWebService)
* [Finnish national gallery API / dump](http://kokoelmat.fng.fi/api/v2support/docs/#/download)
* [Schoenberg database](http://dla.library.upenn.edu/dla/schoenberg/ancillary.html?id=dla/schoenberg/data)
* [Cushman collection metadata](https://github.com/iulibdcs/cushman_photos)
* [WW2 covert support networks](http://programminghistorian.org/lessons/creating-network-diagrams-from-historical-sources#about-the-case-study)
* [Europeana APIs](http://labs.europeana.eu/api)
* [DPLA APIs](http://dp.la/info/developers/codex/)
* [The European Library API](http://www.theeuropeanlibrary.org/confluence/display/developers/API+Documentation)
* [Sydney Powerhouse Museum](http://www.powerhousemuseum.com/collection/database/download.php)
* [EEBO-TCP Phase I](http://www.bodleian.ox.ac.uk/eebotcp/)
* [ECCO-TCP](http://www.textcreationpartnership.org/tcp-ecco/)

## Further resources

* [Data Organization in Spreadsheets for Social Scientists](https://datacarpentry.org/spreadsheets-socialsci/) \(not really anything social science specific\) / [Tidy data for librarians](https://librarycarpentry.org/lc-spreadsheets/) \(nothing library specific either\)
* [Big? Smart? Clean? Messy? Data in the Humanities](http://journalofdigitalhumanities.org/2-3/big-smart-clean-messy-data-in-the-humanities/) \(simple introduction to different kinds of data in the digital humanities\)
* Biases caused by using publicly available Twitter APIs \(search/streaming\) for sampling:
  * [Social Data: Biases, Methodological Pitfalls, and Ethical Boundaries](https://www.frontiersin.org/articles/10.3389/fdata.2019.00013/full)
  * [Assessing bias in samples collected from Twitter](https://www.sciencedirect.com/science/article/pii/S0378873314000057)
  * [We Don't Know What We Don't Know: When and How the Use of Twitter's Public APIs Biases Scientific Inference](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3079927)
  * [Is the Sample Good Enough? Comparing Data from Twitter's Streaming API with Twitter's Firehose](https://www.aaai.org/ocs/index.php/ICWSM/ICWSM13/paper/viewPaper/6071)

