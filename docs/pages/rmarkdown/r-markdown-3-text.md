Some commonly used formatting written in markdown is shown below, which you may
recognize from the [Git tutorial](git-7-working-remotely):

```no-highlight
# This is a heading

This is a paragraph.
This line-break will not appear in the output file.\
But this will (since the previous line ends with a backslash).

This is a new paragraph.

## This is a sub-heading

This is **bold text**, this is *italic text*, this is `monospaced text`,
and this is [a link](http://rmarkdown.rstudio.com/lesson-1.html).

An important feature of R Markdown is that you are allowed to use R code
inline to generate text by enclosing it with `r `. As an example: 112/67 is
equal to `r round(112/67, 2)`. You can also use multiple commands like this:
I like `r fruits <- c("apples","bananas"); paste(fruits, collapse = " and ")`!
```

The above markdown would generate something like this:

> ![](images/markdown_example.png){ width=600px }

Instead of reiterating information here, take a look on the first page (only
the first page!) of this [reference]( https://www.rstudio.com/wp-content/uploads/2015/03/rmarkdown-reference.pdf).
This will show you how to write more stuff in markdown and how it will be
displayed once the markdown document is converted to an output file (*e.g.*
HTML or PDF). An even more complete guide is available
[here](http://rmarkdown.rstudio.com/authoring_pandoc_markdown.html).

* Try out some of the markdown described above (and in the links) in your
  template R Markdown document! Press *Knit* to see the effect of your changes.
  Don't worry about the code chunks just yet, we'll come to that in a second.

!!! Success "Quick recap"
    In this section you learned and tried out some of the basic markdown
    syntax.
