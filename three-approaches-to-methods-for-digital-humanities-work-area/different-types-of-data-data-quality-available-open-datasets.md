# Data

{% hint style="warning" %}
This content is not yet complete (portions not complete marked separately below).
{% endhint %}

![Data in the context of a computational human sciences research process](<../.gitbook/assets/image (10).png>)

On this course, computational human sciences has been defined as **the application of computational and/or statistical techniques** to **data** in order to yield **results of interest to the human sciences**. In this part of the course, we will delve into what we mean by data and discuss the particular problems inherent in the types of data most often used in computational human sciences research.&#x20;

First, to get an intuitive understanding of what data is and how it can be used, we present multiple short glances into different viewpoints around archetypes, modes of engagement and ways to access data. &#x20;

## Archetypes of data

For the purposes of this course, data is defined as information in digital format. For practical purposes, it is useful to partition data into two archetypes: structured and unstructured. Examples of structured data include Excel sheets such as [this one](https://docs.google.com/spreadsheets/d/1t2GsvwAx-\_gCd6QjmXcZ-x2aI7xBuOcstXP0GwLE3x0/edit?usp=sharing) containing information on ancient Greek books, and databases, such as[ this one](http://fbtee.uws.edu.au/stn/interface/query\_books.php?t=sector\&e=rawsales\&id=Clergy\&g=everywhere\&d1=01\&m1=01\&y1=1769\&d2=31\&m2=12\&y2=1794\&d=table) containing information on books, places and people related to French book trade in Enlightenment Europe. Examples of unstructured data include raw texts (like this [Complete Works of William Shakespeare](http://www.gutenberg.org/cache/epub/100/pg100.txt)), sounds (like this[ recording from 1906](https://archive.org/details/Edison\_Blue\_Amberol\_2853-1720)) and images (like this[ image of a newspaper page from 1884](https://digi.kansalliskirjasto.fi/sanomalehti/binding/379556/image/1)).

In the end, computers are really only good with structured data and numbers. They want to count explicit things, be they occurrences of certain gods in ancient Greek texts, or particular types of relationships between people involved in book trade. Thus, if starting with unstructured data, your first task will often be to extract structure out of that data (for example, frequencies of certain words from text, or neural network -deduced keyword descriptions of images)

![Visualisation of what different layers of a convolutional neural network identify from an image (adapted from "Convolutional deep belief networks for scalable unsupervised learning of hierarchical representations", Lee et al. 2009)](<../.gitbook/assets/image (9).png>)

So how do e.g. neural networks manage to extract structure from the "unstructured image", you might ask? Well, it is actually already structured for the computer. It just has structure on an extremely low level. What an image is to a computer is a a grid of numbers, each number describing the colour and brightness of one square in the grid. What a neural network does, is take this extremely low level information, and starts to build higher level features from it by combining information from multiple squares in the grid. For example, if there are multiple bright squares in a row while their other neighbours in the grid are dark, that indicates there may be a line there. Then, when the neural network knows where lines are, maybe it can combine certain patterns of lines into circles, certain patterns of circles into eyes, and finally certain patterns of eyes, mouths and noses into a guess that the image depicts a face.

This is also the way in which many of your analysis processes will proceed. You start with some data, and then apply various means by which you'll derive more involved and sophisticated features from that data, until you arrive at something which corresponds (near enough) to your object of interest. For example, given a set of digitised newspaper images, you may first apply one tool to detect illustrations, a second one to filter those to advertisement images, a third one to extract keyword descriptions out of those, add a manual step to filter and categorise those keywords into categories corresponding to your object of interest (e.g. if you're interested in gender images in advertising, you map "woman" and "girl" to "female" and "man" and "boy" to "male", while grouping a whole slew of keywords either into categories such as "technical", "household", "outdoors" etc). Only after this will you take this data and use your analytical and statistical tools to count the number of times each gender is associated with each category across source, place and time in order to answer your original question.

## Modes of engagement with data

