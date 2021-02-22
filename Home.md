⌛ ➤ ☗ |  ↓ ↑

I am bad at documenting...
But "it is by forging that one becomes a blacksmith".
![image](https://user-images.githubusercontent.com/20149493/108693658-5f0af180-74fe-11eb-8316-79a332ea911f.png)
So if you need help, ping me on Discord:
https://eloistree.page.link/discord


------------------

Also.  
Before we start:  
![image](https://user-images.githubusercontent.com/20149493/108714894-6dff9d00-751a-11eb-873a-1b5ff3075286.png)
PS: I know what I want to create... But I have not idea of what it will look like in the future and what is the best shape for it. Meaning that the architecture of the software can be raw and seem quite random.
- If you think you can do better, feel free to give it a try. (Code(s) are Open Source) 
- If you think I can do better, feel free to talk with me.  (I am on [Discord](eloistree.page.link/discord))
- If you think my way of coding is shit, feel free to help me (It is my first big software)
- If you think my software is not good for professional use,... (o_O') Yes... obviously... it is unstable like 'shit' as it is in a research and development state. Thank captain obvious. 

------------------

------------------

Hello !!!  
Welcome to you.   

The idea of my tool is simple:
1. Play your game / be productive with your software
1. Create & Modify files in the folder 'configuration' of the application to tweak your wish and desire
2. The application detect modified files and load the new configuration.
3. Do that until your happy with your configuration.
4. Share your files with the community when you are proud of it.


----------------------------

# Basic you need to know
Before you start you need to understand:
- "Every situation can be resume in a 'true' or 'false' statement(s)"
  - So my programme is at 80% composed of tools to manage Boolean(true or false) only situation.
- Based on those named 1 and 0 you can make condition statement
  - Is the player jumping and firing ->  ````juming + firing ```
  - Is the player not running  and firing ->  ````!running + firing ```
  - Is the player is in game or in photoshop ->  ````!gamename + photoshop ```
- Those condition will help you to do two main actions
  - Create new named Boolean
    - juming + firing -> epicmoveincoming
    - !left + !right + !up + !down -> notmoving
  - Throw new request to do stuffs: "command line"
    - epicmoveincomming -> macro:startrecordingwithobs
    - notmoving -> macro:stoprecordingwithobs
- Those line(s) of text will do action based on the interpreter you have:
  - Macro interpreter: will try to do several actions when call
  - Mouse Utility interpreter: will try to simulate mouse click and move
  - Copy past interpreter: will copy past as text you stored previously
  - ...

So ... great but how do I configure that?
You just modify some files based on the tutorial in this wiki.

So let's overmatch all that.


## Boolean
In my application a Boolean value is a true or false state linked to a referential name. This is 80% of the application.

## Condition
Small text that ask the state of several Booleans state through the recent past time.

## Command line
One line of text that design something to do. It does know how to do it but it just request to do it. 

## Interpreter
Some codes of the application that a programmer added to the app for you that can understand some command line you can send. For the moment, the first interpreter that understand a command line claimed it and it responsible of executing it.

## Files configuration

Large range of files type that give the shape of how you want the software to assiste your in your daily life.
It only work for files in the configuration folder. An option will be add to import them from an/some URL in the future.

----------------------

# Files
## Used frequently
All the files in this list are regularly used in my everyday life testing.
Meaning they can have issue but they mainly works as intended and are good enought to be used.
|  File | Difficulty   |  What it does ?|
|---|---|---|
.keyboardtoboolean|*|Listen to keyboard in general.
.windowkeytoboolean|*|Listen to window keyboard specificly.
.winxboxtoboolean|*|Listen to Xbox Controller on Window.
.apptoboolean|*|Listen the focus of an application.
.boolstobool|*|Convert conditions to a boolean.
.filetobool|*|Defined boolean that need to exist and set them to a default value.
.morsecondition|**|Listen to a morse sequence to linked it to actions.
.stringtocommands|**|Create actions to be call based on a given name.
.timeofdaytocommands|**|Call action at specific moment of the day or frequence of the day.
.simplecondition|***|Link condition to actions to be call based on switch or maintaining.
.timecondition|***|Link condition to an action based on a range of time to be trigger.
.portnomenclature|***|Allow to listen to Arduino (or else) and convert them to boolean to be used.
.screenzonetoboolean|*|Allow to defined a screenzone and convert it as a boolean value when the mouse enter and exit the zone
.spliter.xml |**| Allows to convert a group of boolean to more booleans to make your avoid thinking about the logic behind a frequently used pattern.

## Complexe
The following files are technicly in my application but they are too hard to explain simply of how they work. If you are challagened enough, feel free to overwatch how to use them.

|  File | Difficulty   |  What it does ?|
|---|---|---|
.booleanregexcondition|***|Allow to trigger actions based on boolean change with Regex detection. Powerfull but very hard to use without knowedlge and training. 

## Check if finish
They are in the program... but I did not tested since a long time and I am not sure they are still working or finished

|  File | Difficulty   |  What it does ?|
|---|---|---|
.copypastfile|*|Allow to have some text that can be copy pasted on command.
.linearcondition|***|Allow to quickly associate an action based on a sequence of conditions
.jomimacro|***|Store some actions that need to be precisely executed with 1-10 milliseconds precision
.regextocommands|***|Give flexibility compare to 'stringtocommands' by using regex instead of string.


.audiointensity|***|Allow to convert the intencity of microphon (window) to a boolean value
.screenlocations
.stack
.timedcommandlines
.sequencedcommandlines
.relativetimedcommdlines
.wowfishingsetting
.reimportcommands

## Interpreter

https://github.com/EloiStree/OpenMacroInput/wiki/InterpretersOverview


------------------

.keyboardtoboolean
.apptoboolean
.boolstobool

Complexe
.booleanregexcondition
.copypastfile
.filetobool
.jomimacro
.keyboardtoboolean
.linearcondition
.morsecondition
.portnomenclature
.regextocommands
.screenzonetoboolean
.simplecondition
.stringtocommands

.timecondition

.timeofdaytocommands

.windowkeytoboolean
.winxboxtoboolean