# R and RStudio

R is a language for statistical computing and graphics.
R's use in the data science, econometrics and marketing communities has taken off over recent years and (at a bare minimum) should be considered as an open source replacement to Stata and SPSS.

## Installing R

Go to the [R homepage](https://cran.r-project.org/) and download the installer for your operating system.

The current version for Mac and Windows is `R version 3.6.1` and for Linux it is `R version 3.4.1`

We strongly suggest you to install R in the directory `C:\R\R-3.x.x\` rather than the default directory, `C:\Program Files\R\R-3.x.x\`.

## Installing RStudio

RStudio provides an easy to work with interface to R, and its format should feel familiar to other software environments like Stata or SPSS.

Download and install the free version of RStudio for your operating system from [here](https://www.rstudio.com/products/rstudio/download3/).

## Verifying your Installation of R

Open RStudio from the start menu. After starting up, you should see the version corresponding to the one chosen on the website.

![Screenshot of R Studio](r.png)


## Installing Additional R Packages

We will need some additional libraries to conduct our statistical analysis. Proceed as follows:

*   Please open RStudio (if not already opened in the previous step)
*   In the **console**, copy and paste the following:
```r
packages <- c("reshape", "rmarkdown",
              "data.table", "Hmisc", "dplr",
                    "stargazer", "knitr",
                    "xtable","tidyverse", 
                    "RSQLite", "dbplyr")

install.packages(packages)
```

* If you are asked if you want to install packages that need compilation, type `y` followed by `Return` to confirm this.
*   Wait until all the packages have been installed and the you are done.
    *   It *may* take a while, so be patient

## Making R Available on the Command Prompt

You have just installed R and RStudio, and learnt how to open RStudio from the start menu.
However, for many of the applications that follow, you are required to access R directly from the command prompt.
For example, this will enable you to run a series of R scripts in batch - which will significantly ease the burden of 
building complex data workflows.

For you to be able to use R from the command prompt, **Windows users** need to follow the steps below.
On Mac and Linux, R is available from the command line by default.

!!! danger "Making R available via the PATH settings on Windows"
    We need to update our PATH settings; these settings are a set of directories that Windows uses to "look up" software to startup. 

    - Right-click on Computer. 
	- Go to "Properties" and select the tab "Advanced System settings". 
	- Choose "Environment Variables" and select `Path` from the list of system variables.
	- Choose `Edit`.
		- **Windows 7 and 8 machines:**
			If you chose your installation directory to be C:\R\R-3.6.1\ during your installation (i.e., you did not use the default directory), copy and paste the following string without spaces at the start or end:

            `;C:\R\R-3.6.1\bin`

		- **Windows 10 machines:**
			- Click `New` and paste the following string:

            `C:\R\R-3.6.1\bin`

			- Click on `OK` as often as needed.

    !!! tip
        You will need to add a new PATH for most of the following installation steps. Always keep in mind that after you add a new PATH, you need to start a *new* cygwin/terminal session to verify whether it worked. Sometimes it may take a couple of minutes until your PATH is recognized by the terminal. 

**Now let's verify whether we can open R from the command prompt**

Open the command prompt/terminal and enter:

```bash
R --version
```

followed by pressing `Return`. The expected return begins with:

```bash
R version 3.x.x (201x-xx-xx) -- "Some Funky Name"
```

Great job - you've managed to install R and configure it for use for data-intensive projects!