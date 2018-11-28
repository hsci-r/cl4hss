# Data processing: regular expressions

{% hint style="info" %}
Context note: this is a self-contained part of the METH4DH course. You can use this to teach yourself the basics of regular expressions. However, if you want to understand more broadly when you might want to use them, you're better off going through the whole course.
{% endhint %}

## Regular expressions

Regular expressions are not programming per se, but instead a versatile grammar for specifying text matching patterns. As such, they are useful for finding complex things in unstructured text, be that for close reading or for extracting those things into structured datasets.

For example, suppose you have the following text, which comes from an automatic transcription of a Swedish language bank employee matricle:

> Aaltio \(född Hinderson\), Ellen, född i Björneborg 25/B 1887, genomgått 6 klasser i Björneborgs, svenska samskola och en bokföringskurs 1899. -- Kassör vid Wasa-Aktie-Banks filialkontor i Björneborg från % 1904, i 4 års tid under vintermånaderna tjänstgjort vid Björneborgs Sparbank. 
>
> Adlercreutz, Herman, född i Kyrkslätt 28/io 1864, stu-. dent 2% 1884, allmän rätts-ex. 81/6 1889, auskultant i Åbo h ofrätt 6/6 s. å. - Kanslist vid Finlands Banks hufvud-kontor sedan 1893. - Vicehäradshöfding 2%2 1892, förste stadsfogde i Helsingfors sedan 1899. -- Deltagit i ridder-skåpet och adelns förhandlingar vid landtdagarne 1897, .1899, 1900, 1904--05, \(suppleant i lagutskottet\) och-1905--06 \(suppleant i fusteringsutskottet\). 
>
> Aejmelaeus, Otto, född i Paldamo 9/x 1850, genomgått 6 klasser i elementarläroverket i Uleåborg. - Direktör för Nordiska Aktiebankens 'för Handel och Industri filialkontor i Jyväskylä från 1896. - Konditionerat hos C. E. Carlström i Kristinestad, Aug. Eklöf i Borgå och i Paul Wahl & C:os trävaruaffär i Jyväskylä. -- Varit ordförande i fattigvårdsnämden och i drätselkammaren i Jyväskylä.

Now, suppose that you'd like to analyse the general profile of these bank employees. For that, you'd like to extract from this text a structured dataset of people, birth places and all attached dates. How would you go about it? 

Looking at the text, there is considerable regularity in how the information is presented. To allow you to better see it, here is the text with all last names _italicised_, first names rendered in a `different font`, birthplaces **bolded** and years both _**italicised as well as bolded**_:

> _Aaltio_ \(född Hinderson\), `Ellen`, född i **Björneborg** 25/B _**1887**_, genomgått 6 klasser i Björneborgs, svenska samskola och en bokföringskurs _**1899**_. -- Kassör vid Wasa-Aktie-Banks filialkontor i Björneborg från % _**1904**_, i 4 års tid under vintermånaderna tjänstgjort vid Björneborgs Sparbank. 
>
> _Adlercreutz_, `Herman`, född i **Kyrkslätt** 28/io _**1864**_, stu-. dent 2% _**1884**_, allmän rätts-ex. 81/6 _**1889**_, auskultant i Åbo h ofrätt 6/6 s. å. - Kanslist vid Finlands Banks hufvud-kontor sedan _**1893**_. - Vicehäradshöfding 2%2 _**1892**_, förste stadsfogde i Helsingfors sedan _**1899**_. -- Deltagit i ridder-skåpet och adelns förhandlingar vid landtdagarne _**1897**_, ._**1899**_, _**1900**_, _**1904--05**_, \(suppleant i lagutskottet\) och-_**1905--06**_ \(suppleant i fusteringsutskottet\). 
>
> _Aejmelaeus_, `Otto`, född i **Paldamo** 9/x _**1850**_, genomgått 6 klasser i elementarläroverket i Uleåborg. - Direktör för Nordiska Aktiebankens 'för Handel och Industri filialkontor i Jyväskylä från _**1896**_. - Konditionerat hos C. E. Carlström i Kristinestad, Aug. Eklöf i Borgå och i Paul Wahl & C:os trävaruaffär i Jyväskylä. -- Varit ordförande i fattigvårdsnämden och i drätselkammaren i Jyväskylä.

