# Reproducible Research with Make

Make is a tool that will allow us to control the execution of a set of command line statements.
We will use make to automate the execution of our research projects with a "single click" so that our entire work flow is reproducible.

## Installation Guide

### For Windows Users

We will install Make so that it plays nicely with your Anaconda/Python distribution and the Windows command line.

Please [download it here](http://gnuwin32.sourceforge.net/downlinks/make.php).

!!! danger "Making make available via the PATH settings on Windows"
    We need to update our PATH settings; these settings are a set of directories that Windows uses to "look up" software to startup. 

    - Right-click on Computer. 
	- Go to "Properties" and select the tab "Advanced System settings". 
	- Choose "Environment Variables" and select `Path` from the list of system variables.
	- Choose `Edit`.
		- **Windows 7 and 8 machines:**
			If you have used the default directory during your installation, copy and paste the following string without spaces at the start or end. Otherwise, modify the path accordingly:

            `;c:\Program Files (x86)\GnuWin32\bin\`

		- **Windows 10 machines:**
			- Click `New` and paste the following string:

            `c:\Program Files (x86)\GnuWin32\bin\`

			- Click on `OK` as often as needed.

<!---

within CygWin.
Its time to go back to the **setup-x86_64.exe** we [told you not to delete](commandLine.md). We will use it to install make.
Proceed as follows:

* Click through the installation until you arrive at the page "Select packages."
* Type make into the search function and wait for the results to be filtered.
* Click the '+' next to "Devel" and then find the following lines:
    * make
    * gcc-tools-epoch1-automake
    * gcc-tools-epoch2-automake
 and then click on the word 'Skip' located next to each of these. 'Skip' should then be replaced with some numbers (the version which we will install).
 * Now click on "Next" in the bottom right corner and continue accepting all options until the installation is complete.

-->

### For Mac Users

* Please install X-code command line tools, which includes *make*. 

Open a terminal by searching for it with spotlight, `cmd + spacebar` then type terminal and press `Return` when it appears. Then, copy and paste the following:

```bash
xcode-select --install
```

### For Linux Users

Make is pre-installed on Linux operating systems so there is nothing to be done.


## Verifying Your Installation

To check that Make is installed and working correctly, open a terminal session and type (then hit the return key):

```bash
make
```

If everything is working correctly, you should get the following output:

```bash
make: *** No targets specified or no makefile found. Stop.
```