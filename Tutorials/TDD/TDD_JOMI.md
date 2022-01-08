➤ ☗ | ↓ ← → ↑ _ ‾ ∨ ∧ ¬ ⊗ ≡ ≤ ≥ ⌃ ⌄ ⊓⇅ ⊔⇵ ⊏ ⊐ ↱↳ ∑ -no unity ⤒ ⤓ ⌈ ⌊ 🀲 🀸 ⌛ ⏰ ▸ ▹ 🐁 🖱 💾
---------------------------------------



# Hello World

Launch the JOMI.JAR application on a computer.  
Use any tool that can send UDP message to its IP and Port address that JOMI.Jar display.  

- Be sure Java is install on the machine (often by default)
- Be sure that firewall are open on local network for the port you want to use.

`IP:127.0.0.1 Port:2501` by default.
Send: `sc: [[Hello World!]]`


# Communicate from OMI to JOMI
OMI is the Unity3D application that is the brain and JOMI is just the multiplaform executor.
I try to keep JOMI the more simple possible and the less buggy.

If you want to communicate you can use `jomiraw:` and `jomi:`

- `jomi:` Then the following text as a command to translate (a shortcut text)
  -  `jomi: a↓ a↑` Will press A and release
- `jomiraw:` Then the following text as a command to execute
  - `jomiraw:tms:500:ms:l` Will mouse click left button after 500 milliseconds
  - `jomiraw:sc: a↓ a↑` Will press A and release

**In resume:**
JOMI don't do all commands but is short and fast to write.
JOMIRAW do all commands but is precise, compressed and structured. 
Depending on the situation you need both of them.


# Time

When you trigger macro there is two main types.
The one that you don't care of the timing and the one that are precise.


**As soon as possible:**  

Execute thte command as soon as it received it in the order it received it.  
- `sc: [[Hello...]]`
- `sc: [[...World!]]`

If the package 'world' arrive a bit earlier that hello it will write '...World!Hello...'
_For most of the macro we don't really care._

**Good enough:**
Execute after n milliseconds the command starting at the reception.  
- `tms:1000:sc: [[Hello...]]`
- `tms:5000:sc: [[...World!]]`
If Hello 'arrive' at 16H30 01' and 'World' at 16H30 00' then there will be 3 seconds and not 4 seconds between the both.  
_Package take 1-20ms usually to arrive._  


**Precise:**
Execute the command at exactly the given time based on the computer time if time not passed yet.  
- `t:hour-minute-seconds-milliseconds:command`  

This `t` allows you to be precise on the execution of the command.
Manually that not the best but with some code that perfect to be sure the action(s) are executed at the right timing.
- `t:16-00-00-00:sc: [[Hello...]]`
- `t:16-00-10-00:sc: [[...World!]]`

Note:
- _"Java Robot" take some milliseconds to do some commands like writing text or use the clipboard._


# Shortcut

**Pressing and delay**  
- `sc: space↕` 
  - Press and release space with default minimum delay between both. 
- `sc: space↓ ⌛20 space↑` 
  - Will press space and release with 20 milliseconds between both. 
- `sc: space↓800` 
  - Will press for 800 milliseconds then release. 



**Delay**  
⌛20 vs 20> I used the ⌛ because it is more clear on what is will do.   
But you need to use it all the time everywhere. And it is more fast to just write `30>`.  
- `sc: space↓ ⌛20 space↑` 
  - will press space and release with 20 millisconds between both. 
- `sc: space↓ 20> space↑`
  - will press space and release with 20 millisconds between both. 
- `sc: ⌛200 200> space↓ 20> space↑`
  - will wait 400 milliseconds then press space and release with 20 millisconds between both. 

**Addition**
- `sc: shift+a` 
  - Is equal to `sc: shift↓ a↓ a↑ shift↑` 
  - Will press shift, stroke A and release shift
- `sc: shift+ctrl+a` 
  - Is equal to `sc: shift↓ ctrl↓ a↓ a↑ ctrl↑ shift↑` 
  - Will press shift then control, stroke A and release control then shift.
