# Putting everything together
## Review of the sessions

<figure markdown>
  ![](../images/whats_in_it_for_me.png)
  <figcaption>By working reproducibly you will also make your life a lot easier!</figcaption>
</figure>

### What have we learned?

- How to use the version control system Git to track changes to code
- How to use the package and environment manager Conda
- How to use the workflow managers Snakemake and Nextflow
- How to use R Markdown and Jupyter to generate automated reports and to document your analyses
- How to use Docker and Singularity to distribute containerized computational
environments

### Divide your work into distinct projects

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
### What to do with the different data ?

You must keep your input data read-only - consider it static. Don't create different versions of the input data - write a script, R Markdown document, Jupyter notebook or a Snakemake / Nextflow workflow if you need to preprocess your input data so that the steps can be recreated. Of course, **BACKUP** your data! Keep redundant copies in different physical locations (3-2-1 backup rule).

<figure markdown>
  ![](../images/3-2-1-Backup-Rule.png)
  <figcaption><a href='https://www.msp360.com/resources/blog/following-3-2-1-backup-strategy/'>source</a></figcaption>
</figure>

And of course in an open science & FAIR approach, upload your raw data as soon as possible to a public data repository

### What is reasonable for your project?

The **minimal** level is to write code in a reproductible way. You can connect your results with the code (R markdown, Juyter notebooks, ...) and why not convert your code into a Snakemake / Nexflow workflow.

The **good** level is to add the code versionning. You can use Git for versionning and collaboration and publish your code along with your results on GitHub, GitLab,...

A **better** level would be to add the organisation of software dependencies. You can use conda  to install software in environments that can be easily exported and installed on a different system.

The **best** level would be to add an export of everything. You can completly recreate he compute system with docker or singularity container.

### Alternatives

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

## And now ?

### Create a project from scratch !

It is time to try to set up a project from scratch and use the different
tools that we have covered during the course together! This exercise is very
open-ended and you have free hands to try out a bit of what you want. But you
should aim to use what you've learned to do the following:

1. Create a new git repository for the project (either on BitBucket or GitHub)

2. Add a README file which should contain the required information on how to
   run the project

3. Create a Conda `environment.yml` file with the required dependencies

4. Create a R Markdown or Jupyter notebook to run your code

5. Alternatively, create a `Snakefile` to run your code as a workflow and use a `config.yml` file to add settings to the workflow

6. Use git to continuously commit changes to the repository

7. Possibly make a Docker or Singularity image for your project

This is not a small task and may seem overwhelming! Don't worry if you feel
lost or if the task seems daunting. To get the most out of the exercise, take
one step at a time and go back to the previous tutorials for help and
inspiration. The goal is not necessarily for you to finish the whole exercise,
but to really think about each step and how it all fits together in practice.

!!! note "Recommendation"
    We recommend to start with git, Conda and a notebook, as we would see these as
    the core tools to make a research project reproducible. We suggest to keep the
    analysis for this exercise short so that you have time to try out the different
    tools together while you have the opportunity to ask for help.

### Your own project

This is a great opportunity for you to try to implement these methods on one
of your current research projects. It is of course up to you which tools to
include in making your research project reproducible, but we suggest to aim
for at least git and Conda.

!!! tip
    If your analysis project contains computationally intense steps it may be
    good to scale them down for the sake of the exercise. You might, for
    example, subset your raw data to only contain a minuscule part of its
    original size. You can then test your implementation on the subset and only
    run it on the whole dataset once everything works to your satisfaction.

### Alternative: student experience project

If you don't want to use a project you're currently working on we have
a suggestion for a small-scale project for you. The idea is to analyze
students' experiences at this Reproducible Research course. For this you will
use responses from students to the registration form for the course. Below
you'll find links to files in `*.csv` format with answers from 3 course instances:

