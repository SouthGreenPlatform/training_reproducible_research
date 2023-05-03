!!! info "The programme of this section"
    In this section we will learn:
    
    - markdown
    - how to create an R-markdonw file
    - How to use the different elements that make up a markdown file 
    - How to render the results

## A markup language

A *markup language* is a system for annotating text documents in order to
*e.g.* define formatting. HTML, if you are familiar with that, is an example of
a markup language. HTML uses tags, such as:

```html title="Example in HTML"
<h1>Heading</h1>
<h2>Sub-heading</h2>
<a href="www.webpage.com">Link</a>
<ul>
  <li>List-item1</li>
  <li>List-item2</li>
  <li>List-item3</li>
</ul>
```

and this is the result :

<h1>Heading</h1>
<h2>Sub-heading</h2>
<a href="http://example.com">Link</a>
<ul>
  <li>List-item1</li>
  <li>List-item2</li>
  <li>List-item3</li>
</ul>

## Markdown

*Markdown* is a lightweight markup language which uses plain-text syntax in
order to be as unobtrusive as possible, so that a human can easily read it.
The code below gives the same result as the HTML code shown above : 

```markdown title="Example in markdown"
# Heading

## Sub-heading

### Another deeper heading

A [link](http://example.com).

Text attributes _italic_, *italic*, **bold**, `monospace`.

Bullet list:

  * apples
  * oranges
  * pears
```

A markdown document can be converted to other formats, such as HTML or PDF, for
viewing in a browser or a PDF reader. For example, the page you are reading right now is
written in markdown. Markdown is somewhat ill-defined, and as a consequence of
that there exist many implementations and extensions, although they share most
of the syntax. *R Markdown* is one such implementation/extension.

## R markdown

![hex-rmarkdown](../images/hex-rmarkdown.png){ align=left width=200 }

R Markdown documents can be used both to save and execute code and to generate
reports in various formats. This is done by mixing markdown (as in the example
above), and so-called code chunks in the same document. The code itself, as
well as the output it generates, can be included in the final report.

R Markdown makes your analysis more reproducible by connecting your code,
figures and descriptive text. You can use it to make reproducible reports,
rather than *e.g.* copy-pasting figures into a Word document. You can also use
it as a notebook, in the same way as lab notebooks are used in a wet lab
setting (or as we utilise Jupyter notebooks in the tutorial after this one).

This tutorial depends on files from the course GitHub repo. Take a look at the
[setup](pre-course-setup) for instructions on how to set it up if you haven't
done so already. Place yourself in the `training_reproducible_research/tutorials/rmarkdown/`
directory, create and activate your `rmarkdown-env` Conda environment and start RStudio
from the command line (type `rstudio &`).

An example before we start? A screenshot of an R markdown file...
<div align="center" markdown>

![hex-rmarkdown](../images/exampleRmarkdown_code.png)

</div>

and on the right its result in HTML.

<div align="center" markdown>

![hex-rmarkdown](../images/exampleRmarkdown_result.png)

</div>