- `sc: a+b+c`
  - Will write 'abc' then release in 'cba' in order.

**Duplicator**

- `sc: ( A↕ )x3`
  - `sc: A↕ A↕ A↕ ` 
  - Will stroke 3 time 'A'
- `sc: ( A↕ ⌛2 ( B↕ ) x 4 400> )x3`
  - `sc: A↕ ⌛2 B↕ B↕ B↕ B↕  ⌛400 A↕ ⌛2 B↕ B↕ B↕ B↕ ⌛400 A↕ ⌛2 B↕ B↕ B↕ B↕`
  - Will stroke 3 time 'A' wait then "BBBB" then repeat 3 time with 400 ms delay 


**Screen**
↓ ← → ↑ 🐁 🖱 💾
-`sc: 🐁LeftClick 🐁RightClick 🐁MiddleClick` 
  - Will simulate leftclick of the mouse
-`sc: 🐁R  
  - Will simulate leftclick of the mouse
-`sc: 🐁A→10px↑10px` 
  - Will move the mouse at 10 px of  left and bot border.
-`sc: 🐁A→10↑0.1` 
  - Will move the mouse at 10 px of left and 10% of down border.
-`sc: 🐁A→10↑30→40→40` 
  - Will move the mouse at 40 px of left and 30px of down border.
-`sc: 🐁R→10↑30→40→40` 
  - Will move the mouse at 90 px of left and 30px of down border.
-`sc: 🐁→10%`  
  - Will move the mouse 10% of the screen to the right
- `sc: 🐁R→0.1`  
  - Will move the mouse 10% of the screen to the right
-`sc: 🐁→10` is equal to `sc: 🐁R→10` 
  - By defaul the `🐁→` is relative.
- `sc: 🐁R↓10px←10px`  
  - Will move the mouse 10 px to left and 10 px down
- `sc: 🐁A↓10px←10px`  
  - Will move the mouse in top right corner at 10 px of right border and 10 px of top borrder


_Note that every 🐁 will be replace by 🖱 in the jomi parser if you prefer 🖱._


_Not added yet:_
- `sc: 🐁l 🐁r 🐁m
  - Shot way to write mouse click left right middle. 
