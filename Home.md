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
1. You modify files in the folder 'configuration'.
2. When saved my application detect modified files and load the new configuration.
3. Do that until your happy with your configuration.
4. Later: Share the files to the community when you love your configuration.

Now it means that each file has a way to be written. 
This wiki is here to give you the "grammar" of it and examples. 

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

## Condition

## Command line

## Interpreter

## Files configuration

----------------------

# Files
## Full list
|  File | What it does  |  
|---|---|
|  .spliter.xml | It convert a group of boolean to more booleans to make your avoid thinking about the logic of it based on the context you give them.  |  


# Command Line


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