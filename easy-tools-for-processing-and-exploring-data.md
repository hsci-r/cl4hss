# Easy tools for acquiring, processing and exploring data

{% hint style="danger" %}
This content is not yet complete. In the meantime, see this presentation: [Easy tools for processing and exploring data](https://docs.google.com/presentation/d/e/2PACX-1vQ0GNUtEwkYQ4NyRki6SohJ2DLS0wt4MKF3cVzuU7UlLq9yUij5Qd2ZgFltEb8KcPp7aYOXrSLFMdYa/pub?start=false&loop=false&delayms=3000) \([pdf](https://docs.google.com/presentation/d/1RF4s0AJuoVUAQIdw3c4Sf5ozLIb2Kd_vNN1SXp8IqFg/export/pdf), [gd](https://docs.google.com/presentation/d/1RF4s0AJuoVUAQIdw3c4Sf5ozLIb2Kd_vNN1SXp8IqFg/edit?usp=sharing)\)
{% endhint %}

## Acquiring data

* [Introduction to web scraping](https://librarycarpentry.org/lc-webscraping/) \(quite advanced, but contains a section on a user interface tool as well\)
* Hand-written text transcription: [Transkribus](https://transkribus.eu/)
* Layout and text transcription: [OCR4all](https://github.com/OCR4all/getting_started)
* Keyword generation from text: [Annif](http://annif.org/)
* An [automated sound transcription tool](https://www.google.com/search?q=automated+sound+transcription)
* Twitter archiving: [TAGS](https://tags.hawksey.info/)

## Data processing

{% hint style="info" %}
**Assignment: data processing tools**

* Complete the [OpenRefine tutorial](https://programminghistorian.org/lessons/cleaning-data-with-openrefine)
{% endhint %}

#### Further resources

* [OpenRefine for Social Science Data](https://datacarpentry.org/openrefine-socialsci/) Data Carpentry tutorial, not really for social science but for general cleaning up of data
* Further tutorials:
  * [http://enipedia.tudelft.nl/wiki/OpenRefine\_Tutorial](http://enipedia.tudelft.nl/wiki/OpenRefine_Tutorial)
  * [http://j.mp/dhh15ho](http://j.mp/dhh15ho) \(includes section on extension\)
  * [http://freeyourmetadata.org/reconciliation/](http://freeyourmetadata.org/reconciliation/) \(on reconciliation\)

## Data exploration

### Visualisation

Visualisation is the act of taking data and transforming it into visual shapes and forms. The reasoning behind this is that humans are very good at processing visual information, with a lot of the necessary shape and anomaly detection and comparison processes even happening subconsciously.

Most visualisation is explanatory. [https://pudding.cool/2017/05/song-repetition/](https://pudding.cool/2017/05/song-repetition/)

* [http://www.datajourneyman.com/2016/03/21/preattentive-processing.html](http://www.datajourneyman.com/2016/03/21/preattentive-processing.html) / [https://medium.com/@vidya83.kesavan/preattentive-attributes-in-visualization-an-example-cb05ba1c9371](https://medium.com/@vidya83.kesavan/preattentive-attributes-in-visualization-an-example-cb05ba1c9371)
* Book: [Information visualization : perception for design](https://www.elsevier.com/books/information-visualization/ware/978-0-12-381464-7), particularly chapter 5 for pre-attentive processing and 6 for the gestalt laws.
* [http://socviz.co/lookatdata.html](http://socviz.co/lookatdata.html) section 1.5

{% hint style="info" %}
**Assignment**

Read [Perception deception](https://infoactive.co/data-design/ch17.html) & [Common visualization mistakes](https://infoactive.co/data-design/ch18.html). The articles are primarily oriented around explanatory data visualisation, but most computational humanities data analysis is exploratory. How do the problems transfer into that domain, when the only one you can deceive is yourself?
{% endhint %}

{% hint style="info" %}
**Assignment: data exploration tools**

Experiment with at least one of the following tools:

* tabular data → chart visualisations: [RAW](http://rawgraphs.io/)​
* tabular data → chart visualisations: [Voyager](http://vega.github.io/voyager/)
* tabular data → chart visualisations: ​[Tableau](https://www.tableau.com/)​
* tabular data → ​interactive map/network/timeline/list/facet visualisations: [Palladio](https://moodle.helsinki.fi/hdlab.stanford.edu/palladio/)​
  * Palladio has [help pages](http://hdlab.stanford.edu/palladio/help/). There are also multiple tutorials on using Palladio, for example [this one](http://miriamposner.com/blog/getting-started-with-palladio/), or [this one](https://programminghistorian.org/en/lessons/creating-network-diagrams-from-historical-sources) which is particularly on network analysis.
* tabular data → map\(+timeline\) visualisations: ​[Carto](https://carto.com/)​
* ​text →​ interactive explorative interface for linguistic study: [Voyant tools](https://voyant-tools.org/)​
* ​big, preselected collections of text → interface for linguistic study: [Korp](https://moodle.helsinki.fi/korp.csc.fi) / [corpus.byu.edu](http://corpus.byu.edu/)​
* If you're feeling explorative, feel free to also dig for more tools in  [TAPoR](http://tapor.ca/home).

If you're short on inspiration, feel free to go through [this](https://docs.google.com/document/d/13I7svLlqrg7i0iisw2E_v48Gae5tnXVFWxmeHyGAKFU/edit#) hands-on tutorial covering OpenRefine, RAW and Palladio.

Afterwards, post a message on [\#tools](https://slack.com/app_redirect?channel=tools&team=T276JCMEU) on Slack detailing:

1. What is the tool good for?
2. What kind of data do you need for the tool to be useful? 
   1. What information does the data need to contain?
   2. What format does it have to be in?
3. Your experience with the tool.

If someone has already posted on the tool you tested, don't repeat them. Instead, add to what they've said in a thread.
{% endhint %}



{% hint style="info" %}
**Assignment: visualisation tool development**

Read the following two research articles on developing visualisation tools for particular text-based humanities research questions:

* [Visualizing Mouvance: Toward a visual analysis of variant medieval text traditions](https://doi.org/10.1093/llc/fqx033)
* [Rule‐based Visual Mappings – with a Case Study on Poetry Visualization](https://onlinelibrary.wiley.com/doi/full/10.1111/cgf.12125)

Now, think of a visualisation that would help you in your field. What information would it visualise? Post a message on [\#tools](https://slack.com/app_redirect?channel=tools&team=T276JCMEU) on Slack 
{% endhint %}

## Resources

* [Flowchart on selecting a good visualization](http://extremepresentation.typepad.com/files/choosing-a-good-chart-09.pdf) based on what you want to show 
* [An example](http://daydreamingnumbers.com/blog/4-ways-to-visualize-likert-scales/) of four ways to visualise the same data and how that affects what you can read from it

