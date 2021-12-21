Share this tutorial: https://openmacroinput.page.link/helloworld


----------------------

## Solution of the tutorial

If you just want the solution of the tutorial.   
Feel free to download this zip or to use Git.  

Download example as a ZIP:  
https://github.com/EloiStree/OpenMacroInputConfigExamples/archive/refs/heads/HelloWorldOMI.zip

Download example as a git clone:
``` git
git clone -n https://github.com/EloiStree/OpenMacroInputConfigExamples.git .
git checkout fec391ca182920628e4a69d343c586089647929d
```

------------------------

**The good old hello world.**



### Download OMI  

First download [Open Macro Input](https://openmacroinput.page.link/download)   
![image](https://user-images.githubusercontent.com/20149493/146833460-c19475c2-cf00-4c21-a656-6860fe09dd5a.png)  

### Launch the "Open Macro Input.exe" && the "JOMI.jar"  

 ![image](https://user-images.githubusercontent.com/20149493/146833674-d02c710c-7aa4-4650-ba96-19f010e62cac.png)  

### Listen to the keyboard touch "Page Down"  

`helloworld.keyboardtoboolean`  
```
//Listen to PageDown as a named boolean 'RequestHelloWorldKey'
PageDown♦RequestHelloWorld
```

### Associate the action to write "Hello World to the change of PageDown 

`helloworld.simplecondition`
```
//Write Hello World and press enter before and after when value is 'RequestHelloWorldKey' is true
RequestHelloWorldKey  ♦ jomi:enter↓ ⌛10 enter↑ [[Hello World !]] enter↓ ⌛10 enter↑ ♦ ☗TriggerOnTrue

//Trigger when value become true
RequestHelloWorldKeyLoop  ♦ jomi:[[Hey !!!]] enter↓ ⌛250 enter↑ ♦ ☗TriggerOnTrue
//Trigger action every 500 ms when value is true
RequestHelloWorldKeyLoop  ♦ jomi:[[Hello...]] enter↓ ⌛250 enter↑ ♦ ☗LoopOnTrue 500
//Trigger when value become false
RequestHelloWorldKeyLoop  ♦ jomi:[[...World!]] enter↓ ⌛250 enter↑ ♦ ☗TriggerOnFalse
```

### Be sure that JOMI is launch and active  

![image](https://user-images.githubusercontent.com/20149493/146835094-afe18322-d8a3-4008-8d90-380bbe30fe3e.png)    
JOMI stand for Java Open Macro Input. It is a small java application. Meaning that it runs on most platform.  
It don't facilitate the tasks for new user of OMI but it us very useful to control several computers or do remote controllers.  
OMI is heavy but JOMI is just a light application to run on the side.  

### Communicate between OMI and JOMI  

![image](https://user-images.githubusercontent.com/20149493/146836557-7a178264-8bd2-4cc0-8351-2d52c99ff5d5.png)  
It is a bit geeky but... Both program need to communicated.   
Here we target our current computer, so you need to set the current ip or 127.0.0.1. the two application need the same port.  
(I will code a better version in future but it is like that in current version).   

### Enjoy your "Hello World"  

If you set up everything right.  
Now if you press page down and page up, it should write "Hello World" And "Hey !!! Hello... Hello... Hello... Hello... World !"  
![image](https://user-images.githubusercontent.com/20149493/146840008-71b3167c-3684-40c1-af8c-5ffd9dbbb1f1.png)


### Make a contextual "Hello World"  

The problem of Macro (action(s) triggered) is that you don't want them to happen in the wrong application.
So let's listen to some and apply different behaviour to them.

`helloworld.apptoboolean`
```
// Create a named boolean called arduino if the focus application has ' Arduiono ' in it.
arduino♦ Arduino 
//Save form visual studio.
visualstudio♦- Microsoft Visual Studio
//If you are a bit geeky you can use Regex in here: https://regexr.com/
notepad♦- [Nn]otepad
//  \+ is because you are using regexr so if you don't want to play with it keep is Alpha numerical A-z0-9
notepadplus♦- [Nn]otepad\+\+
```

Set the condition using the new named booleans creted from focus context.
`helloworld.simplecondition`
```
// Code specific to visual studio for C# in Unity
visualstudio + RequestHelloWorldKey  ♦ jomi: [[Debug.Log("Hello World!");]] enter↓ ⌛10 enter↑ ♦ ☗TriggerOnTrue

// Code specific to Arduino for C++ 
arduino + RequestHelloWorldKey  ♦ jomi: [[Serial.println("Hello World");]] enter↓ ⌛10 enter↑ ♦ ☗TriggerOnTrue

// Code specific to notepad but as the name are close we want the notepad that is not notpad++ for text
notepad + !notepadplus + RequestHelloWorldKey  ♦ jomi:[[Hello World !]] enter↓ ⌛10 enter↑ ♦ ☗TriggerOnTrue

// And we want the notepad++ to behave like HTML text as context.
notepad + notepadplus + RequestHelloWorldKey  ♦ jomi:[[<div>Hello World</div>]] enter↓ ⌛10 enter↑ ♦ ☗TriggerOnTrue

// "//" Is for commenting a line. Meaning that it won't be take in consideration.
// So we comment the old version to not remote it yet in case we need it.
//
//Write Hello World and press enter before and after when value is 'RequestHelloWorldKey' is true
//RequestHelloWorldKey  ♦ jomi:enter↓ ⌛10 enter↑ [[Hello World !]] enter↓ ⌛10 enter↑ ♦ ☗TriggerOnTrue
//Trigger when value become true
//RequestHelloWorldKeyLoop  ♦ jomi:[[Hey !!!]] enter↓ ⌛250 enter↑ ♦ ☗TriggerOnTrue
//Trigger action every 500 ms when value is true
//RequestHelloWorldKeyLoop  ♦ jomi:[[Hello...]] enter↓ ⌛250 enter↑ ♦ ☗LoopOnTrue 500
//Trigger when value become false
//RequestHelloWorldKeyLoop  ♦ jomi:[[...World!]] enter↓ ⌛250 enter↑ ♦ ☗TriggerOnFalse

```

If you set up everything correctly. The text that is writen should be now contextualized.



