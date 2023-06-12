Another notebook? But why? We have already seen R markdown and Jupyter. That's true, but Quarto is the new kid on the block and it's already getting a lot of attention!

<figure markdown>
  ![Timeline](../images/quarto_timeline.png)
  <figcaption>Appearance of packages allowing the creation of notebooks (<a href="https://camembr.quarto.pub/hello-quarto/#/les-packages">source</a>)</figcaption>
</figure>

Quarto is an open-source scientific and technical publishing system where authors :

- Can use Jupyter notebooks or with plain text markdown in your favorite editor.
- Create dynamic content with Python, R, Julia, and Observable.
- Publish reproducible, production quality articles, presentations, websites, blogs, and books in HTML, PDF, MS Word, ePub, and more.
- Share results in a lot of publishing systems like GitHub.

His goal ? Unify and extend the R Markdown ecosystem by

1. unifing R Markdown fans
2. extending the ecosystem to those who don't know R Markdown

In addition, Quarto presents itself as the new open-source system for publishing scientific and technical articles with the aim of making the process of creating and collaboration process radically simpler

## Quarto highlights

During the Rstudio Conf 2022, Quarto was presented with the following 4 highlights: 

1. Consistent implementation of attractive and handy features across outputs: tabsets, code-folding, syntax highlighting, etc.
2. More accessible defaults as well as better support for accessibility
3. Guardrails, particularly helpful for new learners: YAML completion, informative syntax errors, etc.
4. Support for other languages like Python, Julia, Observable, and more via Jupyter engine for executable code chunks.

The original presentation is [here](https://mine.quarto.pub/hello-quarto/#/hello-quarto-title)

## One to rule them all

Quarto CLI orchestrates each step of rendering

<figure markdown>
  ![Timeline](../images/quarto_orchastration.png)
  <figcaption><a href="https://mine.quarto.pub/hello-quarto/#/quarto-cli-orchestrates-each-step-of-rendering">Source</a></figcaption>
</figure>

This tutorial depends on files from the course GitHub repo. Take a look at the
[setup](../course-information/pre-course-setup.md) for instructions on how to set it up if you haven't
done so already. As a reminder, go [here](https://quarto.org/docs/get-started/) 
and download the last version of Quarto.