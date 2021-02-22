If you want to do keyboard and mouse action without more complicate action.

You can send UDP message to the IP and port of the Jar of JOMI:
https://github.com/EloiStree/2020_04_10_JavaOpenMacroInputRuntime
```
// This command request to type some text in your game chat.
jomi: enter↓ ⌛20 enter↑ [[Some text to copy past]] enter↓ ⌛20 enter↑

//Make a double jump with some specific delay between the jump. 
jomi: jump↓ ⌛100 jump↑ ⌛200 jump↓ ⌛20 jump↑  

//Make a left click with the mouse
jomiraw:ms:l  

// start pressing the right button of the mouse
jomiraw:mp:r  

// release the right button of the mouse
jomiraw:mr:r  

// Move your mouse at 20% from left to right of the screen and 10% from top to bottom of the screen.
jomiraw:mm:0.2p:0.1p  

```


