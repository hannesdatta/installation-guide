# Why Build Tools?

Imagine you have built a complex project, consisting of dozens of datafiles and scripts. 
Also imagine you haven't worked on the project for a few weeks, and now wish to continue
your work where you left off.

The big questions then become: 

- In which order do the files need to be executed?
- Which files are up-to-date and do not have to be executed again?

For this purpose, we use a *workflow management system* - or, in technical terms - "build tool".
Build tools will allow us to control the execution of a set scripts by by running them from the command line.

We will use *make* to automate the execution of our projects with a "single click" so that our entire work flow is reproducible.

!!! tip "Why a Tool to Manage Project's Execution?"
    We strongly believe in using build tools to manage the execution of a research project - and we hope that by the end of your project, you will do, too.

    Some reasons we push this topic are:

    * Your workflow / order of execution is explicitly documented.
    * Each time you run *make*, it only executes each script if the output is expected to be different from the last time your ran it. That is, it runs 'partial builds.'
    * If multiple users work on the project, they can easily execute code that others have written.

<!--    #* Its written in Python, which minimizes the learning curve needed to pick up the essentials relatively small
#    #* It was designed for academic/professional research (in Bioformatics) so it feels more intuitive than most alternatives for our desired audience.
--!>