2018-11<br>
<font size="2"><a href='https://docs.google.com/spreadsheets/d/1yLcJL-rIAO51wWCPrAdSqZvCJswTqTSt4cFFe_eTjlQ/export?format=csv'>https://docs.google.com/spreadsheets/d/1yLcJL-rIAO51wWCPrAdSqZvCJswTqTSt4cFFe_eTjlQ/export?format=csv</a></font><br>
2019-05<br>
<font size="2">
<a href='https://docs.google.com/spreadsheets/d/1mBp857raqQk32xGnQHd6Ys8oZALgf6KaFehfdwqM53s/export?format=csv'>https://docs.google.com/spreadsheets/d/1mBp857raqQk32xGnQHd6Ys8oZALgf6KaFehfdwqM53s/export?format=csv</a>
</font><br>
2019-11<br>
<font size="2">
<a href='https://docs.google.com/spreadsheets/d/1aLGpS9WKvmYRnsdmvvgX_4j9hyjzJdJCkkQdqWq-uvw/export?format=csv'>https://docs.google.com/spreadsheets/d/1aLGpS9WKvmYRnsdmvvgX_4j9hyjzJdJCkkQdqWq-uvw/export?format=csv</a>
</font>

The goal here is to create a Snakemake workflow, which contains the following:

1. Has a rule that downloads the `csv` files (making use of a `config.yml` file
   to pass the URLs and file names)

2. Has a rule that cleans the files (making use of `wildcards` so that the same
   rule can be run on each file)

3. The final step is to plot the student experience in some way

!!! attention "Remember to"
    * Keep everything versioned controlled with `git`
    * Add information to the `README` file so others know how to re-run
      the project
    * Add required software to the Conda `environment.yml` file

### Inspiration and tips for the student experience workflow

The first two steps should be part of the Snakemake workflow. If you need some help
with the cleaning step, see below for a Python script that you can save to a file
and run in the second Snakemake rule.

??? example "Click to show a script for cleaning column names"
    The script (*e.g.* `clean_csv.py`):

    ```python
    #!/usr/bin/env python
    import pandas as pd
    from argparse import ArgumentParser

    def main(args):
        df = pd.read_csv(args.input, header=0)
        df.rename(columns=lambda x: x.split("[")[-1].rstrip("]"), inplace=True)
        df.rename(columns={'R Markdown': 'RMarkdown'}, inplace=True)
        df.to_csv(args.output, index=False)

    if __name__ == '__main__':
        parser = ArgumentParser()
        parser.add_argument("input", type=str,
                            help="Input csv file")
        parser.add_argument("output", type=str,
                            help="Output csv file cleaned")
        args = parser.parse_args()
        main(args)
    ```

    Command to execute the script:

    ```
    python clean_csv.py input_file.csv output_file.csv
    ```

The third step is really up to you how to implement. You could:

* Include the plotting in the workflow using an RMarkdown document that
  gets rendered into a report
* Have a script that produces separate figures (*e.g.* `png` files)
* Create a jupyter notebook that reads the cleaned output from the workflow
  and generates some plot or does other additional analyses

If you need some help/inspiration with plotting the results, click below
to see an example Python script that you can save to file and run with
the cleaned files as input.

