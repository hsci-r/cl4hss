# Data processing: fundamental concepts of programming for humanists

{% hint style="danger" %}
This content is not yet complete
{% endhint %}

Presentation: [Data processing: fundamental concepts of programming for humanists](https://docs.google.com/presentation/d/e/2PACX-1vSZSb9hmeRG5vTENcKe7WE8k9Uu32xPgTICPz2-Cw8O5Zssqitv-XfNC6wVLf215sod18n4wGMLoyIx/pub?start=false&loop=false&delayms=3000) \([pdf](http://docs.google.com/presentation/d/1Hor0RqZTZEV-77gdwZPgCpz8MlX4ZmsIwSyGcCDi3Ks/export/pdf), [gd](https://docs.google.com/presentation/d/1Hor0RqZTZEV-77gdwZPgCpz8MlX4ZmsIwSyGcCDi3Ks/edit?usp=sharing)\)

This part of the course is an attempt to distil the **absolute minimum understanding** needed for someone from a humanities background to start delving into programming by reading and dissecting ready-made examples that abound on the Internet. 

Being the absolute minimum, it is much, much shorter than most introductory programming courses for the humanities. Indeed, instead of teaching programming, it endeavours to only transfer knowledge of the absolute core **fundamental concepts of programming**. By focusing intently on this core set \(and providing a [cheatsheet](https://mybinder.org/v2/gh/jiemakel/dhintro/master?filepath=programming_cheatsheet.ipynb) of them\), it is hoped that the reader is better able to relate the concepts to each other, and form a unified general understanding of the constructs appearing in all programs.

The core idea behind this is that nowadays, for everything in data processing or visualisation one wants to do, there is a library \(e.g. [Pandas](http://pandas.pydata.org/), [Tidyverse](https://www.tidyverse.org/packages/), [Mallet](http://mallet.cs.umass.edu/), [LDAvis](https://cran.r-project.org/web/packages/LDAvis/README.html), [Matplotlib](http://matplotlib.org/), [Requests](http://docs.python-requests.org/en/latest/), [tm](https://cran.r-project.org/web/packages/tm/index.html), [plotly](https://plot.ly/)\). So, nowadays, programming is mostly reading up how on to use these libraries from their documentation, and writing glue code to hook them together to perform what one wants. To drive this point home, consider the two programs below. The first prints some statements, the second imports a bunch of libraries, and then uses them to fetch the text of Pride and Prejudice from the Internet, to apply statistical topic modeling to it and to interactively visualise the results.

{% code-tabs %}
{% code-tabs-item title="hello\_world.py" %}
```python
print("Hello World!")
print("Hello Again")
print("I like typing this.")
print("This is fun.")
print('Yay! Printing.')
print("I'd much rather you 'not'.")
print('I "said" do not touch this.')
```
{% endcode-tabs-item %}
{% endcode-tabs %}

{% code-tabs %}
{% code-tabs-item title="output:" %}
```text
Hello World!
Hello Again
I like typing this.
This is fun.
Yay! Printing.
I'd much rather you 'not'.
I "said" do not touch this.
```
{% endcode-tabs-item %}
{% endcode-tabs %}

{% code-tabs %}
{% code-tabs-item title="model\_pride.py" %}
```python
import requests
import re
from gensim.parsing.preprocessing import remove_stopwords
from gensim.corpora.dictionary import Dictionary
from gensim.models.ldamodel import LdaModel
import pyLDAvis
import pyLDAvis.gensim

pride_and_prejudice = requests.get("http://www.gutenberg.org/cache/epub/42671/pg42671.txt").text
paragraphs = [re.split(r"\W+",remove_stopwords(paragraph)) for paragraph in re.split(r"\r\n\r\n",re.sub(r"CHAPTER [XIV]+\.","",pride_and_prejudice[pride_and_prejudice.index("CHAPTER I."):pride_and_prejudice.index("***END OF THE PROJECT GUTENBERG EBOOK PRIDE AND PREJUDICE***")]))]
d = Dictionary(paragraphs)
c = [d.doc2bow(paragraph) for paragraph in paragraphs]
m = LdaModel(c,num_topics = 15, alpha='auto')
pyLDAvis.display(pyLDAvis.gensim.prepare(m,c,d))
```
{% endcode-tabs-item %}
{% endcode-tabs %}

Gluing the libraries together to a working pipeline is mostly done through trial and error, and lots of googling. However, in order to understand the documentation and examples, knowledge of the fundamental universal concepts of programming is required.

To further force focus onto the conceptual level, the concepts are taught concurrently in multiple programming languages. This way, one better learns the concept, instead of just the peculiarities of their implementation in a specific language.

Many other programming courses for the humanities start with installing a local version of a programming language, and possibly also an editor environment. The reasoning behind this is often that this is the way actual programmers program, and thus it is useful to familiarise people with the proper environment right off the bat. However, doing so also introduces a lot of extraneous complexity to the course. Thus, this course instead makes use of [Jupyter](http://jupyter.org/) notebooks as the programming environment of choice. Jupyter notebooks are interactive notebooks that mix textual and code cells in an interactive manner, which is great for introducing programming concepts in bite-sized chunks \(they also happen to be useful building blocks for [literate programming](https://en.wikipedia.org/wiki/Literate_programming) and [reproducible research](https://ropensci.org/blog/2014/06/09/reproducibility/), both important concepts in themselves for data scientists\). While Jupyter tools can also be installed locally, the Jupyter ecosystem also has the advantage of being able to provide readily configured temporary environments straight on the web. An environment configured for this course can be started at [https://mybinder.org/v2/gh/jiemakel/dhintro/master](https://mybinder.org/v2/gh/jiemakel/dhintro/master).

To start with, the repository contains first two  notebooks that describe these core concepts in the two programming languages currently most relevant to data science: [Python](http://python.org/) and [R](https://www.r-project.org/).To open them, you either need to install the [nteract](https://nteract.io/) app, or just use a temporary web instance at .

The two notebooks, [python\_intro.pynb](https://raw.githubusercontent.com/jiemakel/dhintro/master/python_intro.ipynb) \(right click on the link, choose save as and then upload into Jupyter\) and [r\_intro.pynb](https://raw.githubusercontent.com/jiemakel/dhintro/master/r_intro.ipynb) \(do the same\) are intended to be viewed and progressed through side by side \(in two browser windows\). 



After the two introductory notebooks, the reader is advised to move on to [korp.pynb](https://raw.githubusercontent.com/jiemakel/dhintro/master/korp.ipynb), which contains an actual, relatively simple process where data is sourced, transformed and then visualized. This notebook also contains tasks for the reader that are typical of what one will encounter when doing similar processing on one's own.

Other notebooks of interest include [shakespeare.ipynb](https://raw.githubusercontent.com/jiemakel/dhintro/master/shakespeare.ipynb) as well as a [reference cheatsheet](programming_cheatsheet.ipynb) to server as a memory aid on the core concepts learned \(available also as a [downloadable notebook](https://raw.githubusercontent.com/jiemakel/dhintro/master/programming_cheatsheet.ipynb)\). A final notebook is [python\_figure\_out.ipynb](https://raw.githubusercontent.com/jiemakel/dhintro/master/python_figure_out.ipynb), where the exercise is to figure out what is actually going on in the program using the instructions given in the reference cheatsheet.

[http://fredgibbs.net/posts/coding-in-the-humanities](http://fredgibbs.net/posts/coding-in-the-humanities): as I continue to experiment with various text mining projects, and continue to fiddle with my digital history course, I am now convinced that basic techniques for data manipulation should be taught as part of the humanities curriculum. Firstly, it’s as fundamental as any other skill related to reading texts \(broadly conceived\), including sorting and organizing source material. Of course not all humanists use texts as their primary object of inquiry, but because textual sources often feature prominently \(if not exclusively\) in research, humanists in general have much to gain by learning how to manipulate the growing body of digital texts with simple but powerful tools. Secondly, not only is data manipulation not antithetical to humanistic research methodology, but it facilitates exactly what the humanities are about: embracing multiple perspectives and engaging with source material in multiple ways. As more and more sources become available online as data \(not just as images\), humanists need tools to manage and explore it. As Ann Blair has recently described of the early modern period, information overload is hardly a new problem. But if the problem of abundance worries the humanist who relies on project-delimiting scarcity, it is a problem to be embraced rather than avoided.

[https://link.springer.com/content/pdf/10.1007/BF02402344.pdf](https://link.springer.com/content/pdf/10.1007/BF02402344.pdf) In the Report of the Conference on Computer Technology in the Humanities 1 the committee on courses and curricula concluded that a first course in computer programming in the humanities should "provide extensive instruction and practice in programming. Insofar as possible, programming should be taught algorithmically ... rather than as aspects of a specific programming language. Such algorithms ... provide an abstract structure onto which any given programming language can be mapped. Hence, the logical aspect of programming, rather than the details of a programming language, is given primary emphasis, and thus the inevitable shifts from one programming language to another necessitated by a change in computer or in research goals are facilitated." \([in context](https://hyp.is/weuQ4s07EeiHoNf0oO2VNA/link.springer.com/content/pdf/10.1007/BF02402344.pdf)\)

A key problem in learning to program is frustration. There are few things so frustrating as being told that a comma is missing and then having tO wait 20 minutes before it can be fixed - or receiving an error message that requires the combined heads of two systems analysts to decode.

Logical errors - those where the actions of the program do not meet the intent of the programmer - are another matter. If logical errors were impossible, there would be nothing to learn in programming. To help correct logical errors FLOW provides a powerful trace feature. This feature allows the program to be executed one line at a time with the results of each line's execution immediately seen and the program corrected if necessary. The trace is detailed below.

## Assignments

1. the [Python intro -part](https://github.com/jiemakel/dhintro/blob/master/python_intro.ipynb) of the [fundamental concepts of programming for humanists](https://github.com/jiemakel/dhintro/)
2. the [waiwa assignment](https://github.com/jiemakel/dhintro/blob/master/waiwa.ipynb), including the [OpenRefine subpart](https://docs.google.com/document/d/1m6EEbPCSnjg6F1VPBj4sa8NNnMWPGduXqirGwXirDxI/edit) of the [fundamental concepts of programming for humanists](https://github.com/jiemakel/dhintro/)
3. the [figure out assignment](https://github.com/jiemakel/dhintro/blob/master/python_figure_out.ipynb)
4. the [regex tutorial](https://regexone.com/) and the [regex assignment](https://regex101.com/r/6439eo/1) \(create regexes to match first names, last names, years, birth places etc\)

