# Reproducible Science Checklist

There is quite some material to cover to make sure your work becomes
reproducible and is well-structured.

Here's a checklist you can fill in to see how well you are
adhering to the suggestions put forward in this guide.

!!! warning
	This checklist is **work-in-progress**, still incomplete,
	and not perfectly aligned with other sections on this website.
	Use at your own risk!


|                                                                         | data-prepation | analysis    | paper       | ...     |
| ------------------------------------------------------------------------|:--------------:|:-----------:|:-----------:|:-------:|
| **Main documentation**
| Readme with project description and technical instruction how to run/build the project
| Authentication credentials stored outside of the repository (e.g., in a JSON file), NOT clear-text in source code
|
| **Documentation at the sub-module level**
| *Documentation*                           
| Readme with explanation what module does + running instructions | &#9744;        | &#9744;     | &#9744;     | &#9744; |    |
| Documenting output files (e.g., if your code is generating a dataset which is different (e.g., new variables) from the raw data, then it is helpful to include a readme with variable operationalization for that data) | &#9744;        | &#9744;     | &#9744;     | &#9744; |    |
| Production of audit files (e.g., statistics, tables, or figures to check data quality/model convergence) | &#9744;        | &#9744;     | &#9744;     | &#9744; |    |
| *File/directory structure*
| Have five subdirectories: code/input/output/temp and audit)  | &#9744;        | &#9744;     | &#9744;     | &#9744; |    |
| All file names are relative, and not absolute (i.e., never refer to C:\mydata\myproject, but only use relative paths, e.g., ../output) | &#9744;        | &#9744;     | &#9744;     | &#9744; |    |
| *Automation*
| Have a Makefile in each module | &#9744;        | &#9744;     | &#9744;     | &#9744; |    |
| Makefile available at the root of the project (tying together individual makefiles) | &#9744;        | &#9744;     | &#9744;     | &#9744; |    |
| Dependencies between source code and files that will be built made explicit, so that make automatically recognizes when a rule does not need to be run? | &#9744;        | &#9744;     | &#9744;     | &#9744; |    |
| Creation of directory structure in code, or use of .gitkeep | &#9744;        | &#9744;     | &#9744;     | &#9744; |    |
| Include function to delete temp, output files, and audit files in makefile | &#9744;        | &#9744;     | &#9744;     | &#9744; |    |
| *Versioning*
| All files versioned (i.e., added to Git/GitHub) that need to be versioned (typically all source code)? | &#9744;        | &#9744;     | &#9744;     | &#9744; |    |
| All files not versioned (i.e., NOT added to Git/GitHub) that need not to be versioned (e.g., everything that is *generated* by your code, such as downloaded input files, temp files, auditing files, or the final output of a module)? | &#9744;        | &#9744;     | &#9744;     | &#9744; |    |
| Use of .gitignore for files/directories that need not to be versioned | &#9744;        | &#9744;     | &#9744;     | &#9744; |    |
| *Housekeeping*
| "Clean" and accessible variable names | &#9744;        | &#9744;     | &#9744;     | &#9744; |    |
| Loop what can be looped | &#9744;        | &#9744;     | &#9744;     | &#9744; |    |
| Use of subprograms/functions rather than one giant script | &#9744;        | &#9744;     | &#9744;     | &#9744; |    |
| Delete what can be deleted (including unnecessary comments, legacy calls to packages/libraries, variables) | &#9744;        | &#9744;     | &#9744;     | &#9744; |    |
| Use of asserts (i.e., make your program crash if it encounters an error which is not recognized as an error)| &#9744;        | &#9744;     | &#9744;     | &#9744; |    |
| *Testing for portability*
| Tested on own computer (wiped temp/input/output/audit) | &#9744;        | &#9744;     | &#9744;     | &#9744; |    |
| Tested on own computer (cloned to different directory) | &#9744;        | &#9744;     | &#9744;     | &#9744; |    |
| Tested on different computer (Windows) | &#9744;        | &#9744;     | &#9744;     | &#9744; |    |
| Tested on different computer (Mac) | &#9744;        | &#9744;     | &#9744;     | &#9744; |    |
| Tested on different computer (Linux) | &#9744;        | &#9744;     | &#9744;     | &#9744; |    |
