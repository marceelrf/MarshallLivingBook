---
title: "The living book of Marshall"
author: "Marcel Ferreira - Marshall"
date: "2022-06-28"
site: bookdown::bookdown_site
documentclass: book
bibliography: [book.bib, packages.bib]
# url: your book url like https://bookdown.org/yihui/bookdown
# cover-image: path to the social sharing image like images/cover.jpg
description: |
  This is a minimal example of using the bookdown package to write a book.
  The HTML output format for this example is bookdown::bs4_book,
  set in the _output.yml file.
biblio-style: apalike
csl: chicago-fullnote-bibliography.csl
---

# About {.unnumbered}

**The living book of Marshall** was born from the idea of producing content based on the concept of open science. It is important to be clear that this book is not peer-reviewed. At least not in the traditional way. The content of this book includes a series of notes on topics of interest to me. Topics that I have been working on in my day-to-day life as a researcher in the areas of biomaterials, bioinformatics, data science, and bone regeneration biology.\
As you read this book you will probably come across some incomplete section. Don't worry, this is part of the idea of a living book. This book will never have a final version. I will try to add sections as I go deeper and believe it is important to share them with the community.\
If you find any wrong information feel free to contact me through my [github profile](https://github.com/marceelrf#-ask-me-anything).

## About me {-}

