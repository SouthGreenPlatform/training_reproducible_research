
## Divide your work into distinct projects

- Keep all files needed to go from raw data to final results in a dedicated directory
- Use relevant subdirectories
- Many software support the “project way of working”, e.g. Rstudio and the text editors
Sublime Text and Atom
- Use Git to create structured and version controlled project repositories

Everything can be a project ! For example, you can find a project directory tempalte proposed by NBIS ([repo](https://github.com/NBISweden/project_template)):

```
project
|- doc/                documentation for the study
|
|- data/               raw and primary data, essentially all input files, never edit!
|  |- raw_external/
|  |- raw_internal/
|  |- meta/
|
|- code/               all code needed to go from input files to final results
|- notebooks/
|
|- intermediate/       output files from different analysis steps, can be deleted
|- scratch/            temporary files that can be safely deleted or lost
|- logs/               logs from the different analysis steps
|
|- results/            output from workflows and analyses
|  |- figures/
|  |- tables/
|  |- reports/
|
|- .gitignore          sets which parts of the repository that should be git tracked
|- Snakefile           project workflow, carries out analysis contained in code/
|- config.yml          configuration of the project workflow
|- environment.yml     software dependencies list, used to create a project environment
|- Dockerfile          recipe to create a project container
```

An other proposition: 

<figure markdown>
  ![Folder architecture](../images/project-organisation.png){ width="100%" }
  <figcaption>Data management tips by Kira Höffler (<a href='https://du-bii.github.io/module-5-Methodes-Outils/seance3_goodpractices/images/Infographic_Data_Management_v02-02_KH.pdf'>source</a>)</figcaption>
</figure>

## Files: naming and format

### Naming

- Brief and to the point
- No spaces or special characters
- With the right date format
- With the most important element first
- With the document version

<figure markdown>
  ![Folder architecture](../images/project-date.png){ width="100%" }
  <figcaption>Date format (<a href='https://xkcd.com/1179/'>source</a>)</figcaption>
</figure>

### Format

- Non-proprietary if possible
- Formats that lose the least data on conversion
- The format used by the community

## Write a good READ ME

An other example from Recheche data gouv ([source](https://recherche.data.gouv.fr/fr/categorie/33/guide/modele-de-readme))

```
<Help text is included in angle brackets and should be deleted before saving.> 
 
<A README: Why ?
 
***The documentation of a dataset should be sufficient to enable any reuser to understand and evaluate its quality. The README provides complementary and accessible information that is not provided through the dataset’s metatada, and its file’s metadata, and/or associated files, or files that are publicly accessible on a long term hosting service (file storage or publication). In the latter case, please include the documents’ persistent URLs or their references***.>
 
<Prefer text document (.txt,) or markdown (.md) as file format>
 
RDG README File Template --- General --- Version: 0.1 (2022-10-04) 
 
This README file was generated on [YYYY-MM-DD] by [NAME].
Last updated: [YYYY-MM-DD].
 
# GENERAL INFORMATION
 
## Dataset title:
 
## DOI:
 
## Contact email:
 
<Here is a list of suggested items to help you enrich your documentation if necessary. Some may not be applicable, depending on the dataset’s discipline or context of production.>
 
<***Remove or add any section if applicable***>
 
# METHODOLOGICAL INFORMATION 
 
## Environmental/experimental conditions: 
 
## Description of sources and methods used to collect and generate data:
<If applicable, describe standards, calibration information, facility instruments, etc. > 
 
## Methods for processing the data: 
< If applicable, describe how submitted data were processed and include details that may be important for data reuse or replication. Add comments to explain each step taken.
For example, include data cleaning and analysis methods; code and/or algorithms, de-identification procedures for sensitive data human subjects or endangered species data.> 
 
## Quality -assurance procedures performed on the data: 
 
## Other contextual information:
<Any information that you consider important for the evaluation of the dataset’s quality and reuse thereof: for example, information about the software required to interpret the data. 
If applicable and not covered above, include full name and version of software, and any necessary packages or libraries needed to read and interpret the data, *e.g.* to run scripts.>
 
 
# DATA & FILE OVERVIEW
 
 
## File naming convention:
 
## File hierarchy convention:
 
 
# DATA-SPECIFIC INFORMATION FOR: [FILENAME]
 
<Repeat this section for each folder or file, as appropriate. Recurring items may also be explained in a common initial section.>
 
<For tabular data, provide a data dictionary/code book containing the following information:>
## Variable/Column List:
For each variable or column name, provide: 

	-- full “human readable” name of the variable, 
	-- description of the variable, 
	-- unit of measurement if applicable, 
	-- decimal separator *i.e.* comma or point if applicable
	-- allowed values : list of values or range, or domain
	-- format if applicable, e.g. date>
 
## Missing data codes: 
<Define codes or symbols used to indicate missing data.>
 
## Additional information: 
<Any relevant information you consider useful to better understand the file>
```

## What to do with the different data ?

You must keep your input data read-only - consider it static. Don't create different versions of the input data - write a script, R Markdown document, Jupyter notebook or a Snakemake / Nextflow workflow if you need to preprocess your input data so that the steps can be recreated. Of course, **BACKUP** your data! Keep redundant copies in different physical locations (3-2-1 backup rule).

<figure markdown>
  ![](../images/3-2-1-Backup-Rule.png)
  <figcaption>3-2-1 Backup rule (<a href='https://www.msp360.com/resources/blog/following-3-2-1-backup-strategy/'>source</a>)</figcaption>
</figure>

And of course in an open science & FAIR approach, upload your raw data as soon as possible to a public data repository

## What is reasonable for your project?

The **minimal** level is to write code in a reproductible way. You can connect your results with the code (R markdown, Juyter notebooks, ...) and why not convert your code into a Snakemake / Nexflow workflow.

The **good** level is to add the code versionning. You can use Git for versionning and collaboration and publish your code along with your results on GitHub, GitLab,...

A **better** level would be to add the organisation of software dependencies. You can use conda  to install software in environments that can be easily exported and installed on a different system.

The **best** level would be to add an export of everything. You can completly recreate he compute system with docker or singularity container.

## Alternatives

There are of course alternatives to all the tools presented in this course such as: 

| Presented      | Alternative                          |
| -------------- | ------------------------------------ |
| **Git**       | **Mecurial** (Distributed model just like Git, close to sourceforge.), **Subversion** (Centralized model unlike git/mercurial; no local repository on your computer and somewhat easier to use) |
| **Conda**       | **Pip** (Package manager for Python, has a large repository at pypi.), **Apt/yum/brew** (Native package managers for different OS. Integrated in OS and might deal with e.g. update notifications better), **virtualenv** (Environment manager used to set up semi-isolated python environments)  |
| **Conda**       | **Make** (Used in software development and has been around since the 70s. Flexible but notoriously obscure syntax.), **Galaxy** (attempts to make computational biology accessible to researchers without programming experience by using a GUI.)  |
| **Jupyter**, **R markdown**, **Quarto**       | **Zeppelin** (Developed by Apache. Closely integrated with Spark for distributed computing and Big Data applications.), **Beaker** (Newcomer based on Ipython, just as Jupyter. Has a focus on integrating multiple languages in the same notebook.)  |
| **Docker**, **Sigularity** | **Shifter** (Similar ambition as Singularity, but less focus on mobility and more on resource management), **VirtualBox/VMWare** (Virtualization rather than containerization. Less lightweight, but no reliance on host kernel.)  |

## In conclusion, what's in it for me ? 

<div align="center" markdown>
![](../images/calvin_hobbes_past_corresponding.png)
</div>
