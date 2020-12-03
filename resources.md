---
layout: page
title: Resources
permalink: /resources/
---

{%- comment -%}
*toward an open lab / reproducible practices in research:*
{%- endcomment -%}

What makes a research project reproducible is not a simple question... Nonetheless I do believe than one should be able to reproduce ones' own analysis without pain, even in the future. This may sound all obvious, but not be so easy to achieve in practice!

Here are some tips for students, based on my iterations toward more reproducible practices:

- Start from the beginning: although it may sometimes feel like a waste of time, putting yourself in the situation of readily redoing your analysis will make your researcher's life easier (and to the very least help you to rerun chunks from earlier work).

- For each usual task (data analysis, plotting, citing references), you should master one tool down to its dirty details.

- Relying on text-based formats (e.g. Markdown, LaTeX, CSV) is critical in order to be able to use version control to maintain your code, to write manuscripts, etc. This may indeed guide your choice of tools. A good starting points to learn version control with `git` is the Software Carpentry [tutorial](https://swcarpentry.github.io/git-novice/). GitHub's [documentation](https://help.github.com) provides help on more advanced topics.


## handling data

- For data analysis and plotting, I enjoy very much (most of the time!) working with `R`'s [`tidyverse`](https://www.tidyverse.org), in particular `dplyr` and `ggplot2`. If you are new to R or to data analysis from the command line, the companion book *R for Data Science* (available [online](http://r4ds.had.co.nz)) is the best introduction you can dream of. My advice: study sections 2 to 8 thoroughly, the next ones will be useful to go deeper on specific topics based on your needs.  
Hint: if you need to speed up your analysis with `dplyr` have a look at its parallelized counterpart [`multidplyr`](https://github.com/hadley/multidplyr).
 
- Dont overlook [RStudio's cheatsheets](https://www.rstudio.com/resources/cheatsheets/)!

- Follow a well-established coding style guide. If you don't know which one to pick, use the [lintr](https://github.com/jimhester/lintr) package (along with [styler](https://github.com/r-lib/styler) for existing code) to follow the [tidyverse's style guide](http://style.tidyverse.org).


- Follow simple guidelines when [recording data in spreadsheets](http://blog.revolutionanalytics.com/2017/11/good-practices-spreadsheets.html)

- Use regular expressions whenever you can. Regexs are great, regexs are tough, and regexs are poorly taught (if at all!) unless you've a computer science background: luckily Damian Conway's presentations are eye-opening (e.g. this [50' video](https://www.infoq.com/presentations/regex)) and there is a [great cheatsheet](https://www.rstudio.com/wp-content/uploads/2016/09/RegExCheatsheet.pdf) for R. Also you want to view what you're doing, e.g. within RStudio using [RegExplain addin](https://github.com/gadenbuie/regexplain) or online with [RegExr.com](https://regexr.com/).

- To share large datasets, [Zenodo](https://zenodo.org) is a great (free) service. If you use another one, make sure that your dataset gets a DOI.


## handling text

- Despite LaTeX's popularity in quantitative fields, I believe that the time is ripe to leave it to advanced editing where microtypography matters... Simpler syntaxes (in particular Markdown) are sufficient for literate data analysis (e.g. with Rmarkdown or R notebooks) and even for more advance tasks like [writing a dissertation](https://github.com/tompollard/phd_thesis_markdown) or [an article](https://github.com/rstudio/rticles); I put online a [template](https://github.com/julou/sci-article-with-R) to render a manuscript and its companion supplementary material with cross-reference. Whatever format you choose to rely on, don't miss that `pandoc` is an incredibly powerful conversion tools between most formats (.md, .tex, .rtf, .docx, etc).  
Hint: the Markdown converter used by RStudio (`pandoc-citeproc`) is able to handle citations just like bibtex would (and in fact simpler!).

- For storing and citing articles, [Zotero](https://zotero.org) is the most versatile open-source software. <!-- However, its user experience is a bit rough on the edges: it took me a while to go back to it after using Papers during three years. Check [my tips to streamline saving,  storing, and citing](). -->


## handling DNA sequences

- [Benchling](https://benchling.com) is the 21st century sequence editor to design and keep track of your molecular biology experiments: design primers, align sequencing chromatograms, test your next cloning *in silico*. It even has an integrated lab notebook!  
Big drawback: your data must be hosted on their servers...


## handling microscopy data

- [Micro-Manager](https://micro-manager.org) is an open-source software for microscope control. If your hardware falls in the list of (over 200) supported items, it is very easy to configure and can be extended to support advanced features such as hardware triggering (on which we wrote a [step-by-step tutorial](https://github.com/vanNimwegenLab/MiM_NikonTi/blob/master/Docs/NikonTi_hardware_triggering.md)). 

- A smooth [introduction lecture to fluorescence microscopy](https://www.ibiology.org/talks/introduction-fluorescence-microscopy/) taken from a great [large series](https://www.ibiology.org/online-biology-courses/microscopy-series/microscopy-series-table-contents/).

<!-- - IJ Fiji resources -->

<!-- - *archiving/browsing microscopy images (fiji, omero, bioformats) -->


## academia survival kit

<!-- (1998) Directed evolution of a full professor. Curr. Biol. 8, R864. -->

- Uri Alon's [materials for nurturing scientists](http://www.weizmann.ac.il/mcb/UriAlon/materials-nurturing-scientists) is probably the best existing "academia survival kit" that I know of (and it even has [additional information](http://www.weizmann.ac.il/mcb/UriAlon/additional-information)). Below is my attempt to enrich it with a few links.

- [*Some Modest Advice for Graduate Students*](http://onlinelibrary.wiley.com/doi/10.2307/20166580/full) by S. Stearns and R. Huey's [*Reply to Stearns: Some Acynical Advice for Graduate Students*](http://onlinelibrary.wiley.com/doi/10.2307/20166581/full).

- Writings such as B. Latour's [*Petites leçons de sociologie des sciences*](http://www.editionsladecouverte.fr/catalogue/index-Petites_le__ons_de_sociologie_des_sciences-9782707150127.html) and I. Stengers' [*Sciences et pouvoirs*](http://www.editionsladecouverte.fr/catalogue/index-Sciences_et_pouvoirs-9782707138576.html) ([*Power and invention*](https://www.upress.umn.edu/book-division/books/power-and-invention)) have helped me to overcome various academic frustrations and hopefully to fight some of their causes. [*Making genes, making waves*](http://www.hup.harvard.edu/catalog.php?isbn=9780674009288) by J. Beckwidth is another inspiring read.

- L'Atelier des Jours à Venir, a French non-profit company promoting reflexive and responsible research practices, gathered valuable [resources](http://www.joursavenir.org/Resources).

<!-- - contribution NKI -->

- On research integrity: I was a founder of the [Scientific Red Cards](https://scientificredcards.wordpress.com) initiative (discontinued). Related issues are currently addressed by [Retraction Watch](https://retractionwatch.com) and [PubPeer](https://pubpeer.com).

- Need a practical guide to research integrity? I find the [guidelines of Piet Borst](https://joursavenir.wordpress.com/2018/03/25/integrity-in-science-by-piet-borst/) one of the most insightful! In particular, his "advice is to be generous towards your colleagues and tough towards yourself. Nearly everybody has the tendency to overestimate his own contribution to the research of others and underestimate the contribution of other people to his own work." Probably worth meditating every time one is upset by the status of a collaboration...

  <!-- + blog post -->
  