Next, again for the purposes of this course, it is useful to delineate and contrast some archetypal modes of engaging with data (all examples being different ways of interacting with the [Finnish national library collection of digitised newspapers](https://digi.kansalliskirjasto.fi)):

* [Non-digital / digital without any functionality](https://digi.kansalliskirjasto.fi/sanomalehti/titles/0785-398X?display=THUMB\&year=1929\&set\_language=en) - both finding relevant sources as well as their analysis happens through manual work and reading
* [Search interfaces](https://digi.kansalliskirjasto.fi/search?query=Einstein\&orderBy=RELEVANCE\&set\_language=en) - aid in finding, but analysis and understanding happens through reading
* Analytical interfaces - _transform_ and _aggregate_ the data in new ways to yield insight. For example:
  * Keyword in context (KWIC) interfaces show search results, but ordered around the word and its particular instances. Data is returned not in its original structure, but transformed to a view centred around the word and its appearances.
  * [Frequency graphs](https://digi.kansalliskirjasto.fi/search?query=Einstein\&formats=NEWSPAPER\&resultMode=CHART\&set\_language=en) _transform_ the data through _aggregation_, here counting how many times a keyword is found in the data, and projecting these counts through time. Through this presentation, large-scale trends can be seen.

## Ways of accessing data

{% hint style="danger" %}
This section not yet complete. In the meantime, please see [this presentation](https://docs.google.com/presentation/d/e/2PACX-1vSv9s1sY5NMfjnCKPU7NJZyB6zY3B7BMSNMXuWSDBi71uDkn6tq\_u53qYbpnhJN3etf9n\_oJgJrU7U8/pub?start=false\&loop=false\&delayms=3000)
{% endhint %}

* User interfaces provide access to pre-defined functionalities in a user-friendly manner
* APIs provide access to pre-defined functionalities for programmes
* Having access to the dataset _as data_ allows you yourself control over which tools to use, and how to tie the tools together into a workflow.
* Data dumps provide access to raw data. However, they may often be very large, and their format may also be complex in order to include all facets of the data. Thus, raw dumps may be difficult to process and use.
* Both user interfaces as well as APIs may allow subsets of the data to be selected and downloaded _as data_ for further analysis. Often these allow limiting both the size of the data, as well as its features, thus making the resulting data much easier to process and handle. However, very often APIs do not contain all facets of the original data, instead making a trade-off between richness and ease of use to serve the data in a simpler, easier format useful for a particular subset of use cases.

## Problems with non-standard data

{% hint style="danger" %}
This section not yet written. In the meantime, please see [this presentation](https://docs.google.com/presentation/d/e/2PACX-1vSv9s1sY5NMfjnCKPU7NJZyB6zY3B7BMSNMXuWSDBi71uDkn6tq\_u53qYbpnhJN3etf9n\_oJgJrU7U8/pub?start=false\&loop=false\&delayms=3000)
{% endhint %}

## Assignment

{% hint style="info" %}
**Assignment**

1. Find a dataset that could be of interest to you in your final project. Post a message on [#datasets](https://slack.com/app\_redirect?channel=datasets\&team=T276JCMEU) on Slack giving:
   1. A link to the dataset
   2. A note on why you selected it
   3. A short description of what types of information the dataset contains, and&#x20;
   4. The structure, technical format and way of downloading the data
2. Find a potential source of bias in a dataset someone else picked. Reply to their message on Slack to let them know about it.
3. If you get a note of bias, respond back by thinking of ways of overcoming or surmounting it.
{% endhint %}

Potential datasets/APIs are for example:

* [CLARIN corpora](https://www.clarin.eu/portal)
* [Korp API](https://kitwiki.csc.fi/twiki/bin/view/FinCLARIN/KielipankkiHelpKorpWebService)
* [Finnish national gallery API / dump](http://kokoelmat.fng.fi/api/v2support/docs/#/download)
* [Schoenberg database](http://dla.library.upenn.edu/dla/schoenberg/ancillary.html?id=dla/schoenberg/data)
* [Cushman collection metadata](https://github.com/iulibdcs/cushman\_photos)
* [WW2 covert support networks](http://programminghistorian.org/lessons/creating-network-diagrams-from-historical-sources#about-the-case-study)
* [Europeana APIs](http://labs.europeana.eu/api)
* [DPLA APIs](http://dp.la/info/developers/codex/)
* [The European Library API](http://www.theeuropeanlibrary.org/confluence/display/developers/API+Documentation)
* [Sydney Powerhouse Museum](http://www.powerhousemuseum.com/collection/database/download.php)
* [EEBO-TCP Phase I](http://www.bodleian.ox.ac.uk/eebotcp/)
* [ECCO-TCP](http://www.textcreationpartnership.org/tcp-ecco/)

## Further resources

* [Data Organization in Spreadsheets for Social Scientists](https://datacarpentry.org/spreadsheets-socialsci/) (not really anything social science specific) / [Tidy data for librarians](https://librarycarpentry.org/lc-spreadsheets/) (nothing library specific either)
* [Big? Smart? Clean? Messy? Data in the Humanities](http://journalofdigitalhumanities.org/2-3/big-smart-clean-messy-data-in-the-humanities/) (simple introduction to different kinds of data in the digital humanities)
* Biases caused by using publicly available Twitter APIs (search/streaming) for sampling:
  * [Social Data: Biases, Methodological Pitfalls, and Ethical Boundaries](https://www.frontiersin.org/articles/10.3389/fdata.2019.00013/full)
  * [Assessing bias in samples collected from Twitter](https://www.sciencedirect.com/science/article/pii/S0378873314000057)
  * [We Don't Know What We Don't Know: When and How the Use of Twitter's Public APIs Biases Scientific Inference](https://papers.ssrn.com/sol3/papers.cfm?abstract\_id=3079927)
  * [Is the Sample Good Enough? Comparing Data from Twitter's Streaming API with Twitter's Firehose](https://www.aaai.org/ocs/index.php/ICWSM/ICWSM13/paper/viewPaper/6071)
