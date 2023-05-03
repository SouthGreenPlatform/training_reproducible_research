Let's begin with starting RStudio and opening a new file (*File* --> *New File*
--> *R Markdown*). If you're using Conda you should have all the packages
needed, but install anything that RStudio prompts you to. In the window that
opens, select *Document and HTML* (which should be the default), and click *Ok*.
This will open a template R Markdown document for you. On the top is a so called
YAML header:

```yaml
---
title: "Untitled"
output:
    html_document:
        toc: true
---
```

!!! warning
    The header might look slightly different depending on your version of
    RStudio. If so, replace the default with the header above.

Here we can specify settings for the document, like the title and the output
format.

* Change the title to `My first R Markdown document`

Now, read through the rest of the template R Markdown document to get a feeling
for the format. As you can see, there are essentially three types of components
in an R Markdown document:

1. Text (written in R Markdown)
2. Code chunks (written in R or another [supported language](https://bookdown.org/yihui/rmarkdown/language-engines.html))
3. The YAML header

Let's dig deeper into each of these in the following sections! But first, just
to get the flavor for things to come: press the little *Knit*-button located at
the top of the text editor panel in RStudio. This will prompt you to save the
Rmd file (do that), and generate the output file (an HTML file in this case).
It will also open up a preview of this file for you.

!!! Success "Quick recap"
    In this section, you learned how to create a R mardown file and generate an 
    output file in HTML.
