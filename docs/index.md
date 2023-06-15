{% raw %}
# Tools for Reproducible Research

![](pages/images/achievement-agreement-arms-1068523.jpg)

## Course overview

<img src="https://www.svgrepo.com/show/305241/github.svg"
    width="20" height="20"/>
    [GitHub repository]( {{config.repo_url}})
<img src="https://www.svgrepo.com/show/20800/event-date-and-time-symbol.svg"
    width="20" height="20"/>
    14 - 16 Juin, 2023

One of the key principles of proper scientific procedure is the act of
repeating an experiment or analysis and being able to reach similar
conclusions. Published research based on computational analysis (*e.g.*
bioinformatics or computational biology) have often suffered from incomplete
method descriptions (*e.g.* list of used software versions); unavailable raw
data; and incomplete, undocumented and/or unavailable code. This essentially
prevents any possibility of reproducing the results of such studies. The term
“reproducible research” has been used to describe the idea that a scientific
publication should be distributed along with all the raw data and metadata used
in the study, all the code and/or computational notebooks needed to produce
results from the raw data, and the computational environment or a complete
description thereof.

Reproducible research not only leads to proper scientific conduct, but also
enables other researchers to build upon previous work. Most importantly, the
person who organizes their work with reproducibility in mind will quickly
realize the immediate personal benefits: an organized and structured way of
working. The person that most often has to reproduce your own analysis is your
future self!

## Course content and learning outcomes

The following topics and tools are covered in the course:

* Data management
* Project organisation
* Git
* Conda
* Snakemake
* Nextflow
* R Markdown
* Jupyter
* Docker
* Singularity

At the end of the course, students should be able to:

* Use good practices for data analysis and management
* Clearly organise their bioinformatic projects
* Use the version control system Git to track and collaborate on code
* Use the package and environment manager Conda
* Use and develop workflows with Snakemake and Nextflow
* Use R Markdown and Jupyter Notebooks to document and generate automated
  reports for their analyses
* Use Docker and Singularity to distribute containerized computational
  environments

## Application

This is an {{config.extra.institute}} course. The course is open for PhD students, postdocs,
group leaders and core facility staff related to the {{config.extra.institute}} Platform (IRD,
CIRAD, INRAE and the Alliance Bioversity international-CIAT).

The only entry requirements for this course is a basic knowledge of Unix systems
(*i.e.* being able to work on the command line) as well as at least a basic
knowledge of either R or Python.

Due to limited space the course can accommodate maximum of 20 participants. If
we receive more applications, participants will be selected based on several
criteria. Selection criteria include correct entry requirements, motivation to
attend the course. We also take in consideration a balance between the different
institute and department.

Please note that {{config.extra.institute}} training events do not provide any formal university
credits. The training content is estimated to correspond to a certain number of
credits, however the estimated credits are just guidelines. If formal credits
are crucial, the student needs to confer with the home department before
submitting a course application in order to establish whether the course is
valid for formal credits or not.

By accepting to participate in the course, you agree to follow the [Code of Conduct](pages/course-information/code-of-conduct.md).

## Schedule

You can find the course schedule at [this page](pages/course-information/schedule.md).

## Location

This course round is given on site. It will take place in the Badiane room at Agropolis.

## Course material

The [pre-course setup](pages/course-information/pre-course-setup.md)
page lists all the information you need before the course starts. The most
important part is the installation and setup of all the tools used in the
course, so make sure you've gone through it all for the course start.

## Teachers

* Jacques Dainat (course responsible) <a itemprop="sameAs" content="https://orcid.org/0000-0002-6629-0173" href="https://orcid.org/0000-0002-6629-0173" target="orcid.widget" rel="noopener noreferrer" style="vertical-align:top;"><img src="https://orcid.org/sites/default/files/images/orcid_16x16.png" style="width:1em;margin-right:.5em;" alt="ORCID iD icon"></a>
* Thomas Denecker (teacher) <a itemprop="sameAs" content="https://orcid.org/0000-0003-1421-7641" href="https://orcid.org/0000-0003-1421-7641" target="orcid.widget" rel="noopener noreferrer" style="vertical-align:top;"><img src="https://orcid.org/sites/default/files/images/orcid_16x16.png" style="width:1em;margin-right:.5em;" alt="ORCID iD icon"></a>
* Aurore Comte (teacher) <a itemprop="sameAs" content="https://orcid.org/0000-0002-6891-5739" href="https://orcid.org/0000-0002-6891-5739" target="orcid.widget" rel="noopener noreferrer" style="vertical-align:top;"><img src="https://orcid.org/sites/default/files/images/orcid_16x16.png" style="width:1em;margin-right:.5em;" alt="ORCID iD icon"></a>
* Gautier Sarah (teacher) <a itemprop="sameAs" content="https://orcid.org/0000-0001-5179-972X" href="https://orcid.org/0000-0001-5179-972X" target="orcid.widget" rel="noopener noreferrer" style="vertical-align:top;"><img src="https://orcid.org/sites/default/files/images/orcid_16x16.png" style="width:1em;margin-right:.5em;" alt="ORCID iD icon"></a>
* Julie Orjuela (teacher) <a itemprop="sameAs" content="https://orcid.org/0000-0001-8387-2266" href="https://orcid.org/0000-0001-8387-2266" target="orcid.widget" rel="noopener noreferrer" style="vertical-align:top;"><img src="https://orcid.org/sites/default/files/images/orcid_16x16.png" style="width:1em;margin-right:.5em;" alt="ORCID iD icon"></a>
* Nicolas Fernandez (teacher) <a itemprop="sameAs" content="https://orcid.org/0000-0001-8490-3714" href="https://orcid.org/0000-0001-8490-3714" target="orcid.widget" rel="noopener noreferrer" style="vertical-align:top;"><img src="https://orcid.org/sites/default/files/images/orcid_16x16.png" style="width:1em;margin-right:.5em;" alt="ORCID iD icon"></a>
* Sébastien Ravel (Helper) <a itemprop="sameAs" content="https://orcid.org/0000-0001-6663-782X" href="https://orcid.org/0000-0001-6663-782X" target="orcid.widget" rel="noopener noreferrer" style="vertical-align:top;"><img src="https://orcid.org/sites/default/files/images/orcid_16x16.png" style="width:1em;margin-right:.5em;" alt="ORCID iD icon"></a>

## Contact

To contact us, please send a mail using the contact form available [here]({{contact}}).

## Acknowledgement

This work is based on the NBIS / ELIXIR course *Tools for Reproducible Research* that can be found [here](https://github.com/NBISweden/workshop-reproducible-research). We extend our gratitude to the creators and providers of the training material used in this course.

{% endraw %}