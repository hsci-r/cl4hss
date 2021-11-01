# Final project

To pass the course, you are required to demonstrate a grasp of actual computational work. Therefore, you are tasked with taking some dataset, and processing it in some way** to yield an analysis that tackles a question of interest in the humanities or social sciences. **

This assignment requires applying all the knowledge you have learned on the course to devise and test a process going from data to results. To do this, you will need to navigate between the limits of the data, methods and research questions, trying to figure out which line of research is possible. Often, this is an iterative process, starting from something, running up against limits of either data or methodology, and then trying to sidestep those. The most important learning goal of this assignment is to gain experience in this process in practice by going through it.

Potential datasets/APIs are for example (but instead of these please choose a dataset that is relevant to yourself):

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

Tools for processing and analysis are for example:

* Preprocessing: [R](https://www.r-project.org), [Python](https://www.python.org), [pandas](http://pandas.pydata.org), [tm](https://cran.r-project.org/web/packages/tm/index.html), [OpenRefine](http://openrefine.org), [OpenCV](http://opencv.org), [TensorFlow™ Image Recognition](https://www.tensorflow.org/versions/master/tutorials/image\_recognition/index.html), [tuneR](https://cran.r-project.org/web/packages/tuneR/index.html), [pyAudio Analysis](https://github.com/tyiannak/pyAudioAnalysis), ...
* Topic modeling: [Mallet](http://mallet.cs.umass.edu), [topicmodels](https://cran.r-project.org/web/packages/topicmodels/index.html), [LDAvis](https://cran.r-project.org/web/packages/LDAvis/index.html), [gensim](https://radimrehurek.com/gensim/), ...
* Dimensionality reduction/clustering: [stats](https://stat.ethz.ch/R-manual/R-devel/library/stats/html/00Index.html), [lsa](https://cran.r-project.org/web/packages/lsa/index.html), [BayesLCA](https://cran.r-project.org/web/packages/BayesLCA/index.html), [pvclust](https://cran.r-project.org/web/packages/pvclust/index.html), [Weka](http://www.cs.waikato.ac.nz/ml/weka/), ...
* Social network analysis: [igraph](http://igraph.org), [sna](https://cran.r-project.org/web/packages/sna/index.html), [statnet](https://cran.r-project.org/web/packages/statnet/index.html), [sonia](http://web.stanford.edu/group/sonia/index.html), …
* Simulation: [NetLogo](https://ccl.northwestern.edu/netlogo/), ...
* Neural networks: [som](https://cran.r-project.org/web/packages/som/index.html), [TensorFlow™](http://www.tensorflow.org), ...
* Association rule learning: [arules](https://cran.r-project.org/web/packages/arules/index.html), [Weka](http://www.cs.waikato.ac.nz/ml/weka/),
* Anomaly detection: [AnomalyDetection](https://github.com/twitter/AnomalyDetection), ...
* Visualisation: [Palladio](http://palladio.designhumanities.org), [nodegoat](http://nodegoat.net), [matplotlib](http://matplotlib.org), [seaborn](https://seaborn.pydata.org/index.html), [ggplot2](http://ggplot2.org), [iPlots](https://cran.r-project.org/web/packages/iplots/index.html), [plot.ly](https://plot.ly), ...

To return the assignment, you will need to upload your data, code and results into a [GitHub](http://github.com) repository, link that repository with [Zenodo](https://zenodo.org) and give us the Zenodo [DOI](https://www.doi.org) for your work. Include in your repository a document (e.g. a [README.md](https://help.github.com/articles/about-readmes/)) describing what you've done, **following as best as possible the guidelines for open, reproducible research**. Make sure the document answers the following questions:

1. What are your humanities/social science research questions?
2. Which data did you use?
3. What did you do to the data, and how can I reproduce it?
4. What does the analysis show, how does it answer the humanities/social science research question?
5. Critically analyze your data and pipeline for potential bias and problems. What would still need to be done for the analysis to be trustable?

**Further info:** as said, the most important learning goal for this assignment is to learn how to navigate the between the shoals of data, method and questions in designing a computational humani science research process. Thus, for submissions, I prefer full pipelines that go from raw data to results. To get there, it is okay to cut massive corners as long as you know which those corners are (and that is what question 5 is for). However, sometimes this just isn't possible. Therefore, submissions can also be just some steps towards a complete pipeline (e.g. the data cleaning part). However, if you don't have end results, you need to very explicitly describe what your next steps would be to get those (i.e. a plan for future research).

To return your assignment, send the Zenodo DOI to Eetu on Slack, along with your student ID number. You probably won't want to include the ID number in the project files themselves, as all of those are public in perpetuity. Remember to also fill the course [feedback form](https://goo.gl/forms/vXqu71qRJG6uzHgG2)!

### Evaluation criteria

* Minimum requirement (grade 1/5): Your project must include a humanities/social science research question, and a description of a complete pipeline that moves from a dataset toward that question. In addition, at least some step of the pipeline needs to be fully implemented.
* You need to document your pipeline in a way that it can be rerun and its results reproduced. (+1 grade)
* You need to include an analysis of the results of your pipeline. If you do not end up with a full pipeline from data to analytical results, then you need to evaluate the reliability of the part of the pipeline that you did develop. (+1 grade)
* To get a 4 or a 5, both your analysis as well as documentation need to be robust, logical and understandable. This includes:
  1. A clear, logical description of your whole research process that will enable it to be critiqued and reproduced in full - what did you do at each point to the data, and why? Also be sure to include an analysis of points of possible biases and problems in your data and pipeline (+1 grade)
  2. Importantly, a reasoned and thorough discussion of the results from your analysis from the viewpoint of the humanities/social science research questions. If possible, contextualize your analysis with regard to other disciplinary knowledge (+1 grade)

Here it should be noted that checking all the marks will be much easier with a pipeline that yields an analytical result at the end. It will be possible to attain these also with partial pipelines, but without an analytical result, you need to employ indirection and projection to relate your reliability analysis to how its results would affect substantive analysis. Alternatively or in addition, you might need to do a manual substantive analysis of a subset to be able to discuss implications from the viewpoint of humanities/social science scholarship.

### Submissions from previous years

To further aid you in your work, here are some previous submissions for inspiration (for most of them, you should actually click the GitHub link on the right to start to make sense of them):

* Themes in Hungarian folk love songs - DOI: [10.5281/zenodo.44570](http://doi.org/10.5281/zenodo.44570)
* Extracting and visualizing biographical information from an old bank matricle - DOI: [10.5281/zenodo.225890](http://doi.org/10.5281/zenodo.225890)
* Analysis of a survey on user involvement in software development - DOI: [10.5281/zenodo.237727](https://doi.org/10.5281/zenodo.237727)
* Comparing Language Complexity in Fact-Checked Fake and Real News - DOI:[ 10.5281/zenodo.4327219](https://doi.org/10.5281/zenodo.4327219)
* Polite vs casual address form use by Finnish language learners in different situations - DOI: [10.5281/zenodo.218844](https://doi.org/10.5281/zenodo.218844)
* Discovering patterns in chalcolithic and early bronze age burials in northeast England- DOI: [10.5281/zenodo.215932](https://doi.org/10.5281/zenodo.215932)
* Finnish politicians in pictures - biases in the contents of the Finna portal - DOI:[ 10.5281/zenodo.4313215](https://doi.org/10.5281/zenodo.4313215)
* Themes discussed in Helsingin Sanomat in 1905 - DOI: [10.5281/zenodo.44572](http://doi.org/10.5281/zenodo.44572)
* Differences in use between the words _maahanmuuttaja_ and _pakolainen_ in Finnish newspapers 1970- to present - DOI: [10.5281/zenodo.44544](http://doi.org/10.5281/zenodo.44544)
* Differences in how frequently Finnish and Swedish newspapers talk about the Romani people - DOI: [10.5281/zenodo.44590](http://doi.org/10.5281/zenodo.44590)
* Contrasting Beck's lyrics to blues lyrics - DOI: [10.5281/zenodo.215292](http://doi.org/10.5281/zenodo.215292)
* Extracting and analysing recipe information in an old cookbook - DOI: [10.5281/zenodo.216232](https://doi.org/10.5281/zenodo.216232)
* Comparing the use of polite plural "you" in Mandarin Chinese and Lithuanian - DOI: [10.5281/zenodo.1134294](https://doi.org/10.5281/zenodo.1134294)
* A thematic analysis of the discussion around Guggenheim on the Suomi24 forum - DOI: [10.5281/zenodo.217719](https://doi.org/10.5281/zenodo.217719)
* Sentiment analysis of Twitter discussion related to the Indian biometric identifier system Aadhaar - DOI: [10.5281/zenodo.1134623](https://doi.org/10.5281/zenodo.1134623)
* Differences in language between texts dealing with altered states of mind and normal fiction - DOI: [10.5281/zenodo.230676](https://doi.org/10.5281/zenodo.230676)
* Social relations as expressed in District Court Sessions of Iisalmi parish 1639-1651 - DOI: [10.5281/zenodo.4327155](https://doi.org/10.5281/zenodo.4327155)
* Preliminary analysis of Free Direct Speech in _Se tapahtui täällä_ by Raija Siekkinen - DOI:[ 10.5281/zenodo.4338190](https://doi.org/10.5281/zenodo.4338190)
* Exploring ways to compare adaptations of a literary work - DOI: [10.5281/zenodo.1127754](http://doi.org/10.5281/zenodo.1127754)
* Preliminary analysis comparing different Finnish cabinet strategies against each other - DOI: [10.5281/zenodo.216604](https://doi.org/10.5281/zenodo.216604)
* Preliminary analysis of patterns in the holdings of the Finnish National Gallery - DOI: [10.5281/zenodo.218735](https://doi.org/10.5281/zenodo.218735)
