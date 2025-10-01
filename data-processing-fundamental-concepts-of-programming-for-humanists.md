# Data processing: fundamental concepts of programming for humanists and social scientists

This part of the course is an attempt to distil the **absolute minimum understanding** needed for someone from a humanities background to start delving into programming by reading and dissecting ready-made examples that abound on the Internet.

{% hint style="info" %}
Context note: this is a self-contained part of the [computational literacy for humanities and social sciences course](./). You can use this to teach yourself the fundamentals of programming, allowing you to then pursue further knowledge in the form of tutorials or more in-depth courses. On the other hand, should you want to know why programming would or would not be useful to you, you'll need to read up on most of the course.
{% endhint %}

## The fundamental concepts of programming

Being the absolute minimum, it is much, much shorter than most introductory programming courses. Indeed, instead of teaching programming, it endeavours to only transfer knowledge of the absolute core **fundamental concepts of programming**. By focusing intently on this core set (and providing a [cheatsheet](https://nbviewer.jupyter.org/github/jiemakel/dhintro/blob/master/programming_cheatsheet.ipynb) of them), it is hoped that the reader is better able to relate the concepts to each other, and form a unified general understanding of the constructs appearing in all programs.

The core idea behind this is that nowadays, for everything in data processing or visualisation one wants to do, there is a library – ready, prepackaged functionality that you can call from your code to accomplish what you want. For example, there is [spaCy](https://spacy.io/), [Stanza](https://stanfordnlp.github.io/stanza/index.html),  [🤗 Transformers](https://huggingface.co/transformers/quicktour.html) and [NLTK](https://www.nltk.org/) for language processing, [tm](https://cran.r-project.org/web/packages/tm/index.html) for text mining, [STM](https://www.structuraltopicmodel.com/), [Gensim](https://radimrehurek.com/gensim/), [Mallet](http://mallet.cs.umass.edu/), [scikit-learn](https://scikit-learn.org/stable/) or [LDAvis](https://github.com/cpsievert/LDAvis) for topic modelling and other statistical analysis, [Pandas](http://pandas.pydata.org/) or [Tidyverse](https://www.tidyverse.org/packages/) for wrangling tabular data, [Seaborn](https://seaborn.pydata.org/), [Matplotlib](http://matplotlib.org/), [ggplot2](https://ggplot2.tidyverse.org/) or [plotly](https://plot.ly/) for plotting, [Requests](http://docs.python-requests.org/en/latest/) for accessing APIs and web resources, and so on and so on.&#x20;

So, nowadays, programming is mostly reading up how on to use these libraries from their documentation, and writing glue code to hook them together to perform what one wants. To drive this point home, consider the two programs linked [here](http://nbviewer.jupyter.org/github/jiemakel/dhintro/blob/master/modern_programming.ipynb). The first prints some statements, the second imports a bunch of libraries, and then uses them to 1) fetch the text of Pride and Prejudice from the Internet, 2) to apply statistical topic modelling to it and 3) to interactively visualise the results in a similar amount of lines.

Glueing the libraries together to a working pipeline is mostly done through trial and error, and lots of googling. However, in order to be able to read and understand the documentation and examples, knowledge of the fundamental universal structures and concepts of programming is required.&#x20;

Many other programming courses for the humanities start with installing a local version of a programming language, and possibly also an editor environment. The reasoning behind this is usually that this is the way actual programmers program, and thus it is useful to familiarise people with the proper environment right off the bat. However, doing so also introduces a lot of extraneous complexity to the course.&#x20;

Thus, this course instead makes use of [Jupyter](http://jupyter.org/) notebooks as the programming environment of choice. Jupyter notebooks are interactive notebooks that mix textual and code cells in an interactive manner, which is great for introducing and experimenting with programming concepts in bite-sized chunks (funnily enough, they also exhibit many of the qualities desired in [this article](https://hyp.is/Ap-aFs08EeinplOX3_QUrQ/link.springer.com/content/pdf/10.1007/BF02402344.pdf) from 1974 of an environment for teaching programming in the humanities. In addition, they also happen to be useful building blocks for [literate programming](https://en.wikipedia.org/wiki/Literate_programming) and [reproducible research](https://ropensci.org/blog/2014/06/09/reproducibility/), both important concepts in themselves for data scientists).&#x20;

While Jupyter tools can be installed locally, the Jupyter ecosystem also has the advantage of being able to provide readily configured temporary environments straight on the web. An environment configured for this course can be started merely by going to [https://mybinder.org/v2/gh/jiemakel/dhintro/master](https://mybinder.org/v2/gh/jiemakel/dhintro/master) (and waiting a bit for it to load).

Another reason for favouring a ready environment is that on this course, to further force focus onto the conceptual level, the concepts are taught concurrently in multiple programming languages. This way, one better learns the concepts, instead of just the peculiarities of their implementation in a specific language.

To start with, two notebooks describe the core concepts in the two programming languages currently most relevant to data science: [Python](http://python.org/) and [R](https://www.r-project.org/).&#x20;

{% hint style="info" %}
**Assignment:**&#x20;

1. Work through the [python\_intro.ipynb](https://mybinder.org/v2/gh/jiemakel/dhintro/master?filepath=python_intro.ipynb) and [r\_intro.ipynb](https://mybinder.org/v2/gh/jiemakel/dhintro/master?filepath=r_intro.ipynb) notebooks. The notebooks are intended to be viewed and progressed through side by side, section by section in two parallel browser windows.
2. After going through the concepts this way, open up the final [Scala](https://www.scala-lang.org/) language version of the fundamentals ([scala\_intro.ipynb](https://mybinder.org/v2/gh/jiemakel/dhintro/master?filepath=scala_intro.ipynb)), and go through it once more comparing it to the earlier two languages. Can you see how the fundamental concepts stay the same between the languages, even when syntax and particulars differ?
{% endhint %}

After going through the above notebooks, and arming yourself with the summary [cheatsheet](https://nbviewer.jupyter.org/github/jiemakel/dhintro/blob/master/programming_cheatsheet.ipynb), you should now be able to understand programming tutorials, library documentation as well as be able to figure out on a conceptual level what some code is doing. So, let's test this:

{% hint style="info" %}
**Assignment:**

1. Go through and try to understand [korp.ipynb](https://mybinder.org/v2/gh/jiemakel/dhintro/master?filepath=korp.ipynb), which contains an actual, relatively simple process where data is sourced, transformed and then visualised. This notebook also contains three simple tasks for the reader that are typical of what one will encounter when trying to modify and glue together other people's sample code and libraries to accomplish your own goals (when doing this and later exercises, do note that the Jupyter environments on Binder are temporary, so if you need to return to the exercise later, you'll need to download the notebook for safekeeping after concluding a work session on it, and then upload it back when you want to resume). If you want more exercise in reading and understanding code, also go through [shakespeare.ipynb](https://mybinder.org/v2/gh/jiemakel/dhintro/master?filepath=shakespeare.ipynb), which is a notebook version of [this tutorial](https://web.archive.org/web/20201025013909/https://datawookie.netlify.app/blog/2013/09/text-mining-the-complete-works-of-william-shakespeare/).
2.  Select a library of relevance to computational humanities (for example [spaCy](https://spacy.io/), [Stanza](https://stanfordnlp.github.io/stanza/index.html),  [🤗 Transformers](https://huggingface.co/transformers/quicktour.html), [NLTK](https://www.nltk.org/), [tm](https://cran.r-project.org/web/packages/tm/index.html), [STM](https://www.structuraltopicmodel.com/), [Gensim](https://radimrehurek.com/gensim/), [scikit-learn](https://scikit-learn.org/stable/), [LDAvis](https://github.com/cpsievert/LDAvis), [Pandas](http://pandas.pydata.org/), [Tidyverse](https://www.tidyverse.org/packages/), [Seaborn](https://seaborn.pydata.org/), [Matplotlib](http://matplotlib.org/), [ggplot2](https://ggplot2.tidyverse.org/), [plotly](https://plot.ly/), [Requests](https://requests.readthedocs.io/en/master/)). Find answers to the following questions about it, and post them on Slack:

    1. What does the library do? For what tasks would it be useful?
    2. What type of data does the library take in?
       1. What information does the input data need to contain?
       2. What concrete format and structure does the input data need to conform to?
       3. What is the format and structure of the output?

    If someone has already posted on the library you chose, don't repeat them. Instead, add to what they've said in a thread.
3. Figure out what [this code](https://mybinder.org/v2/gh/jiemakel/dhintro/master?filepath=python_figure_out.ipynb) does and how it does it. Post answers as private messages to Eetu on Slack.
{% endhint %}

### What is left out

The fundamentals on this course leave out things very important to programming in general. The most important of these is how to design and organise code into conceptually clear, modular and reusable units such as classes, packages and libraries. The reason this is left out is that while they are of the utmost importance when designing large, long-lived, multipurpose code, such considerations are of much lesser import for the kind of one-off glue code that a data scientist, computational social scientist or digital humanities scholar usually needs. You will also passively learn proper organisation practices by reading the documentation of quality libraries, and by going through other peoples code.

Similarly, as already discussed, this course uses Jupyter notebooks for writing and running code. In contrast, "proper software" is usually developed in dedicated editors (IDEs = [Integrated Development Environments](https://coderefinery.github.io/IDEs/01-introduction-to-dev-tools/)), which provide robust local support for writing, testing and packaging software. In addition, this introduction doesn't cover any of [automated testing](https://coderefinery.github.io/testing/), code review, [continuous integration](https://coderefinery.github.io/automation/), or [distributed version control](https://coderefinery.github.io/git-collaborative/), which are all important concepts in software development in general (however, to version management we will return later in the chapter on [open, reproducible research and publishing](three-approaches-to-methods-for-digital-humanities-work-area/open-reproducible-research-and-publishing.md)).

### Dig deeper

Finally, if working with international textual data containing ümläüts, áccênts, or symbols from completely different character sets such as Hangul or Kanji, you may encounter problems with a thing called _encoding_, namely that such characters may become garbled, particularly when moving data between environments and languages. If this happens, [this post](http://kunststube.net/encoding/) will get you up to speed on what's happening at the conceptual level, after which you'll be able to google for help relating to your particular environment.

{% hint style="info" %}
**Assignment:**

Despite sharing fundamental concepts, different programming languages do also have conceptual-level differences. For example, Scala is 1) strongly typed, 2) very object-oriented, and 3) has a rich collection of (higher-order) data transformation functions that take in pieces of code as parameters. What effects do these traits have on programming in the language as compared to Python (dynamically typed, not object-oriented at its core \[but e.g. the data wrangling library [Pandas](http://pandas.pydata.org) highly object oriented], few higher-order functions) or R (dynamically typed, for the most part not object-oriented, support for a limited selection of code parameters only inside certain environments such as the data wrangling library [tidyverse](http://tidyverse.org))? To aid you in pondering this question, look back to the reference and introduction notebooks, as well as consult [programming\_styles.ipynb](https://mybinder.org/v2/gh/jiemakel/dhintro/master?filepath=programming_styles.ipynb) for a more in-depth introduction to functional programming. Post your answers as private messages to Eetu on Slack.
{% endhint %}

## Further resources

* [The Historian’s Macroscope](http://www.themacroscope.org/?page_id=584), a good general-purpose book
* [Computational and Inferential Thinking - The Foundations of Data Science](https://www.inferentialthinking.com/), an excellent introduction to statistical  analysis with interactive Python notebooks
* [Data analysis with Python](https://csmastersuh.github.io/data_analysis_with_python_2020/), a slightly technical but very from-the-ground-up introduction to important libraries and tools for data analysis in Python
* [Introduction to Programming for Digital Humanities](https://rage.github.io/programming-digital-humanities/), the University of Helsinki introductory Python programming course for the humanities
* [Python Programming for the Humanities](http://fbkarsdorp.github.io/python-course/), the best external introduction to programming for humanists that I could find
* [R short and sweet](https://www.datacamp.com/courses/r-short-and-sweet) at DataCamp (a part of the [Introduction to Open Data Science MOOC](https://mooc.helsinki.fi/course/view.php?id=158) at the University of Helsinki)
* [Statistical Inference via Data Science: A ModernDive into R and the Tidyverse!](https://moderndive.com/index.html), a very good and clear resource introducing both statistical concepts, as well as how to apply them in practice in R and Tidyverse. Not an introduction to programming but an excellent follow-up.
* [R for Social Scientists](https://datacarpentry.org/r-socialsci/), an R tutorial, not really anything specific to social science
  * Especially the following are good parts:
    * [Tidy data manipulation](https://datacarpentry.org/r-socialsci/03-dplyr-tidyr/)
    * [Data visualisation with ggplot2](https://datacarpentry.org/r-socialsci/04-ggplot2/index.html)
* [The Programming Historian](http://programminghistorian.org/), lessons and tutorials for doing various DH things
* [Eloquent Javascript](http://eloquentjavascript.net/), a nicely built general, interactive introduction to programming



