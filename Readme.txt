
My English not so good, i try write some info in English what i can, edit if using not correct word or write.

More informations and other free software, visit :
 http://budusoftware.blogspot.my
 If you wish to contribute, support me for better life.

BuduLearningTool Page :
 http://budusoftware.blogspot.my/2017/03/budu-learning-tools.html

BuduLearningTool.exe, Easy to open HelpFile.chm url by selected keyword from text editor
This script using menthod Copy,(send Ctrl+c) for get keyword
and get extentions current file from title bar text editor(current file path or name as title most text editor),

#> Support Script Langguage : redymade ChmUrlShortcut.au3t
1- Autoit3
2- AutoHotKey
3- Xyplorer

If want using For other HelpFile.chm, Extract url from Help.chm with 7z and find all keyword url in All .htm file
(many HelpFile.chm using keyword as .htm file name) and save in text file like .au3t, see sample format in BuduData Folder

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

#> Info And sample BuduLearningTool.ini Seting

[MainHChmData]
											   1 On/ Blank Off
SetKey=1							:  On/Off To using Keybord Shortcut
NextItems=1						:  On/Off Browsher Next Items
KeyClose={ESC}				:  Keybord Shortcut to exit, Change if needed
KeyFind={F6}					:  Keybord Shortcut to find, Change if needed
KeyNext={RIGHT}				:  Keybord Shortcut to browsher next, Change if needed
KeyStop={END}					:  Keybord Shortcut to stop browsher, Change if needed
ToolTip=1							:  On/Off Tooltip Info
TooltipPositionX=750  :  Tooltip Position from left

TotalItems=						:  Total HChmData? Data/Items
DefaultItems=					:  Default Number HChmData? Data/Items

[HChmData1]
HChmPath=							:  Path To Help.chm File, change to your correct path
hWnd=									:  Title Help.chm Windows, using autoit3 format regex
												 hWnd=REGEXPTITLE:Regular_Expresion_Windows_Title;
															REGEXPCLASS:HH Parent (Optional)
												 Or
												 hWnd=TITLE:Windows_Title;
														  CLASS:HH Parent  (Optional)

ChmUrlList=						:  Url list to Help.chm,
											   (to other langguage Extract from Help.chm with 7z and find all keyword url in All .htm file and save in text file like .au3t)
FileExt=							:  Extentions file to run like 'au3;' for autoit and 'xys;' for Xyplore, must last with ; separator
DefaultPage=					:  Default Url if missing or can't find selected keyword
RegexMatches=					:  Piority Regexmatches code, If blank can be using Default Regular Expression
											   Double ()  : can be replece with first seleted word/keyword
											   Double ;;  : Separator

See sample in BuduLearningTool.ini

File list and redy made :

C:\LearningTools\Learning Tools.exe
C:\LearningTools\ReadMe.txt
C:\LearningTools\_BuduData
C:\LearningTools\_BuduData\BuduLearnTool.ico
C:\LearningTools\_BuduData\BuduLearningTool.ini
C:\LearningTools\_BuduData\HHChmAutoHotKey.au3t
C:\LearningTools\_BuduData\HHChmAutoIt3.au3t
C:\LearningTools\_BuduData\HHChmXYplorer.au3t


#Note :

Changelog: Version : BuduLearningTool V2.0
1- Fix some regular expressions
2- Add funtions to using from Keybord Shortcut
3- Add funtions browsher to next page if morethan one macth keyword
4- Fix some and other............


#>> How To run BuduLearningTool.exe with Notepad++ using Argument Command from costum button

1- Open Notepad++, in menu go to : Run and click Run (or press F5 in keybord)

2- In Program to Run dialog box, paste argument like below in text box, click save

   "C:\YourPath\BuduLearningTool\BuduLearningTool.exe"

3- In Shortcut dialog box, Add name e.g : BuduLearningTool

4- press OK and exit/close Program to Run dialog box

5- now click to Run in menu, you can see BuduLearningTool in menu, click BuduLearningTool to make sure it work

#>> Add costum button.

6- Download CustomizeToolbar Notepad++ plugin at link bellow (for 32 bit)
   https://sourceforge.net/projects/npp-customize/?source=navbar

7- copy and paste CustomizeToolbar.dll to Notepad++ plugin folder,

8- Open Notepad++, in menu goto : Plugin > Customize Toolbar > and click Costum Button, restart Notepad++, and new button show in tollbar

