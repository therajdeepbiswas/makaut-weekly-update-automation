# makaut-weekly-update-automation

Download requirements -

1. Check your version of Google Chrome and accordingly download a driver from https://chromedriver.chromium.org/downloads
2. Place chromedriver.exe in the root directory


Excel sheets -

1. Put your excel sheets in the sheets/ directory and rename them to n.xlsx where n is the week number
2. Please make sure the first line (row) of your sheet DOES contain the header names (Semester, Subject, etc) and not just an empty row


Make the following changes to bot.py (I promise this is one time and all the manual work you'll have to do) -

1. Put in your username and password to the accordingly named string varibles
2. To the teachers variable, add the names of teachers in concern to the dictionary from teachers.txt; key: "name as per excel sheet", value: "name as per portal"
I have fetched all teacher names from the portal into the txt file for your convenience; the spacing is very irregular and I wouldn't recommmend you guess and type or even follow the examples I have given (they are just for reference)
Note: I haven't experimented whether "&" works or "&amp;" does, (no one such in BCA), if you get errors, do interchange (currently, everyone is "&")
3. To the subjects variable, Add the names of the subjects in concern in a similar key value pair as above; the "subject code" should be the index of the dropdown menu option of the portal
Also consider every variation that existed in your excel sheets for example, in my case, "Advanced Networking and Communication" and "Networking" refer to the same subject
4. To the semesters variable, add your concerned semester(s).
For professors: If you want all semesters' data, either add all your semesters to the variable or just change: bot.py line 47 'continue' to 'pass'
Note: it's a good idea to keep both string and integer possibilities since I haven't taken the time to browse through all of the excel sheets (the entire point of automation) making sure they are consistent