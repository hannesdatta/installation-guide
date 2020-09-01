% Managing data- and computation-intensive research projects
% [Hannes Datta](https://hannesdatta.com)
% July 2, 2020

# Let's get started!

## This presentation

...is available at [http://tilburgsciencehub.com/slides]()

::: notes

- I invite you to view that deck to go back and forth yourselves.

worked without structure in the past

i discovered a new way of working with data- and computation-intensive projects
happy to share that vision

:::

## Agenda

- Introduction (you & me)
- Motivation for this class
- Key building blocks of efficient workflows
- Wrap-up & tips for implementation

# About you & me

## My professional background

- PhD, quantitative marketing (Maastricht University)
- [Associate professor](https://hannesdatta.com) at Tilburg University
- Research interests
    - digitization & subscription-based business models
    - marketing-mix modeling and optimization
    - branding

::: notes

Personal background

- born and raised in Germany
- moved to NL 11 years ago
- married, 2 kids (2 and 5 years old)
- streaming from 'de zolderkamer' in 's-Hertogenbosch
- geek at heart, love (to play) music

- method
    - causality in observational data
    - data management of structured and unstructured data

:::

<!--
## Current research interest

__Impact of digitization on consumers, producers__

- How did [online streaming](https://tiu.nu/spotify) (Spotify, Netflix) change behavior?
- Bunch of follow-ups
    - "Who runs Spotify?" The power of content owners versus the platform
    - [Music "filter" bubbles](https://research.tilburguniversity.edu/en/publications/streaming-services-and-the-homogenization-of-music-consumption)
    - platform incentives & production of music
- More: see [website](https://hannesdatta.com)
-->

## Your link to Tilburg

*When did you graduate?*


. . .

*Which program did you graduate from?*

. . .

*Did I ever teach you?*

::: notes

- What stage are you in?
- What are you working on right now?
- What's your ambition?
- Where are you? Kids around?

:::


# Motivation for this (short) class

## Mr. Chaos

- coded a lot (data prep, modeling), but didn't *learn how to structure my work(flows)*
- created a complete chaos (but still got published); [see here for the code/directory structure](http://tilburgsciencehub.com/workflow/structure_phd_2013.html) and [here](https://www.hannesdatta.com/publication/free-trials/) for the paper

::: notes

## Can't find stuff...

- Cannot find code that prepped the dataset
- Cannot find code of the econometric model that eventually got published

Ask students what's bad about it?

:::

## What was so bad about it?

- Replicability
    - I couldn't reproduce results whenever I wanted to
- Efficiency
    - when making changes to data or model, I had to go the the beginning, repeating all steps
    - a colleague asked me for the data years after; it wasn't properly documented!

## Why should *you* care?

- You will change code *continuously* before project is final!
- You maybe even have kept some steps in your workflow manual
- Colleagues will (have to) look at your code, or use it
    - to help you
    - to continue your work
- Small efficiency gains will pay off soon

# This (short) class

## Learning objective

Show you a few ways to increase your __efficiency__ when working on __data- and computation-intensive__ projects

::: notes

Disclaimer: there is a long version of this class, where I actually this everything


So - all I can do

:::

## What's efficient?

> - not making mistakes...
  - catching mistakes early
  - catching mistakes at all!!!
  - zero setup costs to return to a project
  - *prototype* the final product, refine later
  - rotating on tasks
  - sharing/reusing code
  - having *others* audit your code

## What's *not* efficient?

> - Waiting (e.g., for results, for estimation)
- Getting distracted while waiting
- Forgetting how things *are* done
- Forgetting how things *were* done
- Losing data
- Using code which isn't properly documented ("don't know how to use it")
- Becoming frustrated, feeling chaotic

## What's a *data*-intensive project?

- Big data: volume, variety, veracity, velocity
    - "Where prototyping on small data makes sense", memory-intense
    - data from multiple sources/formats (e.g., SQL, Excel, Mongo, ...)
    - potential errors, high investment in data cleaning
    - re-do project over and over, on updated or different data (e.g., real-time predictions)

## What's a *computation*-intensive project?

- Small data, but long computation time (CPU-intense)
- "Potential for running things in parallel", or only running the things that need to be run

## What about *your* current work?

- What do *you* feel has been __efficient__ or __unefficient__ in the way you've run projects?

- To what extent do your projects fit the criteria of __data- and computation-intensiveness__?

::: notes

Let's discuss by *type of graduation project*

:::

## How to achieve the learning objectives?

- Familiarize yourself with the ["Tilburg Science Hub"-way of setting up projects](http://tilburgsciencehub.com/workflow)

- Boost your own efficiency
    - ...by making your work reproducible & transparent
- Boost the efficiency of others
    - ...by being able to share your work and collaborate on other projects

::: notes

*Say we build on others, too!*

- Discuss own work, and how to implement suggestions

- Other's efficiency
    - Not recollect what has been collected
    - Not reprogram what has been programmed
    - Learn from one's code, etc.
    - Share ideas
- Light-weight structure: no commercial tools, readily implementable, do not need admin rights [...]

:::


## Disclaimer

> - This is a **very** short class ("rough" overview)
- [Tilburg Science Hub](http://tilburgsciencehub.com) provides the deep-dive
- Think of Tilburg Science Hub as *Scrum* ("commonly agreed system *how* to manage a project"), rather than a software product or a platform
- I don't use tools popular in business (e.g., PowerBI, Tableau)
- I'm a marketer, *not* a computer/data scientist
- Some things may be simple for some, but advanced for others
- Large-scale for us may be small-scale for you (tested on data < 2 TB, 512 GB RAM memory)
- <s>traditional lecture</s> interactive live stream

::: notes

- I will use Tilburg Science Hub a lot

- No Tablaeu/PowerBi:  - because I want to be in control

- I'm a marketer
    - I do marketing analytics
    - It’s close to data science in terms of data acquisition, but...
    - rather distant in terms of methods (e.g., ML methods only enter the field gradually; we’re mostly applied econometricians)

- In the (spontaneous) exercises, I may not know all the answers all the time – but will deliver later if required

:::

# Agenda

## Overview

- Introduction to [Tilburg Science Hub](http://tilburgsciencehub.com)
- Project setup and workflow management (selection of topics)
    - Pipelines & components
    - Data management & directory structure
    - Automation
    - Versioning
- Project templates and tutorials
    - [Reproducible text mining workflow](http://tilburgsciencehub.com/tutorial)
- Wrap-up and implementation plan

::: notes

questions before we start???

:::


# Pipelines

## Definition

*pipeline* {n.}: refers to the (usually automized) __steps necessary to build a project__; *workflow* used interchangeably

> - Examples: steps necessary to prepare data, run model, produce tables and figures

::: notes

- __What steps does your project consist of?__
- __Which steps did you already automize?__

- STAGES are the broader steps

:::

## Example: Academic paper

    - Stage 1: Prepare dataset for analysis
        - Step 1a: download raw data
        - Step 1b: clean data
        - Step 1c: aggregate data
    - Stage 2: Run model on a dataset
        - Step 2a: various variable configurations
        - Step 2b: select best fitting model
    - Stage 3: Produce tables and figures for the paper
        - Step 3a: load result of best-fitting model
        - Step 3b: produce output table

## Drafting a pipeline

![Directed acyclic graph (DAG)](./images/make_flowchart.png)

. . .

- white boxes (inputs or outputs; concurrently!)
- red boxes (transformation by rules)

## Benefits of pipelines

- write clearer source code: smaller code chunks
- obtain results faster: automation (redo); change inputs & check outputs
- increase transparency and collaboration: work in different parts of pipeline
- software stack: full flexibility

## Discussion

__What are common pipeline stages in your domain?__

::: notes

as an academic, it's data-prep, model, writing

(What stages would you choose to change, remove, add?)

Think of:
    - what steps do I do, what steps do others do?
    - other deployment stages: e.g., dashboards, etc.

:::

# Components of a pipeline

## Definition

*pipeline components* {n}: refer to a project's building blocks, consisting of source code, data, generated files, and notes.

## (1) Source code

inputs [data, arguments] &#8594; transformation &#8594; output [datasets, log files, images]

. . .

- Examples:
    - load data from web, save locally as CSV
    - clustering: argument (set *k* for k-means); load matrix of tag words, cluster with *k*, save IDs & cluster IDs to csv
    - load results, compute fit statistics, output to .txt file
    - ...

::: notes

- responsible to **transform inputs into outputs**

:::

## (2) Raw data

- Data *stored remotely*
    - File-based systems (e.g., S3, FTP, Dropbox, Drive)
    - Databases (e.g., MongoDB, MySQL)
    - Get'em all: use our get-data tool!

- Those needed are downloaded *locally* (!)

- [Documented with `readme.txt`](http://tilburgsciencehub.com/workflow/documenting-data)!

::: notes

how do YOU store data?

:::

## (3) Generated files

- These are the *outputs* of your source code.
- Think about cleaned data sets, results of analysis, etc.
- If *final* --> "output"
- If *temporary* --> "temp"
- If used for auditing --> "audit"

::: notes

do you keep them separate? how?

:::


## (4) Notes

- Documentation, literature, PDFs, ...
- Keep in separate folder, with potentially subfolders

::: notes

where do YOU store them?

:::


## Conceptual framework

![](images/workflow.png){ width=800px }

::: notes

- pipeline = logical steps in building project
- components = nuclear units

- why?
  - full portability across colleagues, computers
  - reproducibility and transparency (nothing manually edited)

:::

## Discussion

__What are the benefits (or drawbacks) of keeping project components separate?__

::: notes

. . .

__Do you keep them separate, or not (and why)?__

benefits: each has its own "data management" policies attached to it
e.g., code needs to be versioned, raw data does not


:::

# Data Management and Directory Structure

## Guiding principles

- Others should understand pipeline, merely by *looking at file/directory structure*
- Each step in pipeline is *self-contained* ("portability")
- Project is *versioned & backed-up* (more later)

## Project directory structure (1)

- Three main folders: `src`, `gen`, and `data`
- Subfolders represent pipeline stages (e.g., `data-prep`, `analysis`, `paper`)

```
\src\data-prep       <- SOURCE CODE
\src\analysis
\src\paper

\gen\data-prep\      <- GENERATED FILES
\gen\analysis\
\gen\paper\

\data\website_A\...  <- RAW DATA
\data\company_B\...
```

## Project directory structure (2)

- Keep generated files separate: `input`, `output`, `temp`, `audit`

```
\src\data-prep       <- SOURCE CODE
\src\analysis
\src\paper
\gen\data-prep\input <- GENERATED FILES
\gen\data-prep\output
\gen\data-prep\temp
\gen\data-prep\audit
\gen\analysis\...
\gen\paper\...
\data\website_A\...  <- RAW DATA
\data\company_B\...
```
## Exploration

- Let's explore a directory structure in practice...
- E.g., view [structure of my Spotify paper](http://tilburgsciencehub.com/workflow/structure_spotify_2018.html)

__What's different from what I just told you?__

::: notes

1. Describe the directory structure – where did I store what?
2. What’s the use of the main directories in the project? (raw, derived, analysis) – why do I do it that way?
3. What’s that server directory doing?!

"project" centric - "wipeable"

"submodule centric" - self-contained, highly *portable*

:::

## Using a directory template

Please download the [directory template](http://tilburgsciencehub.com/workflow/dir_structure.zip)

__What changes would you make to *use* this template for your own work?__

# Automation

## Automate your workflow

- Build tools introduce "recipes" of how to make stuff
    - *target* __what__ needs to be built (e.g., a file)
    - *source(s)* what is __required__ to execute the build?
    - *execution* how is the build to be __executed/run__?

## Use cases

- Build only what *needs* to be built
- Quickly move code to another computer (e.g., the cloud)
- "Loop" over different model specifications
- Nightly builds

::: notes

related to the practical example given earlier

:::

## Example recipes

Let's generate some example recipes by writing __pseudo code__...

```
target: source(s)
    execution command
```

::: notes

more examples:
(a) tell me what will be built & the file names
(b) what are the dependencies
(c) how to run it, which software?

:::

## Make is *one* build tool

- Installed on Mac, Linux; [installable on Windows](http://tilburgsciencehub.com/setup/make)
- Documentation [here](http://tilburgsciencehub.com/workflow/automation/)
    - `make` runs entire workflow
    - `make -n` does a dry-run


# Let's put things in practice

## The textmining workflow template

- We have built a tutorial, available at [http://tilburgsciencehub.com/tutorial]()

- Why is it useful?
    - Runs with one command (`make`)
    - Template to kickstart your projects
    - Endless possibilities to extend

- Let's take a look at it!

## Other templates available

- see [http://tilburgsciencehub.com/examples]()

# Versioning

## Versioning the old way

- Use dates in file names, initials for authors

```
cleandata_022113.do
cleandata_022613.do
regressions.log
cleandata_022113a.do
cleandata_022613_jms.do
regressions_022413.do
regressions_022713_mg.do
regressions_022413.log
```

::: notes

- Good
    - Facilitates comparison
    - Facilitates undoing, rolling back
- Bad
    - Which log file comes from which regression?
    - Which version of `cleandata` was used to make data for `regressions`?
    - No software firm does it like that!

:::

## Versioning the new way

- Make use of software tools like Git(Hub)
    - Git is locally installed, open-source
    - GitHub is Git in the cloud; many other providers available

- Git saves *changes* rather than snapshots
- Git allows you to work *in parallel*, with others

::: notes

- show git in an example directory, and how it incrementally saves stuff
- show .gitignore

:::

## Learn and use Git!

- [More on TSH](http://tilburgsciencehub.com/workflow/versioning)
- [Wonderful cheatsheet](https://education.github.com/git-cheat-sheet-education.pdf)
- Useful for collaboration and project management
- Useful for portability across different computers, even when working on your own

# Wrap-up

## Summary

1. Manage your project as a pipeline, and have logical pipeline stages
2. Store data, code, and generated files separately, for each stage
3. Automate entire pipeline, using build tools like `make`
4. Kick-start your own projects using our templates, or use them to build your own

## How to get started?

- Start gradually
    - e.g., have a [directory structure](http://tilburgsciencehub.com/workflow/directories/) first + move files; then start to automate __step by step__
- Use projects or templates you can learn from (e.g., on [Tilburg Science Hub](http://tilburgsciencehub.com))
- Follow our [tutorials](http://tilburgsciencehub.com/tutorial)
- Use our [housekeeping checklist here](http://tilburgsciencehub.com/workflow/checklist/)

## Share & contribute

- Share [http://tilburgsciencehub.com](http://tilburgsciencehub.com) with others
- Want to contribute content? Learn how it works [here](https://github.com/hannesdatta/tilburg-science-hub/blob/tilburg-update/CONTRIBUTING.md)

## Contact

Hannes Datta

[https://hannesdatta.com]()



# Preview of efficient workflows

## A bird eye's view

- What is it about?
    - Build entire pipeline first
    - Then refine steps

- Good for
    - quick prototype
    - swapping/upgrading modules
    - focus on the "big" picture

::: notes

how i Use what I teach

:::

## Portability across computers, operating systems

- What is it about?
    - Prototype on Mac and Windows
    - Move to Linux Cloud

- Good for
    - performance issues
    - collaboration

## Branching out

- What is it about?
    - Take a "copy" of your project
    - Do changes there, test those without breaking the main project

- Good for
    - Testing
    - Robustness checks
    - Going back in time

## Time capsule

- What is it about?
    - Use version history on Git to view code (from the past)

- Good for
    - Because you *can*, you delete code and keep your project clean
    - Finding code that you want to use again
    - Search code *across* projects

## Software agility

- What is it about?
    - Use automation to connect different programs (e.g., R, Python, ...)
    - Use outputs of one as inputs of another

- Good for
    - Use a program what it's best for (e.g., R for data preparation, Python for ML)
    - Extreme flexibility

::: notes

show EC2

:::
