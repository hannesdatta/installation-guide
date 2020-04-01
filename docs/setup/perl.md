# Installing Perl

Perl is a proprietary statistical software frequently used by scientific users.
First check with your local IT support whether your institution has Stata licenses
available.


## Making Stata Available on the Command Prompt

You have just installed Stata. Later, we'd like to access Stata from the
command prompt to automatically execute our source code. That way, you will
be able to run a series of scripts in batch - which will significantly ease the burden of
building complex data workflows.

### Windows users
For you to be able to use Stata from the command prompt, follow the steps below.

!!! danger "Making Stata available via the PATH settings on Windows"
    We need to update our PATH settings; these settings are a set of directories that Windows uses to "look up" software to startup.

    - Right-click on Computer.
    - Go to "Properties" and select the tab "Advanced System settings".
    - Choose "Environment Variables" and select `Path` from the list of system variables.
    - Choose `Edit`.
    	- **Windows 7 and 8 machines:**
    		If you chose the default installation directory, copy and paste the following string without spaces at the start or end:
    
            `;c:\Program Files (x86)\Stata15`
    
    	  Using a different Stata version? Change the version number then in the path above.
    
    	- **Windows 10 machines:**
    		- Click `New` and paste the following string:
    
            `c:\Program Files (x86)\Stata15`
    
    		- Click on `OK` as often as needed.

### Mac users

For you to be able to use Stata from the command line, you have to add Stata to your bash file. A tutorial follows.

!!! danger "Making Stata available via the PATH settings on Mac"

```
Step 1: add Stata to bash file
- Open `Terminal`.
- Type `echo "export PATH=$PATH: Your Stata Path" >> ~/.bash_profile`. For example,
		`export PATH=$PATH: /Applications/Stata/StataMP.app/Contents/MacOS/  >> ~/.bash_profile`

Step 2: Evaluate bash changes
- Type `echo $PATH` to check whether Stata is added to your path.
```



<!--- Linux users not available yet
-->


## Verifying that the installation was successful

To verify that Stata has been correctly installed and configured via your PATH settings,
open a **new** terminal interface and enter:

```bash
StataSE-64.exe
```

followed by hitting the `Return` key. Stata will now start.
