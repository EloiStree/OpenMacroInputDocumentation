 ➤ ☗ | ↓ ↑ _ ‾ ∨ ∧ ¬ ⊗ ≡ ≤ ≥ ⌃ ⌄ ⊓⇅ ⊔⇵ ⊏ ⊐ ↱↳ ∑ -no unity ⤒ ⤓ ⌈ ⌊ 🀲 🀸 ⌛ ⏰
 
Demonstration tutorial by example of JOMI


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
