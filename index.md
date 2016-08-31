---
title       : How I use R
subtitle    : Hacks & Hackers - Data Journalism
author      : Andy Pryke - Andy@The-Data-Mine.co.uk
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

<style>
.title-slide {
  background-color: #FFFFFF; 
}
</style>

## Contents

   * Data Journalists Using R
   * Organising Projects
   * Reproducability
   * Finding Out How to ...
   * Bonus - Nice Packages

--- 

## Data Journalists Using R	
   * Buzzfeed
   * Five Thirty Eight
   * Lots more...
   
   * ["Resources for doing data journalism with R (rddj.info)"](http://rddj.info/)

--- 

## Data Journalists Using R - Buzzfeed
   * Buzzfeed - Peter Aldhous and Charles Seife 
   * ["Data Journalism Awards Data Visualization of the Year, 2016"](http://www.globaleditorsnetwork.org/programmes/data-journalism-awards/)
   * [The Story: Spies in the Skies] (https://www.buzzfeed.com/peteraldhous/spies-in-the-skies?utm_term=.trGQXE05zL#.rcZq1K7g6k)
   * [All on Github - https://github.com/BuzzFeedNews](http://buzzfeednews.github.io/2016-04-federal-surveillance-planes/analysis.html)
   * source: http://blog.revolutionanalytics.com/2016/04/the-fbis-aerial-surveillance-program-visualized-with-r.html

--- 

## Data Journalists Using R - Five Thirty Eight

   * Talk from useR! 2016 conference (17 mins + Q&A)  
http://blog.revolutionanalytics.com/2016/07/data-journalism-with-r-at-538.html
   * Well worth seeing
   * 12 mins in - various examples of using R

--- 

## How I Organise Projects
   * Keep original data somewhere seperate 
      * e.g. "originals" & "processed" directories
   * Start with a Rmarkdown file
   * Work on the command line then move code to file
   * Aim for readable code
   * Create functions to make code easier to read
   * Use very clear variable & function names
      * Don't worry if they are too long
   * Use git / github to version your code

---

## Reproducability - Why

So...
   * ... **when** I make a mistake I can re-do the work instantly
   * ... others can check how I did things (and if it was right)
   * ... so future me can check how I did things
   * ... so future me can re-use my work for new data / project
   

---

## Reproducability - How

   * Try to eliminate manual steps (within reason)
   * Use package "checkpoint" - to ensure you always use the same version of packages, even years later
   * Keep your code somewhere - github?
   * Include your copy of original data
   * Document


---

## Finding Out How to ...
Searching for "R" can be hard

Google actually doesn't do too bad a job  
try adding "package" if you're not getting good results


---

## Finding Out How to ... - Rseek
Rseek - dedicated search for R related things

http://rseek.org/
[rseek: "birmingham -alabama"](http://rseek.org/?q=birmingham+-alabama)


---

## Finding Example Code - github

Use **Advanced Search** - there's a link if you do a normal search

https://github.com/search/advanced

Is there anything about Birmingham?  
[Birmingham extension:R extension:rmd](https://github.com/search?utf8=%E2%9C%93&q=Birmingham+extension%3AR+extension%3Armd&type=Code&ref=searchresults)

Can you use shapefiles in R?  
[extension:rmd extension:R  (".shp" OR shapefile)](https://github.com/search?utf8=%E2%9C%93&q=extension%3Armd+extension%3AR++%28%22.shp%22+OR+shapefile%29+&type=Code&ref=searchresults)

Are there any shapefiles for Birmingham?
[extension:R birmingham (".shp" OR shapefile) NOT alabama](https://github.com/search?utf8=%E2%9C%93&q=extension%3AR+birmingham+%28%22.shp%22+OR+shapefile%29+NOT+alabama&type=Code&ref=searchresults)

How do I use "datatable" from package "DT"  
[datatable library(DT) extension:R extension:rmd](https://github.com/search?utf8=%E2%9C%93&q=datatable+library%28DT%29+extension%3AR+extension%3Armd&type=Code&ref=searchresults)


---

## Question...

What if someone copied your story?
 * All of it, exactly?
 * A paragraph?
 * Rephrased it?
 * Used the same themes?
 * etc.

---

## Question...

What if someone copied your script?
 * All of it, exactly?
 * A function?
 * Rephrased it?
 * Used the same themes?
 * etc.

---

## Question...

What if someone copied your script?
 * All of it, exactly?
 * A function?
 * Rephrased it?
 * Used the same themes?
 * etc.

Where is the line for code?
 - Sometimes there is a licence, often not.

---


---

## Bonus - Nice Packages begining with "D"
   * dplyr - transforming data
   * data.table - Fast handling of larger datasets (10's of Millions)
   * DT - nice display of tables in HTML

---

---

## Test DT in slidify


```r
   dynamic_table <- DT::datatable(iris)
   DT::saveWidget(dynamic_table, 'example.html')
   cat('<iframe src="example.html" height=20 style="height:20"> </iframe>')
```

<iframe src="example.html" height=20 style="height:20"> </iframe>
Hello

---

## Next slide
