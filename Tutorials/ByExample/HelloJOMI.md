Welcome to you 🤗.

If you see this page, it means that you want to learn about how to use JOMI.
Or that you launch JOMI.jar for the first time 

Bravo 🙌 

So let's start, this tutorial.


**In short: What is JOMI?**  
Java Open Macro Input is a light version of the projet OMI.  
The `JOMI.jar` only receive basic command(s) through the network (with UDP) and execute them when it reveices them.

Example:
- `url:http//google.com` will open google in your default browser.
- `ms:l` will make a left click of your mouse (=`mouse stroke: left`)
- `mm:0.75:0.9` will move the mouse at right down of your screen (=`mouse move at: 70% left right : 90% top down`)
- `ks:a` will press and release the letter `a` (=`keyboard stroke: touch 'a'`)

**Is it important for you to know it ?**
It depends of what your plan with JOMI: 
- If it you want to use it from OMI (future version) or from a third party application: `no`
- If you just want to use OMI: `no` but at least you need to know how to launch it.
- If you want to do crazy macro yourself without having to start an application from zero: `yes`
- If you plan to master your computer with OMI: `yes`
- ...

But for this tutorial, I won't speak about OMI anymore: Just JOMI.

# In very short without explication

You don't have time and you like to learn by yourself ?

