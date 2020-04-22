# Installing Lyx

Lyx is an open source document processor based on the LaTeX. [Download Lyx](https://www.lyx.org/Download).

## Making Lyx Available on the Command Prompt

You have just installed Lyx and may need to access Lyx from the command line. 

### Windows users
For you to be able to use Lyx from the command prompt, follow the steps below.

!!! danger "Making Lyx available via the PATH settings on Windows"
    We need to update our PATH settings; these settings are a set of directories that Windows uses to "look up" software to startup.

    - Right-click on Computer.
    - Go to "Properties" and select the tab "Advanced System settings".
    - Choose "Environment Variables" and select `Path` from the list of system variables.
    - Choose `Edit`.
    	- Environment variable name: LYX_BIN
    	- **Windows 7 and 8 machines:**
    		If you chose the default installation directory, copy and paste the following string without spaces at the start or end:
    
            `c:\Program Files (x86)\Lyx`
    
    	- **Windows 10 machines:**
    		- Click `New` and paste the following string:
    
            `c:\Program Files (x86)\Lyx`
    
    		- Click on `OK` as often as needed.

### Mac users

For you to be able to use Lyx from the command line, you have to add Lyx to your environmental variables. A tutorial follows.	

!!! danger "Making Lyx available via the PATH settings on Mac" 

	- open Terminal
	- type `vi ~/.bash_profile`
	- add Lyx to the environmental varibles
	  	- type `i` to input mode of vim
	  	- add `export LYX_BIN=/Applications/LyX.app/Contents/MacOS/lyx`. 
	  	- press `esc` and type `:w` to save the change
	  	- close the ternimal and reopen one terminal. Then type `source ~/.bash_profile` to bring the new .bash_profile into effect.
	- type `$LYX_BIN` to check availability. Remember to type the `$` before `LYX_BIN`. 


<!--- Linux users not available yet
-->


## Verifying that the installation was successful

To verify that Lyx has been correctly installed and configured via your PATH settings,
open a **new** terminal interface and enter:

```bash
$LYX_BIN
```

followed by hitting the `Return` key. 
