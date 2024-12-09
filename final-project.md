# Final project

To pass the course, you are required to demonstrate that you're able to take what you've learned, and use it to design and enact computational work in practice. Therefore, you are tasked with taking some dataset, and processing it in some way **to yield an analysis that tackles a question of interest in the humanities or social sciences.**&#x20;

To do this, you will need to navigate between the limits of the data, methods and research questions, trying to figure out which line of research is possible. Often, this is an iterative process, starting from something, running up against limits of either data or methodology, and then trying to sidestep those. The most important learning goal of this assignment is to gain experience in this process in practice by going through it.

Throughout the course, there are exercises designed to give you ideas on what you could do and what data and methods you could use. Apart from them, an excellent source for ideas and examples are the submissions from previous years listed at the bottom of this page.

### Evaluation criteria

* Minimum requirement (grade 1/5): Your project must include a humanities/social science research question, and a description of a complete pipeline that moves from a dataset to answer that question. Naturally in the context of this course, the pipeline also needs to rely on computation in at least one step. In addition, at least one computational step needs to be fully implemented.
* You need to document your pipeline in a way that it can be rerun and its results reproduced. (+1 grade)
* You need to include an analysis of the results of your pipeline. If you do not end up with a full pipeline from data to analytical results, then you need to evaluate the reliability of the part of the pipeline that you did develop. (+1 grade)
* To get a 4 or a 5, both your analysis as well as documentation need to be robust, logical and understandable. This includes:
  1. A clear, logical description of your whole research process that will enable it to be critiqued and reproduced in full - what did you do at each point to the data, and why? Also be sure to include an analysis of points of possible biases and problems in your data and pipeline (+1 grade)
  2. Importantly, a reasoned and thorough discussion of the results from your analysis from the viewpoint of the humanities/social science research questions. If possible, contextualise your analysis with regard to other disciplinary knowledge (+1 grade)

Here it should be noted that checking all the marks will be much easier with a pipeline that yields an analytical result at the end. It will be possible to attain these also with partial pipelines, but without an analytical result, you need to employ indirection and projection to relate your reliability analysis to how its results would affect substantive analysis. Alternatively or in addition, you might need to do a manual substantive analysis of a subset to be able to discuss implications from the viewpoint of humanities/social science scholarship.

As a special consideration, while naturally hoping that your pipeline succeeds, sometimes in the end you find out that the approach you picked just can't be made to work. In this case, what I'm looking for is a "robust report of failure", meaning that you can document that you've spent a reasonable amount of effort in trying different options and ways to get the pipeline to work. In addition, you must be able to explain in detail exactly how the results are insufficient and/or problematic in being useful for answering your initial research questions.

**Importantly, you are free to submit your final assignment as many times as you want, until you obtain the grade that you desire.**&#x20;

### Returning your assignment