9- goto Notepad++\plugin\Config folder and open CustomizeToolbar.btn with text editor
	 copy and paste button argument bellow in new line and save
	 (change iLeTool_16.bmp.bmp to your icon button or copy iLeTool_16.bmp in BuduData folder and paste in Notepad++\plugin\Config)

   Run,BuduLearningTool,,,iLeTool16.bmp

10- restart Notepad++, make sure it work like picture



Fell Free To Using And Edit

EdyYus

===============================================

#>> Below info about autoit3 simulated keystrokes code

'!'
This tells AutoIt to send an ALT keystroke, therefore Send("This is text!a") would send the keys "This is text" and then press "ALT+a".

N.B. Some programs are very choosy about capital letters and ALT keys, i.e., "!A" is different from "!a". The first says ALT+SHIFT+A, the second is ALT+a. If in doubt, use lowercase!

'+'
This tells AutoIt to send a SHIFT keystroke; therefore, Send("Hell+o") would send the text "HellO". Send("!+a") would send "ALT+SHIFT+a".

'^'
This tells AutoIt to send a CONTROL keystroke; therefore, Send("^!a") would send "CTRL+ALT+a".

N.B. Some programs are very choosy about capital letters and CTRL keys, i.e., "^A" is different from "^a". The first says CTRL+SHIFT+A, the second is CTRL+a. If in doubt, use lowercase!

'#'
The hash now sends a Windows keystroke; therefore, Send("#r") would send Win+r which launches the Run() dialog box.


Send() Command Resulting Keypress

{!} !
{#} #
{+} +
{^} ^
{{} {
{}} }
{SPACE} SPACE
{ENTER} ENTER key on the main keyboard
{ALT} ALT
{BACKSPACE} or {BS} BACKSPACE
{DELETE} or {DEL} DELETE
{UP} Up arrow
{DOWN} Down arrow
{LEFT} Left arrow
{RIGHT} Right arrow
{HOME} HOME
{END} END
{ESCAPE} or {ESC} ESCAPE
{INSERT} or {INS} INS
{PGUP} PageUp
{PGDN} PageDown
{F1} - {F12} Function keys
{TAB} TAB
{PRINTSCREEN} Print Screen key
{LWIN} Left Windows key
{RWIN} Right Windows key
{NUMLOCK on} NUMLOCK (on/off/toggle)
{CAPSLOCK off} CAPSLOCK (on/off/toggle)
{SCROLLLOCK toggle} SCROLLLOCK (on/off/toggle)
{BREAK} for Ctrl+Break processing
{PAUSE} PAUSE
{NUMPAD0} - {NUMPAD9} Numpad digits
{NUMPADMULT} Numpad Multiply
{NUMPADADD} Numpad Add
{NUMPADSUB} Numpad Subtract
{NUMPADDIV} Numpad Divide
{NUMPADDOT} Numpad period
{NUMPADENTER} Enter key on the numpad
{APPSKEY} Windows App key
{LALT} Left ALT key
{RALT} Right ALT key
{LCTRL} Left CTRL key
{RCTRL} Right CTRL key
{LSHIFT} Left Shift key
{RSHIFT} Right Shift key
{SLEEP} Computer SLEEP key
{ALTDOWN} Holds the ALT key down until {ALTUP} is sent
{SHIFTDOWN} Holds the SHIFT key down until {SHIFTUP} is sent
{CTRLDOWN} Holds the CTRL key down until {CTRLUP} is sent
{LWINDOWN} Holds the left Windows key down until {LWINUP} is sent
{RWINDOWN} Holds the right Windows key down until {RWINUP} is sent
{ASC nnnn} Send the ALT+nnnn key combination
{BROWSER_BACK} Select the browser "back" button
{BROWSER_FORWARD} Select the browser "forward" button
{BROWSER_REFRESH} Select the browser "refresh" button
{BROWSER_STOP} Select the browser "stop" button
{BROWSER_SEARCH} Select the browser "search" button
{BROWSER_FAVORITES} Select the browser "favorites" button
{BROWSER_HOME} Launch the browser and go to the home page
{VOLUME_MUTE} Mute the volume
{VOLUME_DOWN} Reduce the volume
{VOLUME_UP} Increase the volume
{MEDIA_NEXT} Select next track in media player
{MEDIA_PREV} Select previous track in media player
{MEDIA_STOP} Stop media player
{MEDIA_PLAY_PAUSE} Play/pause media player
{LAUNCH_MAIL} Launch the email application
{LAUNCH_MEDIA} Launch media player
{LAUNCH_APP1} Launch user app1
{LAUNCH_APP2} Launch user app2
{OEM_102} Either the angle bracket key or the backslash key on the RT 102-key keyboard