??? example "Click to show a script for plotting the student experience"
    The script (*e.g.* `plot.py`):

    ```python
    #!/usr/bin/env python
    import matplotlib as mpl
    import matplotlib.pyplot as plt
    plt.style.use('ggplot')
    mpl.use('agg')
    import pandas as pd
    import seaborn as sns
    import numpy as np
    from argparse import ArgumentParser

    def read_files(files):
        """Reads experience counts and concatenates into one dataframe"""
        df = pd.DataFrame()
        for i, f in enumerate(files):
            # Extract date
            d = f.split(".")[0]
            _df = pd.read_csv(f, sep=",", header=0)
            # Assign date
            _df = _df.assign(Date=pd.Series([d]*len(_df), index=_df.index))
            if i==0:
                df = _df.copy()
            else:
                df = pd.concat([df,_df], sort=True)
        return df.reset_index().drop("index",axis=1).fillna(0)

    def count_experience(df, normalize=False):
        """Generates long format dataframe of counts"""
        df_l = pd.DataFrame()
        for software in df.columns:
            if software=="Date":
                continue
            # Groupby software and count
            _df = df.groupby(["Date",software]).count().iloc[:,0].reset_index()
            _df.columns = ["Date","Experience","Count"]
            _df = _df.assign(Software=pd.Series([software]*len(_df),
                index=_df.index))
            if normalize:
                _df = pd.merge(_df.groupby("Date").sum().rename(columns={'Count':'Tot'}),_df, left_index=True, right_on="Date")
                _df.Count = _df.Count.div(_df.Tot)*100
                _df.rename(columns={'Count': '%'}, inplace=True)
            df_l = pd.concat([df_l, _df], sort=True)
        df_l.loc[df_l.Experience==0,"Experience"] = np.nan
        return df_l


    def plot_catplot(df, outdir, figname, y, palette="Blues"):
        """Plot barplots of user experience per software"""
        ax = sns.catplot(data=df, x="Date", col="Software", col_wrap=3, y=y,
            hue="Experience", height=2.8,
                         kind="bar",
                         hue_order=["Never heard of it",
                                    "Heard of it but haven't used it",
                                    "Tried it once or twice", "Use it"],
                         col_order=["Conda", "Git", "Snakemake", "Jupyter",
                                    "RMarkdown", "Docker", "Singularity"],
                         palette=palette)
        ax.set_titles("{col_name}")
        plt.savefig("{}/{}".format(outdir, figname), bbox_to_inches="tight",
            dpi=300)
        plt.close()

    def plot_barplot(df, outdir, figname, x):
        """Plot a barplot summarizing user experience over all software"""
        ax = sns.barplot(data=df, hue="Date", y="Experience", x=x, errwidth=.5,
                    order=["Never heard of it",
                           "Heard of it but haven't used it",
                           "Tried it once or twice", "Use it"])
        plt.savefig("{}/{}".format(outdir, figname), bbox_inches="tight",
            dpi=300)
        plt.close()

    def main(args):
        # Read all csv files
        df = read_files(args.files)
        # Count experience
        df_l = count_experience(df)
        # Count and normalize experience
        df_lp = count_experience(df, normalize=True)
        # Plot catplot of student experience
        plot_catplot(df_l, args.outdir, "exp_counts.png", y="Count")
        # Plot catplot of student experience in %
        plot_catplot(df_lp, args.outdir, "exp_percent.png", y="%",
                     palette="Reds")
        # Plot barplot of experience
        plot_barplot(df_lp, args.outdir, "exp_barplot.png", x="%")

    if __name__ == '__main__':
        parser = ArgumentParser()
        parser.add_argument("files", nargs="+",
            help="CSV files with student experience to produce plots for")
        parser.add_argument("--outdir", type=str, default=".",
            help="Output directory for plots (defaults to current directory)")
        args = parser.parse_args()
        main(args)
    ```

    Command to execute the script:

    ```
    python plot.py file1.csv file2.csv file3.csv --outdir results/
    ```

## To end on a high note !

To conclude this session, we offer you a demo to go further into reproducibility. We will : 
1. Create a repo on Github
2. Create a README and set a license
3. Add a conda file and our Jupyter note book file
4. Update the README to explain how to edit it and use quarto to generate the page in HTML
5. Publish this page on GitHub and put it online
6. Make a release with Zenodo to have a DOI of your code
7. Set up a contributors file
8. See how to archive the repository on Software heritage

You can find a support with different screenshots if you want try it yourself ([here](https://moodle.france-bioinformatique.fr/pluginfile.php/346/course/section/47/09_expose_your_work_github.pdf))

Et voilà !
