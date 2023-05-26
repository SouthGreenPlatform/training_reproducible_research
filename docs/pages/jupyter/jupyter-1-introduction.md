## Context

There are typical guidelines for keeping a notebook of wet-lab work :

1. Record everything you do in the lab, even if you are following a published procedure.
2. If you make a mistake, put a line through the mistake and write the new information next to it.
3. Use a ball point pen so that marks will not smear nor will they be erasable.
4. Use a bound notebook so that tear-out would be visible.
5. When you finish a page, put a corner-to corner line through any blank parts that could still be used for data entry.
6. All pages must be pre-numbered.
7. Write a title for each and every new set of entries.
8. It is critical that you enter all procedures and data directly into your notebook in a timely manner.
9. Properly introduce and summarize each experiment.
10. The investigator and supervisor must sign each page.

But for dry-lab work... :fearful:

The concept of the notebook is not new, as these quotes show.

!!! quote "Literate programming"
  *Instead of imagining that our main task is to instruct a computer what to do, let us concentrate rather on explaining to human beings what we want a computer to do.* - Donald Knuth (1984)

!!! quote "Literate computing"
  *A literate computing environment is one that allows users not only to execute commands interactively, but also to store in a literate document the results of these commands along with figures and free-form text.*
  - Millman KJ and Perez F (2014)

And the concept was already in place in the 1980s

<figure markdown>
  ![First notebook](../images/jupyter_first_notebook.jpg){ width="300" }
  <figcaption>Wolfram Mathematica notebook (1987)</figcaption>
</figure>

This notebook concept has evolved since then and in this session we will present Jupyter Notebook.
## A solution : Jupyter ! 

The Jupyter Notebook is an open-source web application that allows you to
create and share documents that contain code, equations, visualizations and
text. The functionality is partly overlapping with R Markdown (see the
[tutorial](r-markdown-1-introduction)), in that they both use markdown and code
chunks to generate reports that integrate results of computations with the code
that generated them. Jupyter Notebook comes from the Python community while
R Markdown was developed by RStudio, but you could use most common programming
languages in either alternative. In practice though, it's quite common that
R developers use Jupyter but probably not very common that Python developers
use RStudio. Some reasons to use Jupyter include:

* Python is lacking a really good IDE for doing exploratory scientific data
  analysis, like RStudio or Matlab. Some people use Jupyter simply as an
  alternative for that.
* The community around Jupyter notebooks is large and dynamic, and there are
  lots of tools for sharing, displaying or interacting with notebooks.
* An early ambition with Jupyter notebooks (and its predecessor IPython
  notebooks) was to be analogous to the lab notebook used in a wet lab. It
  would allow the data scientist to document his or her day-to-day work and
  interweave results, ideas, and hypotheses with the code. From
  a reproducibility perspective, this is one of the main advantages.
* Jupyter notebooks can be used, just like R Markdown, to provide a tighter
  connection between your data and your results by integrating results of
  computations with the code that generated them. They can also do this in an
  interactive way that makes them very appealing for sharing with others.

As always, the best way is to try it out yourself and decide what to use it
for!

This tutorial depends on files from the course GitHub repo. Take a look at the
[setup](pre-course-setup) for instructions on how to set it up if you haven't
done so already. Then open up a terminal and go to
`training_reproducible_research/tutorials/jupyter` and activate your
`jupyter-env` Conda environment.

!!! Info "A note on nomenclature"
    - Jupyter: a project to develop open-source software, open-standards, and
    services for interactive computing across dozens of programming
    languages. Lives at [jupyter.org](https://jupyter.org).
    - Jupyter Notebook: A web application that you use for creating and
    managing notebooks. One of the outputs of the Jupyter project.
    - Jupyter notebook: The actual `.ipynb` file that constitutes your
    notebook.
