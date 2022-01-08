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
- `tms:hour-minute-seconds-milliseconds:command`  

This `tms` allows you to be precise on the execution of the command.
Manually that not the best but with some code that perfect to be sure the action(s) are executed at the right timing.
- `tms:16-00-00-00:sc: [[Hello...]]`
- `tms:16-00-10-00:sc: [[...World!]]`

Note:
- _"Java Robot" take some milliseconds to do some commands like writing text or use the clipboard._


# Shortcut

## Pressing and delay
- `sc: space↕` 
  - Press and release space with default minimum delay between both. 
- `sc: space↓ ⌛20 space↑` 
  - Will press space and release with 20 milliseconds between both. 
- `sc: space↓800` 
  - Will press for 800 milliseconds then release. 




⌛20 vs 20> I used the ⌛ because it is more clear on what is will do.   
But you need to use it all the time everywhere. And it is more fast to just write `30>`.  
- `sc: space↓ ⌛20 space↑` 
  - will press space and release with 20 millisconds between both. 
- `sc: space↓ 20> space↑`
  - will press space and release with 20 millisconds between both. 

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
