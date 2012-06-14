ConkySoccerInterface
===================

What to do
----------
Place csi.py in this folder: ~/.conky 
You might need to create this folder first.

How to configure conky
----------------------
 * Edit ~/.conkyrc
 * Add some lines like these:
````${font size=11:italic}${color slate grey}Fußball EM 2012 ${hr}${color }${font }
${execi 60 python2 ~/.conky/csi.py}````
 * Notice: This way conky will call the script every 60 seconds

Known issues
------------
 * Sometimes conky will not show any results after running the script. Just wait for the next update in case.
 * Depending on your conky-configuration some letters might be truncated