In your work, you are expected to **follow as best as possible the guidelines for open, reproducible research**. Thus, to return the assignment, you will need to upload your data, code and results into a [GitHub](http://github.com/) repository, link that repository with [Zenodo](https://zenodo.org/) and give us the Zenodo [DOI](https://www.doi.org/) for your work. To ensure readability, include with your project a document (e.g. a [README.md](https://help.github.com/articles/about-readmes/)) describing what all the parts of the project are (e.g. what is the main documentation file, where are the data, where are any code files, etc).

To return your assignment, send the Zenodo DOI to Eetu on Slack, along with your student ID number. You probably won't want to include the ID number in the project files themselves, as all of those are public in perpetuity. Remember to also fill the course [feedback form](https://forms.gle/mAzroPpS89Hw2BQS8)! (University of Helsinki students should use the [official version](https://norppa.helsinki.fi/targets/82907178/feedback))

As to why I'm requiring you to return your final project this way:&#x20;

* [Open science isn't one but many things](https://doi.org/10.1007/978-3-319-00026-8_2). While they're all important, on this course, we're concerned with only the facets of open science that align with the drive to increase the reproducibility (and through that the trustworthiness) of research, i.e. open data, open research processes and open source.
* Reproducibility is a huge issue for science today; it turned out that most of our research results actually couldn't be replicated - i.e. may not have been real or trustworthy in the first place. One of the fields hit early by the reproducibility problem tsunami was psychology. Running from 2011-2015, the [Reproducibility Project: Psychology ](https://osf.io/ezcuj/)could [replicate only 35 out of 97 landmark studies in psychology](https://www.science.org/doi/10.1126/science.aac4716). In addition, it was found that [over half of the publications in psychology contain simple statistical errors](https://mbnuijten.com/wp-content/uploads/2013/01/nuijtenetal_2015_reportingerrorspsychology1.pdf). However, other fields have since then also had similar comeuppances: In [cancer research](https://www.cos.io/rpcb), [only 9 out of 53 landmark studies were reproducible](https://www.nature.com/articles/483531a), while in management science, [a change in requirements in 2019 increased the reproducibility from a horrid \~6% to 68%](https://doi.org/10.1287/mnsc.2023.03556).
* At its core, replication seeks to verify the results of earlier research. Complete verification may often also require regathering data and using complementary methods. However, everything starts with reproducibility and transparency, i.e. the ability of would-be-replicators to understand what you did, and to, if they want, re-run your analyses exactly as you did, verifying/modifying only the parts they want (e.g. to check where the statistical errors come from in the above example, and whether the results still hold if you correct for that source of error in the process)
* To ensure the reproducibility of research, one needs to provide, to an unknown external person in the future, as transparent as possible access to a) the data and b) the research process that yielded the results reported. The most transparent way to do this is of course to openly archive into a long-term facility both data as well as the process, including e.g. the exact program codes you used to run your analyses if you did computational analyses (however, note also that just bare code is never enough, in addition you need a thorough description of your process from start to finish!)
* At the same time, the mantra is "As open as possible, as closed as necessary", so if you can't share something due to e.g. privacy or intellectual property rights concerns, then so be it (for proper research work, there are also solutions where you can archive this stuff in a non-open fashion, making it available only for legitimate reproduction research)
* How all of this relates to the final project is that Zenodo is an open long-term archival service for all kinds of things. So, I want you to return your stuff in such a long-term-preserved open archive that is also citable through a DOI (Digital Object Identifier). At the same time, Zenodo isn't that good for actually viewing the content. So for this, I'm asking you to have the master data, code and documentation in GitHub, which /is/ a platform geared toward easily looking through e.g. data processing code (in addition, GitHub is great for iterative work, so you can see [changes in the code/data through time](https://github.com/dfalster/baad/commits/master), as well as collaborative work, where multiple people can work on the same thing in a [controlled, productive manner](https://github.com/dfalster/baad/issues). As this is a solo project, we'll not be delving into these capabilities here, but it's still good to be aware of them. If you want to learn more about Git, upon which GitHub is based, head e.g. [here](https://swcarpentry.github.io/git-novice/))
* So, to reiterate, what I'm looking for here is an as complete and transparent as possible view into what you did that would theoretically allow me to follow the same exact steps you took. This includes codes and data ("You need to document your pipeline in a way that it can be rerun and its results reproduced"), but also very importantly a textual description, "a clear, logical description of your whole research process that will enable it to be critiqued and reproduced in full" (quoting directly from the evaluation criteria. If you want to learn more about reproducible computational research, see for example [this tutorial](https://coderefinery.github.io/reproducible-research/). As an example of how these research processes can be shared openly more generally, check out for example [protocols.io](https://www.protocols.io/view/de-novo-transcriptome-assembly-workflow-ghebt3e)).

### Submissions from previous years

To further aid you in your work, here are some previous submissions for inspiration (for most of them, you should actually click the GitHub link on the right to start to make sense of them):

* Errors in machine translating Finnish surnames - DOI: [10.5281/zenodo.7469559](https://doi.org/10.5281/zenodo.7469559)
* Themes in Hungarian folk love songs - DOI: [10.5281/zenodo.44570](http://doi.org/10.5281/zenodo.44570)
* Languages used in Dutch Golden Age correspondence - DOI: [10.5281/zenodo.10932274](https://doi.org/10.5281/zenodo.10932274)
* A tool for comparing different editions of the same book - DOI: [10.5281/zenodo.10415253](https://doi.org/10.5281/zenodo.10415253)
* An analysis of Finnish milk propaganda - DOI: [10.5281/zenodo.10419360](https://doi.org/10.5281/zenodo.10419360)
* Sentiment analysis of wall inscriptions found in Pompeii - DOI: [10.5281/zenodo.10395676](https://doi.org/10.5281/zenodo.10395676)
* Differences and similarities in the depiction of ghosts in two Chinese novels from different eras - DOI: [10.5281/zenodo.7467017](https://doi.org/10.5281/zenodo.7467017)
* Theories of consequence in early English books (1473-1700) - DOI: [10.5281/zenodo.5800084](https://doi.org/10.5281/zenodo.5800084)
* Extracting and visualizing biographical information from an old bank matricle - DOI: [10.5281/zenodo.225890](http://doi.org/10.5281/zenodo.225890)
* Analysis of a survey on user involvement in software development - DOI: [10.5281/zenodo.237727](https://doi.org/10.5281/zenodo.237727)
* Comparing Language Complexity in Fact-Checked Fake and Real News - DOI:[ 10.5281/zenodo.4327219](https://doi.org/10.5281/zenodo.4327219)
* Polite vs casual address form use by Finnish language learners in different situations - DOI: [10.5281/zenodo.218844](https://doi.org/10.5281/zenodo.218844)
* Are people on the Internet more rude at night? - DOI: [10.5281/zenodo.10418513](https://doi.org/10.5281/zenodo.10418513)
* Discovering patterns in chalcolithic and early bronze age burials in northeast England- DOI: [10.5281/zenodo.215932](https://doi.org/10.5281/zenodo.215932)
* Finnish politicians in pictures - biases in the contents of the Finna portal - DOI:[ 10.5281/zenodo.4313215](https://doi.org/10.5281/zenodo.4313215)
* Analysing the poets and themes selected for the book "Three Hundred Tang Poems" - DOI: [10.5281/zenodo.5796611](https://doi.org/10.5281/zenodo.5796611)
* Analysing the composition of the collection of the Metropolitan Art museum - DOI: [10.5281/zenodo.8076250](https://doi.org/10.5281/zenodo.8076250)
* Images of the human body across four Japanese novels - DOI: [10.5281/zenodo.10420251](https://doi.org/10.5281/zenodo.10420251)
* Themes discussed in Helsingin Sanomat in 1905 - DOI: [10.5281/zenodo.44572](http://doi.org/10.5281/zenodo.44572)
* Topics covered in Finnish proverbs from the 1930s - DOI: [10.5281/zenodo.6365445](https://doi.org/10.5281/zenodo.6365445)
* Differences in use between the words _maahanmuuttaja_ and _pakolainen_ in Finnish newspapers 1970- to present - DOI: [10.5281/zenodo.44544](http://doi.org/10.5281/zenodo.44544)
* Differences in how Australian and Indian news discuss violence against women - DOI: [10.5281/zenodo.10419406](https://doi.org/10.5281/zenodo.10419406)
* Differences in how frequently Finnish and Swedish newspapers talk about the Romani people - DOI: [10.5281/zenodo.44590](http://doi.org/10.5281/zenodo.44590)
* Contrasting Beck's lyrics to blues lyrics - DOI: [10.5281/zenodo.215292](http://doi.org/10.5281/zenodo.215292)
* Extracting and analysing recipe information in an old cookbook - DOI: [10.5281/zenodo.216232](https://doi.org/10.5281/zenodo.216232)
* Comparing the use of polite plural "you" in Mandarin Chinese and Lithuanian - DOI: [10.5281/zenodo.1134294](https://doi.org/10.5281/zenodo.1134294)
* A thematic analysis of the discussion around Guggenheim on the Suomi24 forum - DOI: [10.5281/zenodo.217719](https://doi.org/10.5281/zenodo.217719)
* Foci of climate change media discourse in the Southern China Morning Post 2016-2017 - DOI: [10.5281/zenodo.10866841](https://doi.org/10.5281/zenodo.10866841)
* Sentiment analysis of Twitter discussion related to the Indian biometric identifier system Aadhaar - DOI: [10.5281/zenodo.1134623](https://doi.org/10.5281/zenodo.1134623)
* Exploring themes in Helsinki tourist brochures 1967-2008 - DOI: [10.5281/zenodo.6045173](https://doi.org/10.5281/zenodo.6045173)
* Differences in language between texts dealing with altered states of mind and normal fiction - DOI: [10.5281/zenodo.230676](https://doi.org/10.5281/zenodo.230676)
* Social relations as expressed in District Court Sessions of Iisalmi parish 1639-1651 - DOI: [10.5281/zenodo.4327155](https://doi.org/10.5281/zenodo.4327155)
* Analysing the composition of print and audio book versions of the New York Times bestseller lists - DOI: [10.5281/zenodo.5795399](https://doi.org/10.5281/zenodo.5795399)
* Preliminary analysis of Free Direct Speech in _Se tapahtui täällä_ by Raija Siekkinen - DOI:[ 10.5281/zenodo.4338190](https://doi.org/10.5281/zenodo.4338190)
* Exploring ways to compare adaptations of a literary work - DOI: [10.5281/zenodo.1127754](http://doi.org/10.5281/zenodo.1127754)
* Preliminary analysis comparing different Finnish cabinet strategies against each other - DOI: [10.5281/zenodo.216604](https://doi.org/10.5281/zenodo.216604)
* Preliminary analysis of patterns in the holdings of the Finnish National Gallery - DOI: [10.5281/zenodo.218735](https://doi.org/10.5281/zenodo.218735)
