<!-- saved from url=(0053) https://kacos2000.github.io/Win10-Research/JumpList/ --> 

# [Windows 10 - *(Search)* Jumplist Parser](https://github.com/kacos2000/Win10-Research/blob/master/JumpList/Jumplist.ps1) #


PowerShell script that reads the contents the location:<br>
*'HKCU -> Software\Microsoft\Windows\CurrentVersion\Search\JumplistData'*<br> from a precollected (*not live*) **NTUser.dat** file. 

**Note:** *must be run in a PowerShell console with Administrator privileges.*

Starts by allowing user to select NTUser.dat file:

![File selection](https://raw.githubusercontent.com/kacos2000/Win10-Research/master/JumpList/select.JPG)

Calculates the SHA256 hash of the *NTUSer.dat* hive file and opens it (*Read Only*). The results are shown in a popup window with Filestamp in user localtime.
User can select all lines (Ctrl+A) or specific lines (Ctrl+click) and copy/paste (Ctrl+C and Ctrl+V) the data to a text file or MS Excel spreadsheet. The Selected lines are also displayed in the console after the user presses the OK button.

![Jumplist data](https://raw.githubusercontent.com/kacos2000/Win10-Research/master/JumpList/results.JPG)

After the result window is closed *(user presses the OK button)*, a new SHA256 hash of the *NTUSer.dat* hive is calculated and checked against the original:

![Hash Check](https://raw.githubusercontent.com/kacos2000/Win10-Research/master/JumpList/HashCheck.JPG)