![It's mee!](images/marshall.jpg)

I'm a brazilian medical physicist with master in Biotechnology and currently a PhD candidate (Biotechnology) at São Paulo State University ([UNESP](https://unesp.br/)). On April 2022 I joined the Witek Lab at [New York University](https://www.nyu.edu/) as a visiting schoolar. I'm currently working on the development of tools for bone biomaterials analysis, focusing on alternative methods to animal testing. I have interest in biological databases, bioinfomatics analysis, data science, machine learning and new technologies as 3D bioprinting and organ-on-a-chip. I am an enthusiast of open science and the R programming language. Right now I am preparing the documentation for my first package!\
For my scientific publication records please check my [google schoolar profile](https://scholar.google.com.br/citations?user=lS42GYwAAAAJ&hl=pt-BR)




<!--chapter:end:index.Rmd-->

# Hello bookdown 

All chapters start with a first-level heading followed by your chapter title, like the line above. There should be only one first-level heading (`#`) per .Rmd file.

## A section

All chapter sections start with a second-level (`##`) or higher heading followed by your section title, like the sections above and below here. You can have as many as you want within a chapter.

### An unnumbered section {-}

Chapters and sections are numbered by default. To un-number a heading, add a `{.unnumbered}` or the shorter `{-}` at the end of the heading, like in this section.

<!--chapter:end:01-intro.Rmd-->

# (PART\*) R programming {.unnumbered}

# R basics {#rprog}

The R language was developed for data analysis with a solid statistical background. R is a multi-paradigm object-oriented, functional programming, dynamic, weakly typed, programming language focused on data manipulation, analysis, and visualization. It was originally created by Ross Ihaka and Robert Gentleman in the Statistics department at the University of Auckland, New Zealand. The Base R packages are developed and maintained by the R Development Core Team (R Core), through their controlled Software Development Life Cycle (SDLC). All source code is available for review under the Free Software Foundation's GNU Public License (GPL). You can download in the Comprehensive R Archive Network ([CRAN](https://cran.r-project.org/)) website.

There are several development interfaces for programming with R, but among all of them I strongly recommend using [RStudio](https://www.rstudio.com/). You can work with in Windows, Mac, and Linux, or through a web browser using the RStudio server, if you want.

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/ed/RStudio_IDE_screenshot.png/450px-RStudio_IDE_screenshot.png" title="RStudio" alt="RStudio"/>

## R object classes

<!--chapter:end:02-Rbasics.Rmd-->

# Parts

You can add parts to organize one or more book chapters together. Parts can be inserted at the top of an .Rmd file, before the first-level chapter heading in that same file. 

Add a numbered part: `# (PART) Act one {-}` (followed by `# A chapter`)

Add an unnumbered part: `# (PART\*) Act one {-}` (followed by `# A chapter`)

Add an appendix as a special kind of un-numbered part: `# (APPENDIX) Other stuff {-}` (followed by `# A chapter`). Chapters in an appendix are prepended with letters instead of numbers.




<!--chapter:end:03-parts.Rmd-->

# Footnotes and citations 

## Footnotes

Footnotes are put inside the square brackets after a caret `^[]`. Like this one ^[This is a footnote.]. 

## Citations

Reference items in your bibliography file(s) using `@key`.

For example, we are using the **bookdown** package [@R-bookdown] (check out the last code chunk in index.Rmd to see how this citation key was added) in this sample book, which was built on top of R Markdown and **knitr** [@xie2015] (this citation was added manually in an external file book.bib). 
Note that the `.bib` files need to be listed in the index.Rmd with the YAML `bibliography` key.


The `bs4_book` theme makes footnotes appear inline when you click on them. In this example book, we added `csl: chicago-fullnote-bibliography.csl` to the `index.Rmd` YAML, and include the `.csl` file. To download a new style, we recommend: https://www.zotero.org/styles/


The RStudio Visual Markdown Editor can also make it easier to insert citations: <https://rstudio.github.io/visual-markdown-editing/#/citations>

<!--chapter:end:04-citations.Rmd-->

# Blocks

## Equations

Here is an equation.

\begin{equation} 
  f\left(k\right) = \binom{n}{k} p^k\left(1-p\right)^{n-k}
  (\#eq:binom)
\end{equation} 

You may refer to using `\@ref(eq:binom)`, like see Equation \@ref(eq:binom).


## Theorems and proofs

Labeled theorems can be referenced in text using `\@ref(thm:tri)`, for example, check out this smart theorem \@ref(thm:tri).

::: {.theorem #tri}
For a right triangle, if $c$ denotes the *length* of the hypotenuse
and $a$ and $b$ denote the lengths of the **other** two sides, we have
$$a^2 + b^2 = c^2$$
:::

Read more here <https://bookdown.org/yihui/bookdown/markdown-extensions-by-bookdown.html>.

## Callout blocks


The `bs4_book` theme also includes special callout blocks, like this `.rmdnote`.

::: {.rmdnote}
You can use **markdown** inside a block.


```r
head(beaver1, n = 5)
#>   day time  temp activ
#> 1 346  840 36.33     0
#> 2 346  850 36.34     0
#> 3 346  900 36.35     0
#> 4 346  910 36.42     0
#> 5 346  920 36.55     0
```

:::

It is up to the user to define the appearance of these blocks for LaTeX output. 

You may also use: `.rmdcaution`, `.rmdimportant`, `.rmdtip`, or `.rmdwarning` as the block name.


The R Markdown Cookbook provides more help on how to use custom blocks to design your own callouts: https://bookdown.org/yihui/rmarkdown-cookbook/custom-blocks.html

<!--chapter:end:05-blocks.Rmd-->

# Sharing your book

## Publishing

HTML books can be published online, see: https://bookdown.org/yihui/bookdown/publishing.html

## 404 pages

By default, users will be directed to a 404 page if they try to access a webpage that cannot be found. If you'd like to customize your 404 page instead of using the default, you may add either a `_404.Rmd` or `_404.md` file to your project root and use code and/or Markdown syntax.

## Metadata for sharing

Bookdown HTML books will provide HTML metadata for social sharing on platforms like Twitter, Facebook, and LinkedIn, using information you provide in the `index.Rmd` YAML. To setup, set the `url` for your book and the path to your `cover-image` file. Your book's `title` and `description` are also used.


This `bs4_book` provides enhanced metadata for social sharing, so that each chapter shared will have a unique description, auto-generated based on the content.

Specify your book's source repository on GitHub as the `repo` in the `_output.yml` file, which allows users to view each chapter's source file or suggest an edit. Read more about the features of this output format here:

https://pkgs.rstudio.com/bookdown/reference/bs4_book.html

Or use:


```r
?bookdown::bs4_book
```




<!--chapter:end:06-share.Rmd-->

# (PART\*) Bone biology {-}
# Proline Metabolism

This chapter is inspired in the Dr Karner's Lab (<https://www.utsouthwestern.edu/labs/karner/research/proline.html>)

## General metabolism

Proline is biosynthetically derived from the amino acid L-glutamate. Glutamate-5-semialdehyde is first formed by glutamate 5-kinase (ATP-dependent) and glutamate-5-semialdehyde dehydrogenase (which requires NADH or NADPH).

[![Proline biosynthesis](images/Pathway-of-proline-biosynthesis-and-degradation-in-bacteria.png)](https://www.researchgate.net/profile/Maurizio-Trovato/publication/226456939/figure/fig1/AS:393621418332161@1470858067068/Pathway-of-proline-biosynthesis-and-degradation-in-bacteria.png)

## How is proline uptake regulated during osteoblast differentiation?

Slc38a2 (Sodium-coupled neutral amino acid transporter 2)

## What are the proline transporters and how are they regulated?

<!--chapter:end:07-Proline-Metabolism.Rmd-->

# (PART\*) Protocols {-}

# Cell culture

## Basis  


<!--chapter:end:08-protocols_cellculture.Rmd-->

# Western Blotting

This chapter is based on the protocol used in the [Bioassays and Cell Dynamic lab](https://www.instagram.com/bioassaysandcelldynamic/) directed by Dr Willian Zambuzzi.

Western Blotting is a technique in molecular biology/biochemistry for detecting proteins in a homogenate (lysed cells) or in an extract of a biological tissue. This technique uses gel electrophoresis to separate denatured proteins by mass (polypeptide length). Proteins are separated from the gel onto PVDF (polyvinylidene fluoride) membrane, where antibodies specific to the protein to be studied are used as probes.

## Step 1 - Sample preparation

Before performing the electrophoretic run the cells need to be lysed in order to release the proteins of interest. However, a protease inhibitor cocktail is used in the Lysis Buffer to prevent the proteins from being degraded/digested.

The β-mercaptoethanol (reducing agent) used in the Sample Buffer binds to the disulfide (S-S) bonds of the cysteine residues, which promote the binding of proteins to other monomers, other proteins, or even to the tertiary structure of the same protein, thus keeping the proteins separated and in the primary conformation.

### Materials

- Sample (standardized - see separate protocol).
- Falcon tubes.
- Warm PBS.
- Lysis buffer and sample buffer.
- Ice.
- Centrifuge and vortex.

### Procedures

-  Scrape the cells from the petri dish with scrap.
-  Centrifuge in a falcon tube for 5 min at a speed of 3000 rpm.
-  Discard the supernatant.
-  Resuspend the pellet with warm PBS.
-  Centrifuge in a falcon tube for 5 min at 3000 rpm.
-  Discard the supernatant.
-  Resuspend the pellet in 50-200μL lysis buffer (variable volume).
-  Wait 2 hours on ice, shaking the solution on the vortex every 20 min.
-  Centrifuge the eppendorfs in a refrigerated centrifuge for 15 min at a temperature of 4°C to 8°C at a speed of 14000 rpm.
-  Collect the supernatant, measuring the exact volume (discard the pellet).
-  Separate 10 μL for protein dosage (see protocol ...)
-  To the remainder add sample buffer (TA) in a 1:1 ratio (see protocol ...)
-  Heat at 95°C for 5 min and then freeze.

## Step 2 - Gel preparation  

The gel preparation will be an inert matrix through which the proteins can migrate. It is made by polymerizing acrylamide monomers, and the pore size of the gel can be adjusted by varying the concentration of acrylamide (LOWER gel) added, depending on the molecular weight of your protein of interest. SDS, which is negatively charged, binds in the hydrophobic regions of the proteins, masking their intrinsic charges and allowing them to migrate toward the positive pole of the electric field formed.


Table: (\#tab:upperGel)Upper gel

|Reagent               |Volume     |
|:---------------------|:----------|
|Tris 0.5M, pH 6.8     |2.5 mL     |
|SDS 10%               |100 µL     |
|Acrylamide 40% Bis 1% |1 mL       |
|Water                 |6.40 mL    |
|APS 10%               |50 µL      |
|TEMED                 |10 – 20 µL |
|Total                 |10 mL      |

The gel recipe below has been adjusted to volumes of 10mL for each concentration (\@ref(tab:lowerGel)). If you want to work with 20mL, 30mL, or 40 mL, just multiply by 2, 3, or 4, respectively. The X% contains the recipe to make a lower gel in any desire concentration.  


Table: (\#tab:lowerGel)Lower Gel

|Reagent               |X6.      |X8.      |X10.     |X12.     |X.                          |
|:---------------------|:--------|:--------|:--------|:--------|:---------------------------|
|Tris 1.5M, pH 8.8     |2.5 mL   |2.5 mL   |2.5 mL   |2.5 mL   |2.5 mL                      |
|SDS 10%               |0.1 mL   |0.1 mL   |0.1 mL   |0.1 mL   |0.1 mL                      |
|Acrylamide 40% Bis 1% |1.5 mL   |2 mL     |2.5 mL   |3.0 mL   |0.25 mL * X%                |
|Water                 |5.85 mL  |5.35 mL  |4.85 mL  |4.35 mL  |7.35 mL - Acrylamide volume |
|APS 10%               |0.05 mL  |0.05 mL  |0.05 mL  |0.05 mL  |0.05 mL                     |
|TEMED                 |0.005 mL |0.005 mL |0.005 mL |0.005 mL |0.005 mL                    |
|Total                 |10 mL    |10 mL    |10 mL    |10 mL    |10 mL                       |

### Procedures

-  Take two falcon tubes. One for each solution.  
-  In one tube prepare the Upper, placing all components except the TEMED and APS (avoiding polymerization).  
-  In one tube prepare the Lower, placing all the components!  
-  Place the Lower solution in the gel preparation compartment (between the vials) until approximately the green line on the glass.  
-  Add 1 mL of butanol solution or distilled water until the end of the glass (avoiding the contact with the $O_2$ and helping the polymerization). After the addition, wait for the gel to polymerize.  
-  Discard the water or butanol. Next, place the APS and TEMED in the Upper, homogenize the solution, and apply it above the Lower.  
-  Once added to the Upper, place the comb (10 or 15 wells) to form the wells.  
-  Wait for polymerization (~ 20 min) and remove the comb.  

## Step 3 - Electrophoresis run  

From the conditions exposed in the previous steps, the gel is subjected to an electric field and the proteins, now negatively charged due to the action of SDS, migrate to the positive pole of the electrode. This technique will estimate the molecular weight of the proteins, since differentiated migration of molecules with different sizes will occur.

### Procedures  

- 	Place the cassette with the polymerized gel in the vat.  
- 	Pipette 5 μL of the molecular weight marker into the first well of the gel, and pipette 5 - 35 μL of your samples (depending on the amount obtained in the protein assay).  
- 	Fill the electrophoretic tank with the Running Buffer.  
- 	Turn on the device and run at 50V - 80V for each gel, until the sample runs through the entire gel, for approximately 1 hour (note the location of the bands).  
- 	Turn off the instrument.  

## Step 4 - Transfer of the gel proteins to the membrane

SDS-PAGE, although an analytically technique, does not allow the analysis of individual and separate proteins. For this to be possible, it is necessary to use antibodies specific for the desired protein. However, these proteins need to be on a solid support. At LaBio we generally use PVDF membrane. This transfer of the proteins from the gel to the membrane is done by electrophoretic transfer.

- 	Cut the PVDS membrane to the gel dimensions and wet it well with methanol.  
- 	Disassemble the electrophoresis tank and uncouple the glass plates to remove the gel. Do this inside the transfer buffer using a spatula (use a white tray).  
- 	After removing the gel, assemble the "sandwich" as shown in the diagram below, following the direction of the arrow.  
- 	Fill a vat with Transfer Buffer and place the platform surface of the transfer device, leaving it immersed. The black part of the platform down/transparent part up.
**IMAGE**
- 	Close the "sandwich" and place it in the transfer vat (the black part of the holder facing the black part of the vat).  
- 	Place an icex on the transfer tray to prevent the system from overheating or place the tray in a bowl of ice in the refrigerator.  
- 	Switch the device on and apply a 400 mA current for 45 minutes.  
- 	Switch off the device.  

## Step 5 - Membrane blocking

The membrane has a high affinity for proteins. Thus, it is necessary to block it to prevent antibodies from binding to the entire membrane surface, i.e. generating nonspecific binding.

Either milk powder or BSA can be used with a blocking solution. However, when using phosphospecific antibodies^[Phospho-specific antibody: antibody directed against phosphorylated peptides. The first category is generic, consisting of phosphotyrosine, phosphoserine and phosphothreonine antibodies, which will bind to any phosphorylated tyrosine, serine and threonine residue, regardless of the neighboring amino acid. The second category includes antibodies against specific epitopes of phosphoamino acids.], the use of milk is not recommended, because of the high background noise.

### Procedures  

-  For phosphorylated proteins: make a solution of TBST + 5% BSA (w/v).  
-  For non-phosphorylated proteins: make a solution of TBST + 5% powdered Milk (m/v).  
-  In both cases, block the membrane for 1 hour at moderate stirring and room temperature.

## Step 6 - Primary antibody incubation 

After blocking, the membrane should be stained with ponceau (dye that shows if there was transference of the proteins from the gel to the membrane), and this solution should be reused.  
To visualize the protein of interest, a specific antibody is used to react with an epitope of the protein, forming an antigen-antibody complex.

### Procedures  

-  Make a solution of TBSTA + primary antibody. The dilution of the antibody must follow the datasheet (e.g. 1: 1000). The diluted antibody can be reused several times - store in the freezer after use.  
-  Incubate the membrane in this solution and store in the refrigerator under moderate agitation overnight.  
-  After incubation store antibody and perform three washes (with constant agitation): TBST for 15 min and 2 of TBS for 15 min each (buffers should be discarded).  

## Step 7 - Secondary antibody incubation  

In this step, the membrane is incubated with a secondary antibody. This antibody has some specific biochemical modification that will allow the visualization of its protein of interest. At LaBIO, the secondary antibodies used are conjugated with an enzyme that will be important at the time of film development.

### Procedures

-  Remove the membrane from the TBS solution and place it in the solution made with secondary antibody (TBSTA + secondary antibody) under moderate stirring for 1 hour. The dilution of the antibody should follow the datasheet.  
-  Remove the membrane from the solution with the secondary antibody and repeat the three washes: TBST for 15 min and 2 of TBS for 15 min each (the buffers must be discarded).  

## Step 8 - Membrane read

At the time of the membrane development, a substrate of the enzyme mentioned above is added. In the places where this enzyme is present the reaction and the formation of the product will occur. A film is used and marking will appear in the regions where this reaction occurred, allowing the localization of the protein of interest.

### Procedures

-  On the bench, place the membranes on top of a substrate (e.g. parafilm).  
-  Make an ECL or luminol solution, in which you mix two fluorescent reagents: ECL WB Reagent A and ECL WB Reagent A in a 1:1 ratio (should be kept in the refrigerator after use).  
-  Place the solution on the membranes (make sure that the entire membrane is soaked by the solution). Wait for 1 min.  
-  Place the membrane on the plastic inside the cassette.  
-  Take the cassette to darkroom and develop the film.  
-  In the darkroom set up the developing bench: place a basin with developer, water, fixer, and water (exactly in that order).  
-  After leaving the membrane(s) being exposed (variable time), remove the film and leave it 60 seconds in each tray, in the order described above.  
-  Let the film dry. 


<!--chapter:end:09-westernbloting.Rmd-->

# Cross-references {#cross}

Cross-references make it easier for your readers to find and link to elements in your book.

## Chapters and sub-chapters

There are two steps to cross-reference any heading:

1. Label the heading: `# Hello world {#nice-label}`. 
    - Leave the label off if you like the automated heading generated based on your heading title: for example, `# Hello world` = `# Hello world {#hello-world}`.
    - To label an un-numbered heading, use: `# Hello world {-#nice-label}` or `{# Hello world .unnumbered}`.

1. Next, reference the labeled heading anywhere in the text using `\@ref(nice-label)`; for example, please see Chapter \@ref(cross). 
    - If you prefer text as the link instead of a numbered reference use: [any text you want can go here](#cross).

## Captioned figures and tables

Figures and tables *with captions* can also be cross-referenced from elsewhere in your book using `\@ref(fig:chunk-label)` and `\@ref(tab:chunk-label)`, respectively.

See Figure \@ref(fig:nice-fig).


```r
par(mar = c(4, 4, .1, .1))
plot(pressure, type = 'b', pch = 19)
```

<div class="figure" style="text-align: center">
<img src="cross-refs_files/figure-html/nice-fig-1.png" alt="Plot with connected points showing that vapor pressure of mercury increases exponentially as temperature increases." width="80%" />
<p class="caption">(\#fig:nice-fig)Here is a nice figure!</p>
</div>

Don't miss Table \@ref(tab:nice-tab).


```r
knitr::kable(
  head(pressure, 10), caption = 'Here is a nice table!',
  booktabs = TRUE
)
```



Table: (\#tab:nice-tab)Here is a nice table!

| temperature| pressure|
|-----------:|--------:|
|           0|   0.0002|
|          20|   0.0012|
|          40|   0.0060|
|          60|   0.0300|
|          80|   0.0900|
|         100|   0.2700|
|         120|   0.7500|
|         140|   1.8500|
|         160|   4.2000|
|         180|   8.8000|

<!--chapter:end:cross-refs.Rmd-->


# References {-}


<!--chapter:end:references.Rmd-->

