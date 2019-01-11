
# Windows

## Anaconda

1. Press the windows key and type `add or remove programs`. Click on this option.
    * Another way of getting there is through Settings -> Apps -> Apps & features
2. In the search bar, type `python`. 
3. If nothing shows up, Anaconda is probably not installed. Point them to https://github.com/DHRI-Curriculum/install/
4. If one or more versions of Anaconda is installed, it will show up as something like "Python 3.7.0 (Anaconda3 5.3.1 64-bit). It will also show the date of the version. They should be good to go. 
3. Most anaconda versions should work with all the workshops. We haven't tested Python 2 versions, so if that is the version they have, in order to be on the safe side, I would ask them to get the newer Python 3 version. 
4. If they need a newer version, they should uninstall and then follow our install instructions on the website. Point them to https://github.com/DHRI-Curriculum/install
5. To uninstall, right there at the apps & features section, click on the program name, and a "Uninstall" button will appear. I suggest to uninstall all python versions you see there, and install a new one from scratch.

## Conda Path

1. If they followed the instructions to install python on https://github.com/DHRI-Curriculum/install , the path should be working. 
2. To test it, open the Command Prompt or Powershell and type `python`. If you see the three arrows, it is working! IF not, we have some things to do:
3. Get the python's and anaconda's paths:
    * Go to Anaconda Prompt
    * Type `where python` and enter
    * The result will be something like ```C:\Users\MyUserName\Anaconda\python.exe```
    * Now type `where conda` and Enter
    * The result will be something like ```C:\Users\MyUserName\Anaconda\Scripts\conda.exe```
4. Add the paths to the environment variables:
    * Type windows key and search for `environment`. Click on the option "Edit the system environment variables" (needs admin password)
    * Another way is pressing `windows + pause`. Click in "Advanced system settings -> Environment Variables
    * If none worked, try Settings -> System -> About -> System info (upper right corner) -> Advanced System settings -> Environment Variables
    * On the System Variables box (the bottom box, NOT the top one), select "PATH". Click on "Edit"
    *. Click on "New" and add one of the addresses of step 3 to the end of the list. Press enter. Click "New" again and add the other. ATTENTION:
    * When copying the paths from step 3, get everything but the executable command (the last part of the address).  In the example above, you would add ```C:\Users\MyUserName\Anaconda``` and ```C:\Users\MyUserName\Anaconda\Scripts```
5. Close the terminal. Go back to step 2 to test it.
6. If nothing works, the solution is to delete anaconda, and install it again (see Anaconda section above). Yikes!

## Git

1. Look for Git Bash (press windows key and type `git bash` or look for git folder on programs) If it is not there, Git has probably not been installed. 
2. To double check, open powershell or command prompt and type `git --version`. If the output is an error, git has not been installed.
3. If you need to install it, go to https://git-scm.com/download/win

## Git working with python

1. On Git Bash, type `python` and press Enter. If you see the three arrows, it is working!

2. If it goes to a blank line and nothing happens, then try to go back to the prompt (try Ctrl + Z then Enter; try `exit()` then Enter; if none works, just close the window)

3. We will need to create a file to have alias to the python executable. Just follow the steps:
1. To be sure that you are at the home directory, type `cd ~` and Enter.
1. Type `touch .bashrc` and Enter to create a hidden file.
1. Now we need to edit this file. Type `code .bashrc` and Enter. This should open the file on VS Code
1. On the first line of the file, type `alias python='winpty python.exe`
1. Save the file and close it.
    * If VS Code is not installed, try `nano .bashrc`. Ctrl + o and Enter saves; Crtl + x closes.
1. This should do the trick. You just need to restart the shell: close Git Bash and open it again.
1. Type `python` and Enter and see if it works.

## VS Code and path
If they followed the instructions, it should be working. If it is not working, there is a solution here: https://code.visualstudio.com/docs/setup/mac

## NLTK

1. Open the terminal and type `python` and Enter
2. Type `from nltk.book import text1` and Enter
2. Error message means nltk is not installed. In that case:
3. Go to the terminal and type `python` and Enter:
4. Once you see the three arrows, type `import nltk` and Enter
5. Than, type `nltk.download('all', halt_on_error=False)`
6. Go back to step 1 to test
 
## Pandas
1. Pandas should be installed since Anaconda brings it by default. 
1. To check, open the terminal and type `python` and Enter
2. Once you see the three arrows, type `import pandas`. 
3. If pandas is installed, the import will succeed and a new blank line will appear.
4. If there is an error message, Pandas might not be installed. In that case:
1. Exit python typing `exit()` and Enter
1. Type `conda install pandas -y` and Enter
1. Follow along with the installation.
1. Go back to steps 1 and 2 to check.

## Sklearn

1. To check, open the terminal and type `python` and Enter
2. Once you see the three arrows, type `import sklearn`. 
3. If sklearn is installed, the import will succeed and a new blank line will appear.
4. If there is an error message, sklearn might not be installed. In that case:
1. Exit python typing `exit()` and Enter
1. Type `conda install scikit-learn -y` and Enter
1. Follow along with the installation.
1. Go back to steps 1 and 2 to check.

## QGIS 

Try to launch it. That's pretty much it.

# MacOS

## Vs code and path
1. The vs code path does not work by default, but if they follow the instructions it should be working. 
1. To check that, open the terminal and type `code` and Enter. If the program opens, it is working. If there is an error, we need to add vs code to the path. Try the following:
2. Open VS Code
3. Navigate to View -> Command Pallet (Command + Shift + p also works)
4. Type `shell` into the text bar, and choose the option "Shell Command: Install 'code' command in PATH"
5. Close vs code and the terminal.
6. Go back to step 1 to check if it is working. 

## Git

1. Open the terminal and type `git --version`. If the output is an error, git has not been installed.
2. If it is not installed, type `xcode-select --install` and proceed with the install
3. Go back to step 1 to test it. 

## Anaconda

1. Open the terminal and type `conda --version`. If you get an error message, Anaconda is not installed.
2. If Anaconda is installed, you will get an output with the version. They should be good to go.
4. If by any reason they need to update, go to the Terminal and type `conda update -n root conda` and Enter. 
5. After that, type `conda update --all`.

## NLTK

1. Open the terminal and type `python` and Enter
2. Type `from nltk.book import text1` and Enter
3. Error message means nltk is not installed. In that case:
4. Go to the terminal and type `python` and Enter:
5. Once you see the three arrows, type `import nltk` and Enter
6. Than, type `nltk.download('all', halt_on_error=False)`
7. Go back to step 1 to test
 
## Pandas
1. Pandas should be installed since Anaconda brings it by default. 
1. To check, open the terminal and type `python` and Enter
2. Once you see the three arrows, type `import pandas`. 
3. If pandas is installed, the import will succeed and a new blank line will appear.
4. If there is an error message, Pandas might not be installed. In that case:
1. Exit python typing `exit()` and Enter
1. Type `conda install pandas -y` and Enter
1. Follow along with the installation.
1. Go back to steps 1 and 2 to check.

## Sklearn

1. To check, open the terminal and type `python` and Enter
2. Once you see the three arrows, type `import sklearn`. 
3. If sklearn is installed, the import will succeed and a new blank line will appear.
4. If there is an error message, sklearn might not be installed. In that case:
1. Exit python typing `exit()` and Enter
1. Type `conda install scikit-learn -y` and Enter
1. Follow along with the installation.
1. Go back to steps 1 and 2 to check.

## QGIS 

Try to launch it. That's pretty much it.