Looking at the patterns, you could derive for example the following rules to extract the elements:

* Year: four numbers anywhere 
* Last name: all letters before a space or a comma at the start of the line 
* First name: consecutive letters following the first comma on a line 
* Birthplace: consecutive letters following “född i”

Regular expressions allow you to transform such rules into one the computer is able to automatically process. For example, the regular expression for matching four numbers anywhere can be written [`[0-9][0-9][0-9][0-9]`](https://regex101.com/r/6439eo/1) \(click through for an interactive visualisation and explanation of the pattern\). However, because the regular expression grammar contains functionality for describing repeats, it can also be written [`[0-9]{4}`](https://regex101.com/r/jZD95S/2) . Further, because numbers are such a common class of things one might want to match, they too have their own shorthand symbol. Thus, the shortest equivalent regular expression for matching four consecutive numbers is [`\d{4}`](https://regex101.com/r/vCvTXk/1).

In practice, crafting regular expressions is an iterative process, where you experiment with different formulations of a pattern to end up with one that matches what you want, but doesn't match anything else. For example, the current formulation does not discover the year 1905 from the string `1904--05` . If that year was interesting information, a second pattern might need to be added. On the other hand, if you discovered that there are other four digit numbers in the text that aren't years, maybe you'd think of countering that by restricting matches only to numbers that start with either 18 or 19 \(realised e.g. as [`1[89]\d{2}`](https://regex101.com/r/wZXHTW/1)\).

{% hint style="info" %}
**Assignment**

1. Go through [this regex tutorial](https://regexone.com/)
2. Create regexes to extract first names, last names, years, birth places etc from the bank matricle. To start with, here are some different attempts for matching the last names:

   * [^\[^ \]+](https://regex101.com/r/LHc1xP/1) \(everything before a space at the start of the line\)
   * [^\w+](https://regex101.com/r/wwKHlt/1) \(consecutive word characters at the start of the line \[but see below\]\)
   * [^\p{Lu}\p{L}+](https://regex101.com/r/nAy4fr/1) \(One uppercase character followed by consecutive upper or lower case characters. Here, the `\p{Lu}` and `\p{L}` come from [Unicode character classes](https://www.regular-expressions.info/unicode.html). This is important, because historically, regular expressions were very Anglocentric. Therefore `\w` only matches the letters a-z, and not for example ümläüts, áccênts, or symbols from completely different sets such as Hangul or Kanji. Using the Unicode character classes fixes all this.\)

   Note that it is often easier to:

   1. craft separate patterns for the different elements instead of trying to match them using a single expression
   2. even for matching a single element such as birth place, to have multiple overlapping patterns to catch the variants you want instead of trying to cram all the variation in a single pattern, and
   3. match more than you actually want and then extract from that using [capturing groups](https://regexone.com/lesson/capturing_groups), instead of trying to craft a pattern capturing just the element \(which often anyway requires fooling around with non capturing [lookarounds](https://www.regular-expressions.info/lookaround.html)\).
{% endhint %}

### Further examples

* Removing all punctuation, multiple spaces etc, and replacing them with a single space: `s/\W+/ /g`
* Finding full names \(some basic named-entity recognition or NER\): `\p{Lu}\p{L}* \p{Lu}\p{L}*`
* Matching different ways of spelling the word cannot in a varied historical corpus: `[kc]an.?no.?t.`

One of the problems with regular expressions is that when you develop them iteratively, you invariably end up with [patterns that are indecipherable](https://blog.codinghorror.com/regex-use-vs-regex-abuse/) \(even to yourself later on\). Here's for example my best effort in crafting a single regular expression to capture both last as well as first names from the matricle: [`^*?(\p{Lu}\p{L}+)(?: (+?))?, (?:(+?) )?((?:\p{Lu}\p{L}+ ?)+)`](https://regex101.com/r/KUSHk2/1) \(which again speaks to the fact that you really shouldn't try to capture too much in a single expression, as the same information could be extracted using multiple much smaller and thus more understandable patterns\).

### Resources

* [Regular expressions 101](https://regex101.com/), an environment for experimenting with regular expressions
* [Regular-Expressions.info](https://www.regular-expressions.info/quickstart.html) reference

![Regular Expressions. Source: https://xkcd.com/208/, CC BY-NC 2.5 license.](.gitbook/assets/image%20%284%29.png)