1. [Download `JOMI`](http://openmacroinput.com/download)
2. Launch it once then launch `StartJOMI.bat`
3. Send UDP message on the IP and port display on the console. 
4. Don't close it until you are done.
5. See the [GitHub code](https://github.com/EloiStree/2020_04_10_JavaOpenMacroInputRuntime) for the manual or the end of this tutorial to lean the commmands
6. _Enjoy and don't forget to suppor the projet or send me a beer if you like the app._


# In Long with details

## Download & Launch JOMI

If not already done:
1. [Download `JOMI`](http://openmacroinput.com/download)
2. No pay-wall, you can skip the donation to download `JOMI.Jar`
3. Launch `JOMI.jar` the first time
4. Launch `StartJOMI.bat`
5. Enjoy 🙂.

_(Geek note: after the first launch. `JOMI.jar` will execute in 'hidden mode' if you need. You can use `StopJOMI.bat` to stop it)_


**What do you means enjoy ?**
I means. It is running and ready to listen to your orders.  
Until you close the console (the black window).  

But now he you need to send him command(s), like:   
`tms:5000:sc: enter↓ enter↑ [[Hello world !!]] enter↓ enter↑`  
That will write your first `Hello World` after 5 seconds.  

Or `t:17-30-0-0:url:https://www.youtube.com/watch?v=G1IbRujko-A`
That will launch 10H Gand Alf Sax at 17h30 (if you don't close the app until then).


So let's learn how to do that.  

## Send command(s) to JOMI

To send message to the application you can use "what ever you want".    
It just need to send small message on the network that we call UDP message  
_(To a target computer that is running JOMI and that is not block by the 'firewall' on the port used)_  
  
The application I am using on Window is:  
Packet Sender: https://packetsender.com/download#show  
[![image](https://user-images.githubusercontent.com/20149493/147727453-623c00b9-7c75-436c-9123-a6835c742db3.png)](https://packetsender.com/download#show  )

If you prefer on Android, you have a hundred of application:  
[Google play search: UDP Sender](https://play.google.com/store/search?q=send%20udp&c=apps)  
I will use this one:[UDP Sender / Receiver](https://play.google.com/store/apps/details?id=com.jca.udpsendreceive)  
[![image](https://user-images.githubusercontent.com/20149493/147727474-37e702d1-5b2d-409b-b9e1-968b596e94f1.png)](https://play.google.com/store/apps/details?id=com.jca.udpsendreceive)

_Note that you can do you own application like I did here:   
[JOMI Demo on Android Store](https://play.google.com/store/apps/details?id=be.eloistree.jomi)
[![image](https://user-images.githubusercontent.com/20149493/147727572-17dba9b6-9c3b-4064-9b13-cc5b1411cb9a.png)](https://play.google.com/store/apps/details?id=be.eloistree.jomi)


By default the port is 2501 and the IP is the one of your computer.  
![image](https://user-images.githubusercontent.com/20149493/147727361-b4293de8-e59f-49b2-8d10-c811adbeee4a.png)  
(`127.0.0.1` as IP should work in most of the case if you don't know what to use)

If you followed the previous step you should have the `ip` and the `port` here:
![image](https://user-images.githubusercontent.com/20149493/147723572-9d24242d-ab6f-47bf-87f2-96f038806275.png)
At least if you are on the version of 2021-12-30, or near.


### For UDP Sender (Window)
0. Downloaded and install.
_(I let's you do that. Classic download next > next > next > launch)_
1. Check that JOMI is well open
2. Enter the IP in the address field: `127.0.0.1`
3. Enter the port in the port field: `2501`
4. Enter the following line in the ASCII Field: `tms:3000:url:https://youtu.be/dQw4w9WgXcQ`
6. Press `send`  

![image](https://user-images.githubusercontent.com/20149493/147727836-cc49c4ec-d8e6-43d0-861e-ea75bd837c7e.png)

And "Ta-Da" you have open your first web page with JOMI.  
If you want to do the 'Hello World' classic example, you can use the following line(s):
`sc: enter↓ enter↑ [[Hello world !!]] enter↓ enter↑`




### For the junior developer: Python example
1. Download Python: https://www.python.org/downloads/
2. Create a file `HelloWorld.py`
3. Be sure that JOMI is running.
4. Launch the file with this command: `python HelloWorld.py`

File: `HelloWorld.py`
```
import socket
UDP_IP = "127.0.0.1"
UDP_PORT = 2501
MESSAGE = "tms:5000:sc: enter↓ enter↑ [[Hello world !!!]] enter↓ enter↑"
print("UDP target IP: %s" % UDP_IP)
print("UDP target port: %s" % UDP_PORT)
print("message: %s" % MESSAGE)
sock = socket.socket(socket.AF_INET, socket.SOCK_DGRAM)
sock.sendto(MESSAGE.encode(), (UDP_IP, UDP_PORT))
```




**Unicode you will use:**  
↓ ↑ ⇅ ⇵ ⌛ ⏰

 
Demonstration tutorial by example of JOMI



PS:https://onlineasciitools.com/convert-unicode-to-ascii  
//in 4000 milliseconds, could you write 'Hello...' then wait that it is 1h13 and 20 seconds to write 'you'  
tms:4000:sc:[[Hello...]]  ⏰1h13:20  [[You]]  
//Same but with ASCII code instead of Unity for UDP Package Sender  
tms:4000:sc:[[Hello...]]  \e2\8f\b01h13:20  [[You]]  

// Press two time on left arrow  
tms:4000:sc:left⇵ left⇵  
tms:4000:sc:left\e2\87\b5 left\e2\87\b5   


Demo of JOMI and Android:
- Download: https://play.google.com/store/apps/details?id=be.eloistree.jomi
- Video: add it here


Java is a language that communicate with your computer.
The advantage:
- Is that it runs on almost all computer.
The disadvantage:
- It need to be install (by default or by the user)
- It can only do action that are generic and not native.

For example he can simulate keyboard and mouse move but can't use the key mail or or calculatrice of your keyboard as it is specific of Window.


## Why OMI is code in C# and Unity and JOMI in Java ?

The final goal of my project is to have OMI on Oculus Quest, Hololens and future VR AR Glass.
So it needs to works on Unity 3D.

But as you can't run Unity on Raspberry and all platforms I need it to be verstatil. At least on the execution part.
That why JOMI was created. JOMI execute instruction and OMI think and listen to native part of the device it runs on.

In future version of the projet they will be a boolean network that will allows intercommunication between devices and applications.



What can you do with JOMI

shortcut: jomi: ↓ ↑ ⤒ ⤓ ⇵ ⇅  ⌛ ⏰


How do you do to play so badly Patate ?

Go uninstall you fag Legend23

Jesus Chris, what the fuck are you doing Leroy ?

Do you like to get fucked Legend23 ?


How do you do to play so badly Leroy ?



![image](https://user-images.githubusercontent.com/20149493/147372700-35740892-f01d-4c6c-886c-1021e041ebdd.png)
- UDP : https://packetsender.com/download#show
- Unicode dico: https://unicode-table.com/en/sets/symbols-for-steam/



Example of use:
- cmd:start %appdata%/..  // send a window command as launch bat   
- cmd:shutdown /s /t 1800"  // shutdown the computer in 1800 seconds 
- "tms:"   // time as milliseconds
- t:{0}-{1}-{2}-{3}:cmd  hh:mm seconds, milliseconds
- ksc:  A↕ | B↕ | C↕"
- "img2clip:"+ url
- sc: Ctrl↓ V↕ Ctrl↑"
- clipboard:[cut,past,copy,copypast,cutpast]  // Do a clipboard action
- past: past some following text
- sc:  ...  // send a shortcut text
- empl:{0}裂{1}   // Per line embrace
- em:{0}裂{1}"   // Per text embrace
- uni:U+{0}   // Unicode hexa code
- unicode:U+
- uni:{0} // unicode index int
- unicode:{0}
- url:{0} // default browser to open at url
- rep:{0}裂{1}  // to replace 0 by in the clipboard
- up↕
- 2↓ 2↑ RightClick↓  RightClick↑ 
- Ctrl+0 
- Ctrl+A ⌛10 Backspace↓ ⌛200 Backspace↑  [[Elysian Thade ]] ⌛100 Enter↓ Enter↑ 
- VK_END↓ VK_END↑
- ms:l
- mm:0.206%:0.14% || mm:0.5p:0.3p
- ma:0.206%:0.14%
- ks:a
- kp:a 
- kr:a
- ms:[0,1,2] [l,r,m]
- wh:[wheel:int]
- mm:[x:int px]:[y:int px]
- ma:[x:int px]:[y:int px]
- mm:[x:int %]:[y:int %]
- ma:[x:int p]:[y:int p]
- ct:[text]

Not in the code but will be later:
- Backspace⇵   == Backspace↓ Backspace↑
- Backspace⇅  == Backspace↑ Backspace↓
- A↓600  == A↓ ⌛600 A↑
- A↑600  == A↑ ⌛600 A↓
- A↓ A↑ ⏰16H30 Enter↓ Enter↑ B↑ ⌛600 B↓ = Press 'a' then wait that it is 16h30 to continue and press 'enter' follow by B ofr 600 ms
- ⏰Flush == Flush all the waiting time to execute
- ⌛Flush == Flush all the in queue commands
- Flush == Flush all the temporary memory in waiting.
- 🖱move:lrdt:0.5:0.7 = move mouse at 50% of left to right and 70% of down to top of the screen.
- 🖱left:lrdt:50:60 = left click at 50pixel from left to right and 60 from bot to top
- 🖱go:lrdt:0.5:0.7 = move mouse at 50% of left to right and 70% of down to top of the screen.
- 🖱left:lrdt:50:60 = left click at 50pixel from left to right and 60 from bot to top
- 🖱middle:lrdt:50:60 = left click at 50pixel from left to right and 60 from bot to top
- 🖱right:lrdt:50:60 = left click at 50pixel from left to right and 60 from bot to top


When you use OMI, you canuse jomi or jomiraw
- jomiraw: You want to send a command and you know how to write it
- jomi: You want to send a command but you use a short compress version


### Password

I am not a expert in security. But I wanted to give a minimu of protection in the application.
You can define a password to be used with JOMI. If someone push 3 times the wrong password. JOMI is block and you need to relaunch it.
Contact me for tutorial on that subject of if you want to help me protect the software with better solution.


### File Configuration

The following list is all the key that can be stroke by Java and so by JOMI  
`AllStrokableKeys.txt`
```
VK_ENTER 
VK_BACK_SPACE
VK_TAB
VK_CANCEL
VK_CLEAR
VK_SHIFT
VK_CONTROL
VK_ALT
VK_PAUSE
VK_CAPS_LOCK
VK_ESCAPE
VK_SPACE
VK_PAGE_UP
VK_PAGE_DOWN
VK_END
VK_HOME
VK_LEFT
VK_UP
VK_RIGHT
VK_DOWN
VK_KP_UP
VK_KP_DOWN
VK_KP_LEFT
VK_KP_RIGHT
VK_COMMA
VK_MINUS
VK_PERIOD
VK_SLASH
VK_0
VK_1
VK_2
VK_3
VK_4
VK_5
VK_6
VK_7
VK_8
VK_9
VK_SEMICOLON
VK_EQUALS
VK_A
VK_B
VK_C
VK_D
VK_E
VK_F
VK_G
VK_H
VK_I
VK_J
VK_K
VK_L
VK_M
VK_N
VK_O
VK_P
VK_Q
VK_R
VK_S
VK_T
VK_U
VK_V
VK_W
VK_X
VK_Y
VK_Z
VK_OPEN_BRACKET
VK_BACK_SLASH
VK_CLOSE_BRACKET
VK_NUMPAD0
VK_NUMPAD1
VK_NUMPAD2
VK_NUMPAD3
VK_NUMPAD4
VK_NUMPAD5
VK_NUMPAD6
VK_NUMPAD7
VK_NUMPAD8
VK_NUMPAD9
VK_MULTIPLY
VK_ADD
VK_SEPARATOR
VK_SUBTRACT
VK_DECIMAL
VK_DIVIDE
VK_DELETE
VK_NUM_LOCK
VK_SCROLL_LOCK
VK_F1
VK_F2
VK_F3
VK_F4
VK_F5
VK_F6
VK_F7
VK_F8
VK_F9
VK_F10
VK_F11
VK_F12
VK_F13
VK_F14
VK_F15
VK_F16
VK_F17
VK_F18
VK_F19
VK_F20
VK_F21
VK_F22
VK_F23
VK_F24
VK_PRINTSCREEN
VK_INSERT
VK_HELP
VK_META
VK_BACK_QUOTE
VK_QUOTE
VK_DEAD_GRAVE
VK_DEAD_ACUTE
VK_DEAD_CIRCUMFLEX
VK_DEAD_TILDE
VK_DEAD_MACRON
VK_DEAD_BREVE
VK_DEAD_ABOVEDOT
VK_DEAD_DIAERESIS
VK_DEAD_ABOVERING
VK_DEAD_DOUBLEACUTE
VK_DEAD_CARON
VK_DEAD_CEDILLA
VK_DEAD_OGONEK
VK_DEAD_IOTA
VK_DEAD_VOICED_SOUND
VK_DEAD_SEMIVOICED_SOUND
VK_AMPERSAND
VK_ASTERISK
VK_QUOTEDBL
VK_LESS
VK_GREATER
VK_BRACELEFT
VK_BRACERIGHT
VK_AT
VK_COLON
VK_CIRCUMFLEX
VK_DOLLAR
VK_EURO_SIGN
VK_EXCLAMATION_MARK
VK_INVERTED_EXCLAMATION_MARK
VK_LEFT_PARENTHESIS
VK_NUMBER_SIGN
VK_PLUS
VK_RIGHT_PARENTHESIS
VK_UNDERSCORE
VK_WINDOWS
VK_CONTEXT_MENU
VK_FINAL
VK_CONVERT
VK_NONCONVERT
VK_ACCEPT
VK_MODECHANGE
VK_ALPHANUMERIC
VK_FULL_WIDTH
VK_HALF_WIDTH
VK_CODE_INPUT
VK_INPUT_METHOD_ON_OFF
VK_CUT
VK_COPY
VK_PASTE
VK_UNDO
VK_AGAIN
VK_FIND
VK_PROPS
VK_STOP
VK_COMPOSE
VK_ALT_GRAPH
VK_BEGIN
VK_UNDEFINED
KEY_LOCATION_UNKNOWN
KEY_LOCATION_STANDARD
KEY_LOCATION_LEFT
KEY_LOCATION_RIGHT
KEY_LOCATION_NUMPAD
```


As remembering VK_NUMPAD0 is less easy that NP0
The following file near the Jar allows to add shortcut ot it.

For example if you want to use Zero PadZero to type zero from OMI.
You can do it like this 

`KeyShortcut.txt`
```
VK_NUMPAD0: PadZero
VK_0: Zero
```

`KeyShortcut.txt`
```
VK_NUMPAD0: NP0
VK_NUMPAD0: NP0
VK_NUMPAD1: NP1
VK_NUMPAD2: NP2
VK_NUMPAD3: NP3
VK_NUMPAD4: NP4
VK_NUMPAD5: NP5
VK_NUMPAD6: NP6
VK_NUMPAD7: NP7
VK_NUMPAD8: NP8
VK_NUMPAD9: NP9
VK_0: 0
VK_1: 1
VK_2: 2
VK_3: 3
VK_4: 4
VK_5: 5
VK_6: 6
VK_7: 7
VK_8: 8
VK_9: 9
VK_PLUS: +
VK_MINUS: -
VK_MULTIPLY: *
VK_DIVIDE: /
VK_KP_DOWN: .
VK_UP: Up
VK_LEFT: Left
VK_RIGHT: Right
VK_DOWN: Down
VK_SPACE: Space
VK_CONTROL: Ctrl
VK_ALT: Alt
VK_ALT_GRAPH: AltGr
VK_SHIFT: Shift
VK_CAPS_LOCK: ShiftLock
VK_TAB: Tab
VK_ESCAPE: Escape
VK_DELETE: Del
VK_DELETE: Delete
VK_ENTER: Enter
VK_BACK_SPACE: BackSpace
VK_WINDOWS: Window
VK_A: A
VK_B: B
VK_C: C
VK_D: D
VK_E: E
VK_F: F
VK_G: G
VK_H: H
VK_I: I
VK_J: J
VK_K: K
VK_L: L
VK_M: M
VK_N: N
VK_O: O
VK_P: P
VK_Q: Q
VK_R: R
VK_S: S
VK_T: T
VK_U: U
VK_V: V
VK_W: W
VK_X: X
VK_Y: Y
VK_Z: Z
VK_F1:   F1
VK_F2:   F2
VK_F3:   F3
VK_F4:   F4
VK_F5:   F5
VK_F6:   F6
VK_F7:   F7
VK_F8:   F8
VK_F9:   F9
VK_F10: F10
VK_F11: F11
VK_F12: F12
VK_INSERT   : Insert
VK_HOME     : Home
VK_PAGE_DOWN: PageDown
VK_PAGE_UP  : PageUp
VK_PAUSE    : Pause
VK_NUM_LOCK : NumLock	
```