- `sc: 🐁0 🐁1 🐁4
  - Click on the additional mouse number (if java allow it) 
- `sc: 🐁LeftClick↓ 🐁RightClick↑ 🐁MiddleClick↕ 🐁r↑` 
  - Other way to write "LeftClick↓" to be more visual. 


**Screen save**
- `sc: 🐁>💾`
  - Will save the mouse position as pixel in memory. 
- `sc: 🐁<💾`
  - Will move the mouse at the pixel position in memory
- `sc: 🐁>💾Point1`
  - Will save the mouse position as pixel in memory as "Point1" Key id name.
- `sc: 🐁<💾Point1`
  - Will move the mouse at the pixel position named "point1" in memory
- `sc: 🐁>💾 10> 🐁A→0.5↑0.5` 10> 🐁LeftClick 10> 🐁<💾
  - Will save the mouse position the move it to center to click then come back to it previous position with a bit of delay between those actions. 
- `sc: 🐁>💾Point1` 
  - Then `sc: 🐁>💾Point2` 
  - Then `sc: ( 🐁<💾Point1 LeftClick↕ 80> 🐁<💾Point2 LeftClick↕  200> )x10 `   
  - This commands will save point1 and point2 that are positions on the screen and then will click on point1 then point2 with 280 milliseconds as interval for tens times.

**Screen cursor move**
I could implement a screen mouvement like the other software. But I am a bit against it.
I want the execution to be precise in time and managing the movement could delay the execution of commands of 1-3ms. You will find this functionnalty in OMI.
(Ping me if you really need this in JOMI.)
(Not counting the coding time that is up to 3-20 days to make it simple and robuste)

# Raw
## Keyboard
- ks: 
## Mouse

Pression  
- `ms:l` Strike Mouse button Left
- `ms:r` Strike mouse button Right
- `ms:m` Strike mouse button middle
- `mp:l` Press mouse button middle
- `mr:m` Release mouse button middle

Move  
- `mm:0.5p:0.6p` Move to 50% of screen left to right from border 
- `mm:0.5%:0.6%` Move to 50% of screen bot to top from border
- `mm:0.5px:0.5%` Move to 5 PX from screen border left at 50% of bot>top of the screen
- `ma:50px:100px` Move add relatively to current cursor at 50px right and 100px top
- `ma:-50px:-100px` Move add relatively to current cursor at 50px  left and 100px down
- `ma:.1%:10px` Move add relatively to current cursor at 10% to right and 10px top



----------------- 
To describe next:

- `wh:3` `wh:-3`
  - D

- `sc: copypast cut past copy `
  - D
- `sc: ctrl cmd ctrlcmd`
  - D
- `exit` `stop`
- `past: some text `
- `clipboard:copypast`
- `clipboard:copy`
- `clipboard:past`
- `clipboard:cut`
- `url:`
- `unicode:`
- `unicode:u+`
- `cmd:`
- `img2clip:`
- `ksc:cmd1裂cmd2裂cmd3`
  - D


- JavaKeyShortcut list


Could be usefull (not coded)

- `sc: 📋<url:`
- `sc: 📋<filepath:`
- `sc: 📋<` copy
- `sc: 📋>` past
- `sc: ✂` cut
- `sc: ☸up:3`
- `sc: ☸down:3`
- `sc: copypast↓ copypast↑` should be replace by  `sc: clipboard` ore remove

 ← → 
-----------
- ` `
- ` `
- ` `
- ` `
- ` `
- ` `
- ` `
- ` `
- ` `
- ` `
- ` `
- ` `
- ` `
- ` `
- ` `

Weirdo
- `sc: [[It is... Wait for it...]]⏰16H30 [[16h30]] ⌛4000 [[And everything is fine]]`
  - The following will write to wait. Then wait that it is 16h30 to write the time. Only then after 4 seconds it will say that "everything is fine"


# Password

The password is there for security reason.
If JOMI has as password set then every message must start witht the password.
**Example:**
> This section must be test and verified. Not used since long time
- password: YoLesFrites
- `YoLesFrites:tms:500:sc:[[Hello]]`  
If user don't send 'YoLesFrites', after 3 times the programme will close and send a error message to warn the user.  
The aim here is to protect that someon access the ip & port and use jomi to do shit.  
That not the perfect solution. But for now that all I have in JOMI.  

----------------

# .JOMIMacro In OMI

During some playthroughs, I realized that some action need 1-2ms precision.
So I create a .jomimacro file extension
```
☗callid actionName
☗description description of the action
30♦ms:l
45♦ms:l
73♦ms:l
433♦ms:l
```
It will transform them before sending them.
For example, if executed at 16h00 (0s 0mms).
```
sc:t:16-00-00-00:ms:l
sc:t:16-00-00-30:ms:l
sc:t:16-00-00-40:ms:l
sc:t:16-00-00-70:ms:l
sc:t:16-00-00-433:ms:l`
```
The idea hear is to avoid that the network make precision lost but keep the writing of the macro simple.


# WOMI
 _"Window Open Macro Input"_  
In the Unity OMI application there is a WOMI library that is less developped that "JOMI".
There reasons:
- Java Robot can execute only commands commun to all platform
- WOMI is more sure and fast that UDP sending to JOMI, but some application bug because you use the same "window hook". It happens to me on Apex Legends for example.
- Game that ban cheater has more tools to detect a program using Window native that Java Robot. Leading me to use WOMI if I need <2ms precision and JOMI if not.

Maybe one day I will create UnOMI, a version to execute under <1ms some commands from Arduino Micro.
And AOMI (not her...) AndroidOMI, that can simulate keystroke on Android with ADB.
