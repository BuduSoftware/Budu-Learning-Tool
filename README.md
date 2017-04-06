# Budu-Learning-Tool
Easy to open HelpFile.chm url by selected program language keyword from most text editor


More informations and other free software, visit :
 http://budusoftware.blogspot.my
 
 If you wish to contribute, support me for better life.

BuduLearningTool Page :
 http://budusoftware.blogspot.my/2017/03/budu-learning-tools.html

BuduLearningTool.exe, Easy to open HelpFile.chm url by selected keyword from text editor
This script using menthod Copy,(send Ctrl+c) for get keyword
and get extentions current file from title bar text editor(current file path or name as title most text editor),

#> RedyMade Support Script Langguage : redymade ChmUrlShortcut.au3t
1- Autoit3
2- AutoHotKey
3- Xyplorer

If want using For other program language keyword Or other kewyword HelpFile.chm from text editor, Extract url from Help.chm with 7z and find all keyword url in All .htm file, (many HelpFile.chm using keyword as .htm file name) and save in text file like .au3t, see sample format in BuduData Folder

#> How to Using
Extract BuduLearningTool.7z, Change to your correct data in ini seting like file path and other

Using for costum toolbar button(some text editor allow to using costum button)
  1-Using Argument Command : "C:\YourPath\BuduLearningTool\BuduLearningTool.exe"
    If not recent using, recomended using as Argument Command, because not runing as background, single instan every click button
    For on Browsher NextItems, add 1 to On in BuduLearningTool.ini, e.g NextItems=1 and blank to SetKey e.g SetKey=
  2-Select keyword in text editor and press button

Or Using Keybord Shortcut(for other text editor), To using Keybord Shortcut,(Default On in seting ini)
  1-To On Keybord Shortcut, Open BuduLearningTool.ini, see at SetKey Key, add 1 to On, Or Remove to Off(using as run agrument from button)
  2-Run BuduLearningTool.exe
  3-Select keyword in text editor and press F6 to find, If Next funtions On and software get more than one result,
  tooltip show above next keyword url, Press RIGHT erro to browsher next items or Press END to stop browsher

Note : most text editor can Using with Keybord Shortcut

