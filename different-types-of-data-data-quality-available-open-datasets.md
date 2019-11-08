# Different types of data, data quality, available open datasets

{% hint style="danger" %}
This content is not yet complete. In the meantime, please see this presentation: [Different types of data, data quality, available open datasets](https://docs.google.com/presentation/d/e/2PACX-1vRxpRxXXyF-fTZ8YpB5utG09SNnmti4MB7qTzYU2ipQl0VBlmmODdqgIX0g4CO3EEJ3OiKuePP3vlt0/pub?start=false&loop=false&delayms=3000) \([pdf](https://docs.google.com/presentation/d/1KFpHbK9Fu8mu5pN-6FA7wmNuX1HTrpmGZ3lhPlASvd4/export/pdf), [gd](https://docs.google.com/presentation/d/1KFpHbK9Fu8mu5pN-6FA7wmNuX1HTrpmGZ3lhPlASvd4/edit)\)
{% endhint %}

## Types of data

* Structured vs unstructured:
  * Structured data - [Excel sheets](https://docs.google.com/spreadsheets/d/1t2GsvwAx-_gCd6QjmXcZ-x2aI7xBuOcstXP0GwLE3x0/edit?usp=sharing), [databases](http://fbtee.uws.edu.au/stn/interface/query_books.php?t=sector&e=rawsales&id=Clergy&g=everywhere&d1=01&m1=01&y1=1769&d2=31&m2=12&y2=1794&d=table), [2](https://docs.google.com/drawings/d/1lZHqRw_rFlbnWytL6olSXE-mKS2HJqic5debjH7__bw/edit?usp=sharing)
  * Unstructured data - [text](http://www.gutenberg.org/cache/epub/100/pg100.txt), [2](http://digi.kansalliskirjasto.fi/sanomalehti/binding/379556?page=1&ocr=true), [3](https://goo.gl/Kpt4iv), [sounds](http://www.automaticsync.com/captionsync/youtube-automatic-captions/), [images](https://www.clarifai.com/demo)
* Clean vs messy
* **Biased? ← incomplete, messy, badly sampled**

## Modes of engagement with data

* Non-digital / digital without any functionality - both finding relevant sources as well as their analysis happens through manual work and reading
* Search interfaces - aid in finding, but analysis and understanding happens through reading
* Analytical interfaces - _transform_ and _aggregate_ the data in new ways to yield insight. For example:
  * Keyword in context \(KWIC\) interfaces show search results, but ordered around the word and its particular instances. Data is returned not in its original structure, but transformed to a view centred around the word and its appearances.
  * Frequency graphs _transform_ the data through _aggregation_, counting how many times a keyword is found in the data, and projecting these counts through time. Through this presentation, large-scale trends can be seen.

## Data access

**Ways of accessing data**

* User interfaces provide access to pre-defined functionalities in a user-friendly manner
* APIs provide access to pre-defined functionalities for programmes
* Having access to the dataset _as data_ allows you yourself control over which tools to use, and how to tie the tools together into a workflow.
* Data dumps provide access to raw data. However, they may often be very large, and their format may also be complex in order to include all facets of the data. Thus, raw dumps may be difficult to process and use.
* Both user interfaces as well as APIs may allow subsets of the data to be selected and downloaded _as data_ for further analysis. Often these allow limiting both the size of the data, as well as its features, thus making the resulting data much easier to process and handle. However, very often APIs do not contain all facets of the original data, instead making a trade-off between richness and ease of use to serve the data in a simpler, easier format useful for a particular subset of use cases.

#### Open data in the digital humanities - the good

* Great aggregators pushing for CC0 licenses, publishing participating data: [Europeana](http://www.europeana.eu/portal/europeana-providers.html), [Digital Public Library of America](http://dp.la/) & [The European Library](http://www.theeuropeanlibrary.org/tel4/access/data/opendata/details)
* Influential national libraries moving to co-operative open \(linked\) data
  * [Library of Congress](http://id.loc.gov/), [Deutsche Nationalbibliothek](http://www.dnb.de/EN/lds.html), [British Library](http://www.bl.uk/bibliographic/data.html), [Bibliothèque nationale de France](http://data.bnf.fr/)
* Museums, Galleries and Archives catching up: [British Museum](http://collection.britishmuseum.org/), [Finnish National Gallery](http://kokoelmat.fng.fi/api/v2support/docs/#/overview), …
* Glue available: [VIAF](http://viaf.org/), [CIDOC-CRM](http://www.cidoc-crm.org/definition_cidoc.html), Getty [AAT](http://www.getty.edu/research/tools/vocabularies/aat/), [TGN](http://www.getty.edu/research/tools/vocabularies/tgn/index.html), [ULAN](http://www.getty.edu/research/tools/vocabularies/ulan/index.html), [CONA](http://www.getty.edu/research/tools/vocabularies/cona/index.html), [Pleiades](http://pleiades.stoa.org/), ...

#### Open data in the digital humanities - the bad

* Academic libraries have a long tradition of collaborating with library service companies \(primarily EBSCO Information Services, ProQuest LLC and Gale Cengage Learning\) to produce services
* Often, they also participate in content creation projects, and then hold the rights for that content
  * e.g. [Early English Books Online](http://www.textcreationpartnership.org/tcp-eebo/) \(ProQuest\), [Nineteenth Century Collections Online](http://gale.cengage.co.uk/product-highlights/history/nineteenth-century-collections-online.aspx) \(Gale\), [State Papers Online](http://gale.cengage.co.uk/state-papers-online-15091714.aspx) \(Gale\)
* But, this is also a wider culture inside humanities, e.g. [Electronic Enlightenment](http://www.e-enlightenment.com/info/subscribers/why_charge.html)

Potential datasets/APIs are for example:

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

### Further resources

* [Data Organization in Spreadsheets for Social Scientists](https://datacarpentry.org/spreadsheets-socialsci/) \(not really anything social science specific\) / [Tidy data for librarians](https://librarycarpentry.org/lc-spreadsheets/) \(nothing library specific either\)
* [Big? Smart? Clean? Messy? Data in the Humanities](http://journalofdigitalhumanities.org/2-3/big-smart-clean-messy-data-in-the-humanities/) \(simple introduction to different kinds of data in the digital humanities\)
* Biases caused by using publicly available Twitter APIs \(search/streaming\) for sampling:
  * [Social Data: Biases, Methodological Pitfalls, and Ethical Boundaries](https://www.frontiersin.org/articles/10.3389/fdata.2019.00013/full)
  * [Assessing bias in samples collected from Twitter](https://www.sciencedirect.com/science/article/pii/S0378873314000057)
  * [We Don't Know What We Don't Know: When and How the Use of Twitter's Public APIs Biases Scientific Inference](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3079927)
  * [Is the Sample Good Enough? Comparing Data from Twitter's Streaming API with Twitter's Firehose](https://www.aaai.org/ocs/index.php/ICWSM/ICWSM13/paper/viewPaper/6071)

