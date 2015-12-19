# ConkySoccerInterface


# What to do
Place csi.py in this folder: ~/.conky 
You might need to create this folder first.

# Dependencies
 * For the SOAP client: python-suds or python2-suds (depending on your distribution)

# Configuration
## General

 * Edit ~/.conkyrc
 * Add some lines like these:

```
${font size=11:italic}${color slate grey}Fußball EM 2012 ${hr}${color }${font }
${texeci 60 python ~/.conky/csi.py}
```
 * If you use a distribution with Python3 as default, you need to replace 'python' with 'python2' in the command above
 * Notice: This way conky will call the script every 60 seconds
 * If the file was empty before, do not forget to add the `TEXT` line to tell config and content apart:

```

 
TEXT
${font size=11:italic}${color slate grey}My league ${hr}${color }${font } ${texeci 60 python ~/.conky/csi.py}
```
 
## Configure leagues
* Visit "openligadb" and search for your league.
* There should be an "info" column with the following fields:
    * Liga-Id: 848
    * Liga-Shortcut: bl1
    * Saison: 2015
* Edit `csi.py`
* Change `LEAGUE_NAME`, `LEAGUE_SAISON` and `LEAGUE_ID` corresponding to the values of your league


# Isssues
 * Sometimes conky will not show any results after running the script. Just wait for the next update in case.
 * Depending on your conky-configuration some letters might be truncated
