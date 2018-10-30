# Introduction: three approaches to methods for digital humanists

{% hint style="danger" %}
This content is not yet complete
{% endhint %}

## All the different digital humanities

There is no single digital humanities. Instead, it is often used as a tactical term:

> To assert that digital humanities is a “tactical” coinage is to insist on the reality of circumstances in which it is unabashedly deployed to get things done—“things” that might include getting a faculty line or funding a staff position, establishing a curriculum, revamping a lab, or launching a center.
>
> _— Kirschenbaum, M. \(2012\). Digital Humanities As/Is a Tactical Term. In M. K. Gold \(Ed.\), Debates in the Digital Humanities \(_[_in context_](https://hyp.is/bNjpythNEeiDfqOwZfYFKg/dhdebates.gc.cuny.edu/debates/text/48)_\)_

On a global level, this results in digital humanities as a field being comprised of a complex landscape of _partially_ overlapping domains, including e.g. humanities computing, multimodal cultural heritage and digital culture studies. Crucially, while each of these subcamps have aspects in common with their neighbours, who have things in common with their neighbours, these connections do not extend uniformly across the whole landscape. Therefore, it makes sense to think about, and clearly explicate the subsets of digital humanities meant in each particular context.

In the context of this course, three viewpoints into methods will be considered:

## Three approaches to methods for digital humanities - what to learn if you're a humanist?

1. Knowledge of easy to use end-user data processing and visualization tools
   * Easy to use for their intended purpose, but limited
2. Knowledge of the fundamentals concepts of programming
   * Frees you to process your data more efficiently
   * Allows you to more freely apply visualizations etc based on ready libraries and tutorials on the Internet
3. High-level understanding of what types of things can be accomplished with advanced CS methods
   * To be able to communicate in collaborative projects

In the following, we will discuss where these approaches come from,  and how they relate to each other.

## Digital humanities as humanities computing

> "The digital humanities comprise the study of what happens at the intersection of **computing tools** with cultural artefacts of all kinds. This study begins where basic familiarity with standard software ends. It probes how these common **tools** may be used to make new knowledge from our cultural inheritance and from the contemporary world. It equips students to analyze problems in terms of **digital methods**, choose those best for the job at hand, apply them creatively and assess the results. It teaches students to use **computing as an instrument** to investigate how we know what we know, hence to strengthen and extend our knowledge of the world past and present."
>
>  _— Center for Computing in the Humanities. "Introduction to the Digital Humanities". King's College London._ 13 January 2006 \([in context](https://hyp.is/A3betthREeiK4hfqTp5pCg/web.archive.org/web/20060114101653/http://www.kcl.ac.uk:80/schools/humanities/cch/digihum), replaced in 2011 with a much more [generic description](http://web.archive.org/web/20111204033346/http://www.kcl.ac.uk:80/artshums/depts/ddh/about/dh.aspx)\)

According to the above definition, digital humanities can be seen as the application of computation to yield new knowledge on phenomena of interest to scholars in the humanities. Congruent to this definition, many discussions seeking a history for digital humanities name the work of Roberto Busa as a progenitor of the field. In 1949, Busa pitched to IBM the novel idea of using general purpose computers to create an index of the words appearing in Thomas Aquinas's works \(see e.g. [this article](http://www.historyofinformation.com/expanded.php?id=2321) for a detailed historical account of the project\). 

At the same time, while Busa did manage to significantly decrease the labour in crafting such an index, his work is also already part of long traditions. To pick two examples, already in 1890, the U.S. Census was recorded on punch-cards and tabulated automatically, while already in 1887 T. C. Mendenhall suggested that quantitative analysis of texts \(in this case, word length\) could be used to determine their authorship. Indeed, indices such as Busa's had also already been compiled, both manually as well as through partial automation.

Thus, the birth of humanities computing as a field can also be seen just arising organically out of already existing \(quantitative\) approaches to humanities questions, made possible or at least vastly less labour intensive by the development of general purpose computers.

In any case, by the mid 1960's, the field was already well defined, as testified by the establishment, in 1966, of the journal "Computers and the Humanities" \(in 2005 renamed to "Language Resources and Evaluation"\). In the [first volume](https://link.springer.com/journal/10579/1/1/) of the journal, in [an announcement on the third ACLS Program for Computer Studies in the Humanities](http://doi.org/10.1007/BF00188012), one even finds the following statement:

> The Council has not considered, even if funds continue to be available, when it will bring its current program to a close. One can explore for just so long. Then it will seem that nothing more or nothing of special interest is going to turn up, and that better uses for the always limited resources should be found.
>
>  — _The ACLS program for computer studies in the humanities: Notes on computers and the humanities_, Computers and the Humanities, September 1966, Volume 1, Issue 1, page 9 \([in context](https://hyp.is/deB2BNhdEeiDziep2xxgAg/link.springer.com/content/pdf/10.1007/BF00188012.pdf)\)

Particularly singled out as "already solved" are stylistic literary analyses and quantitative historical studies:

> For instance, many excellent plans to study a writing style, or to compare two styles, or even to study "influences" propose a use of computers which is routine, and too routine for an award in a program aimed at feeling for what new uses of computers there might be. Even many of those historical studies which collect and order vast quantities of information, say, about the members of an assembly or a voting group are now so settled in their method that, again, only if a proposal is of special moment is there much chance that it will receive support. 
>
> — The ACLS program for computer studies in the humanities: Notes on computers and the humanities, Computers and the Humanities, September 1966, Volume 1, Issue 1, page 8 \([in context](https://hyp.is/rdNu5s4WEeihKDcztm1ZWQ/link.springer.com/content/pdf/10.1007%2FBF00188012.pdf)\)

### Whatever happened to humanities computing?

At the same time, the texts in the first volume of the Computers and the Humanities journal reflect hopes on how computers could and should transform the humanities as a whole. For example, the same announcement states:

> We don't know what shapes studies in the humanities will take in ten or twenty years. Even our ideas about kinds of studies are changing now. The overlap of fields and departments of study seems only a surface over deeper stirrings. \([in context](https://hyp.is/FD-zEtjxEeiDvG_D9GElgA/link.springer.com/content/pdf/10.1007/BF00188012.pdf)\)
>
> ....
>
> We don't know, of course, what the further subtleties will be as formalities are probed still more, how computers will incorporate them, or how the thought and instrument will enter and affect the humanities. For a long while, perhaps, the traditional or institutional divisions in the humanities will stay steady, so that within the established departments, along with other studies, there will also be some formalistic ones — studies in literature, government or history, for example, done with the aid of computers. It might happen, though, that our divisions themselves will change, that we will have departments of formal or computer studies, and that in these new departments there will be studies _of_ literary and historical and other materials. \([in context](https://hyp.is/j_AkDtjuEeiTIpf6gZVJLw/link.springer.com/content/pdf/10.1007/BF00188012.pdf)\)

Now, over 50 years later, the situation and expectations are seemingly exactly the same with regard to digital humanities. So, what went wrong? Why didn't the promised revolution come? Why would this time be any different?

{% hint style="info" %}
**Assignment:** From the 1966 inaugural issue of "Computers and the Humanities", read the [ACLS announcement](http://doi.org/10.1007/BF00188012) in full, as well as the [prospect](http://doi.org/10.1007/BF00188009) outlining the idea for the journal. Then, browse [this article](https://doi.org/10.2307/203882) from 1983 reflecting on how quantitative history had developed up to that point. Finally, read [this article](https://doi.org/10.4000/diacronie.2795) from 2012. 

Do your own searches and try to dig up the history of quantitative or computational approaches in your own field, and any analyses on how they ended up relating to the core field. 

After going through your sources, reflect on the general questions above from the perspective of your field. Add your hypotheses and insights to the discussion on the course Slack. There is no simple answer.
{% endhint %}

My own take is that on the one hand, there really is nothing new under the sun, apart from continuous incremental improvement. All through history, methodologists have developed better analytical, mathematical, statistical and computational methods for exposing and validating phenomena in data, while others have sought to apply them to whatever material and questions they have had. Which is all as it should be.

Also similarly then as now, these practitioners were not really the ones painting juxtapositions, revolutions and the doom and gloom of traditional scholarship. Instead, right from the start, while they indeed were excited about the prospects offered by computing, they were also mindful of its limitations:

> To imagine future uses for computers in the humanities, we have to remind ourselves of the notions that are central to computer operation, and to think how they might be interpreted even more imaginatively than they have been up till now. One of these notions is the notion of the countable item. A countable item can have a place in an array, be isolated, be combined or removed from combination, and compared with other items. The great advances which have so far been made with computers have been in those fields where we find countable items or have ready substitutes for them. The real or seeming extraneousness of computer studies for the humanities is owed to the fact that, in the humanities, what are most important are, if items at all, items that we can't count, or can count only most artificially. We know, for example, how little definite we mean in saying that we have two or three ideas, that there are four themes in a play, or that there were this or that number of historical events. Our "counting" is not the counting of items that were somehow there separate, waiting to be pointed out; it is a "counting" in which judgments themselves mark out what come to be the items that we count. Apart from the judgments, there are no separate items. Therefore, no technique of counting such items so as to yield, for the first time, a judgment or a summary is possible at all. But, granting that this sort of limitation is inescapable, computers could, it seems, still come to have a more vital use in the humanities than we have seen so far. The first, though the hardest, step in having this come about is simply to find or make countable surrogates for non-countable items \([in context](https://hyp.is/XKUD2s4XEei7uUunrJN3UA/link.springer.com/content/pdf/10.1007%2FBF00188012.pdf)\)

At the same time, for reasons I cannot really explain, this basic interdisciplinary interaction did often end up being cut off in one way or another. Regarding linguistics, computational linguistics branched off from humanities computing to strike out on its own, later further devolving on the one hand into language technology which developed methods seemingly without notion to their use, and on the other hand into corpus linguistics, which stuck to established tools, measures and processes without much ambition to develop them. In social sciences similarly, quantitative statistical explorations were confined into certain subfields, among them economics and population statistics.

Further muddying the waters, with the coming of personal computers in the 1980's and the Internet in the 1990's, what was meant by humanities computing and later digital humanities became muddled, further cutting off our view to this incremental progress of interdisciplinary interaction. All of a sudden, computers were no longer all about computation, but instead aids in all kinds of work, be it using word processors to edit texts, using email to communicate or publishing digital critical editions on the web.

When does then work fall under the heading of humanities computing, and when is the use of a computer incidental? Are you a digital humanist if you use Excel, Email or Word to do your work? 

For this course, the answer will be that whenever you are utilising a computerised process to yield new meaning on questions of import for the humanities, you are engaging in digital humanities. Thus, from the above, at least Excel starts counting immediately after you move from merely entering values in a spreadsheet to summing them across dimensions or projecting them as graphs to better understand them. On the other hand, publishing digital critical editions on the web does not count. But the act of using a computer program to more easily compare versions in the building of such a critical edition does - as does utilising a well designed interface to a multilayered critical edition to yield new insight on the textual tradition.

## What should be taught under humanities computing

This is also not a new question. Already in 1987

[https://doi.org/10.1007/BF00517809](https://doi.org/10.1007/BF00517809)

The Vassar Workshop generated considerable debate on questions such as whether humanities students need to learn programming, whether to teach programming before or after introductory packaged programs, and the depth of knowledge required in related areas such as statistics. The arguments reflected two distinct philosophies concerning the goals of training humanities students in computing

But what should the nature of this training be? This is the question considered by the first panel at the Vassar Workshop. The panelists agreed that computers and the humanities courses must provide two things: \(1\) familiarity with a range of computer applications in humanities disciplines, in order to acquaint students with the range of possibilities for computer use in humanities research as well as methodology; and \(2\) training in computing skills relevant to such applications.

The first of the two extremes may be called the "Holistic View" of computers and the humanities courses. In this view, such courses as introductions to computers and the humanities are a field of study.4 As such, these courses should do what any introductory course should do: provide a broad survey of the field and identify and expound the theoretical principles that inform its methodologies, in order to provide a foundation for further learn- ing and work.5 Emphatically and primarily, they are not intended to provide task-specific information and skills, but instead seek to lay the foundation for a possible lifetime of humanities research activity involving computers.

Substantial treatment of the methodological context and perspective within the humanities is also the basis of research in which the computer can play a role. Also involved is the acquisition of computing skills, but these are taught primarily to convey an understanding of the general principles they illustrate, rather than as ends in themselves.

According to the second view of computers and the humanities courses, the extreme opposite end of my continuum, the content of such courses is primarily intended to provide students with tools and skills to do one or more jobs. The overall intent is to familiarize students with existing tools and provide sufficient skills to enable them to automate phases of fundamentally traditional humanities research

The overall intent is to provide for immediate application of the computer to work and research in the humanities, without necessarily enabling students to develop additional skills later.

### Digital humanities as the programming humanist

"Do you have to know how to code? I’m a tenured professor of digital humanities and I say “yes.” So if you come to my program, you’re going to have to learn to do that eventually." - Stephen Ramsay: Who's In and Who's Out, position paper at the “History and Future of Digital Humanities” panel at the 2011 mla

### Digital humanities as multidisciplinary collaboration

"Our mission is to produce, **through the lens of humanistic inquiry, new modes of thinking in design and computer science** to serve data-driven research in the humanities. We believe that humanistic inquiry, grounded in interpretation, has much to contribute to the development of technologies if they are to help us reveal ambiguity and paradox, allowing human-scale exploration of complex systems." - About -page of the Humanities + Design research laboratory at Stanford

![](https://lh6.googleusercontent.com/lDzpywLdesGvdFy3j3iLkP-Knl9P0sXtqnG2Q1jsaemirxWjea1QeTY_EYN_ITHLwqQE8wvXfiAKU_Coh_63SBl4YOhbGFg7CxNkt_Qb8JFUn3M_pnIROD-l68UhKd5fzGb6w_bd3Q)

{% embed url="http://booksearch.blogspot.fi/2010/12/find-out-whats-in-word-or-five-with.html" %}

![](https://lh5.googleusercontent.com/_U2RpW-zg5_9YRK2kW3SOylyVuCuGHBCjgSCcSIfimwsT1bKF1C-0R0AucLaB9k7zngWOkOTLVpJE3l-yWMiohE2NCQ6WIRe0pzywRXtT2nSZUTO7jYCXakJYZqPuH7Qjn0ONQsEJQ)

![](https://lh4.googleusercontent.com/PMy1_BN_BRO8EFnwGzv2Nz2_E6kEIF2rd29SAZ57hT8hDc7VQPZiVAYu8b4eq7Cxxg8XskD9cMe21vyWmDT05Gcnf9Zf55KtIqbXJgks66RYUpVxr-SX6DtzvwesF9Q3Y-kowjMJbg)

> Scholars who are thinking of "computer projects" need, of course, some notion of what computers can and cannot do. But they need not be formally trained or even deeply knowledgeable about computer theory or technique. The reason for this is that we seem to be coming upon a second stage in using computers in the humanities; it is imagination, if only modestly informed, rather than technical expermess that is most needed now.

## Historical context

file:///Users/jiemakel/Downloads/DigitalHumanitiesPedagogy.pdf “\[technological\] skills training is not research training,” since “the knowledge gained is \[as\] transient” as the tools themselves, whereas “\[critical\] thinking skills are the most important because they are the most deeply embedded and the most transferable.”

[https://link.springer.com/article/10.1007/BF00120965](https://link.springer.com/article/10.1007/BF00120965) Such attitudes can be seen in a person who regards a word processor as something to boost the efficiency of a secretary or in someone who sets out to write an expert system by hiring someone else to do the programming. This tendency to consider the technology as separable from the research or instruction may be fostered by computing and the humanities courses which teach software use or programming in a kind of content-free environment that stresses technique and hopes that desirable and specific applications of the technique will somehow later emerge in students' minds.

On the other hand, when computer scientists entertain the notion of computing and the humanities they tend to regard the activity as somewhat uninteresting, even frivolous. Most computer scientists regard their discipline as primarily one of perfecting approaches to machine computation and they regard problem solving as an abstract task rather than one of developing specific application programs, especially applications in the humanities. In the world of computer science there is not yet an applied computer science specialization, though some engineering schools emphasize applications. If a computer scientist does become involved in humanities research or teaching it is often at a largely technical level, perhaps as a favor to a colleague.

If, for example, a course is taught by two persons, each specializing in either the idea or the technical aspect of the process, this team approach itself quickly communicates the idea that the subject matter being studied cannot easily be handled from a unified perspective by a single person. In other words, the idea is underscored that computing in the humanities is not an identifiable field but a loose, ad hoc amalgamation of at least two fields.

The key to integrating computer science and the humanities is to develop and promote projects and courses for which the involvement of the computer is integral rather than secretarial. In achieving this goal I would insist that some humanists need to develop their understanding of computer science as well as their computer skills and some computer scientists must become more involved in non-technical, humanistic research. The result would be a type of scholar in whom computational and humanistic interests combine to foster new directions and methods on the basis of traditional concerns.

Neural network design affords limitless possibilities to the person who wishes to interrelate humanities and computing

As soon as I had said that it would be a course on literature and computing, the immediate response of one person, delivered in a very knowing and almost amused manner was, "Oh, you mean the kind of course where you count words and decide if Shakespeare did it."

Presentation: [Introduction: three approaches to methods for digital humanists](https://docs.google.com/presentation/d/e/2PACX-1vQ65t6vb2LpJbHUDNkUdONZxFtDHKfCwPfccRHCtUgmOZILAA8JeA0ZFdU4ck2iifaOeEAj2dYBT6ge/pub?start=false&loop=false&delayms=3000) \([pdf](http://docs.google.com/presentation/d/1PAWx9XMddcnLo6bR9IX7-OhRQdwcsvOTHKk4MhNrmIM/export/pdf), [gd](https://docs.google.com/presentation/d/1PAWx9XMddcnLo6bR9IX7-OhRQdwcsvOTHKk4MhNrmIM/edit?usp=sharing)\)

## Don’t get carried away by fancy methods!

1. Your dataset must be applicable to the methods you choose. Complex methods often make presuppositions about the data they apply to - if you don’t understand these deeply, you’ll end up with invalid results
2. In typical DH research, 90% of your time will go to gathering and understanding the data and transforming it into a form you can use - using complex methods, another 90% of your time may go to altering them to fit your data, and it’ll run out
3. Complex methods are often unnecessary for DH work. On the contrary, often simpler methods are actually better.

## Assignments

* Answer the course background [questionnaire](https://goo.gl/forms/gQpLPyOVV4ZvtL1x1)
* Look over the final projects from last year. Select the project that interests you the most. Post a short message on the [\#introductions](https://slack.com/app_redirect?channel=introductions&team=T276JCMEU) channel on the course [Slack](http://meth4dh.slack.com/) to introduce yourself and to describe why you chose those that project.



