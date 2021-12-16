Welcome to you on this tutorial about how to use OMI through the game League of Legends.  

You will be able to find the Ready to use example of this tutorial here:  
//Add Link.html  



At the end of this tutorials, you should be able to use the tool OMI in the version of 2021 December 15 with Xbox Controller , Keyboard and Midi Piano.

> The application is in development state.
> Sorry if it is a bit complexe at first.
> But the reward is huge.


## To use the tool you need to understand how it works on the paper

If I have to resume the application you will use in a step by step:
1. They are files where you fill your intent of what you want to do.
2. OMI check those file to understand what you want to do (Based on standard I am creating in the application for you).
3. It listens to what you asked him to listen and overwatch them for conditions you gave it.
4. If it found a condition you asked him. it will send a text to execute.
  - Example: If space and arrow is down and you are in League of Legend, go back to base and open the store after 8 seconds
  -  `space + arrowdown ♦ macro:lol:gobacktobase ♦ ☗TriggerOnTrue` in a `filename.simplecondition` file
  -  `lol:gobacktobase ♦ jomi:b↓ ⌛50 b↑ ⌛8000 i↓ ⌛50 i↑` in a `filename.stringtocommands` file
5. The text is sent to a `interpretor` that will try to understand it and convert it to code to execute.
  - The interpretor are code by me for the moment on what I think could be useful for the users
  - In future version, interpretor will be added as official and commmunity custom one.
6. If an interpretor understnad the text it will manage the code execution and it can send back some text to others interpretor.
  - For example:
     - The macro interpertor recognize `macro:********` and so send: "Hey guys this macro is called:"lol:gobacktobase". Do we have one like that. As you do it will send the text in the macro `jomi:b↓ ⌛50 b↑ ⌛8000 i↓ ⌛50 i↑`
     - The jomi interpretor recognize: `jomi:*****` and send: "Hey the application Java Open Macro Input, could you simulate this to the computer:`b↓ ⌛50 b↑ ⌛8000 i↓ ⌛50 i↑`".
     - The Java application  try to understand the text and execute it as: I press 'b' wait for 50 ms the release 'b' wait 8000ms then press i wait 50ms and release i.
7. What is the Java Open Macro Input (jomi) ? It is a small application that run on your computer that is portable and run on any platform that listen on the network for instruction of how to simulate keyboard and mouse. Meaning that you can for example use your phone to control your game (but that an other subject).




## Configure Sona With Midi

Ok let's learn by doing a basic example of how OMI work.  

### 1. Download the last build of OMI  
[![image](https://user-images.githubusercontent.com/20149493/146397675-b604fde6-3c78-407a-b9b1-a365e657cc6d.png)](https://openmacroinput.itch.io/openmacroinput)  
(https://openmacroinput.itch.io/openmacroinput)  
- 'OMI Last build' is the last stable build push on line.
- 'JOMI' is a portable executable that OMI use to do that keybaord and mouse action on your computer.

### 2. Let's listen to Midi
- You need to say to OMI that you will listen to MIDI entry in a `default.omi.xml`
``` xml
<omixml>
  <!-- Listen to a Midi board you can crafted with Arduino  -->
  <midiconnectionin midiName="Arduino Micro" />
  
  <!-- Listen to the MPK Mini Play (what I have) -->  
  <!-- https://www.amazon.fr/s?k=mpk+mini+play --> 
  <midiconnectionin midiName="MPK mini play" />
  
  <!-- If you want to play music while playing Sona -->
  <midiconnectionout midiName="Microsoft GS Wavetable Synth" />
  
</omixml>
```

Now want to can listen to Midi. You should be able to debug what you are listening to like this:  
![image](https://user-images.githubusercontent.com/20149493/146399730-351b6748-d535-43ca-a4e4-d7a4a5a8b1d4.png)  
![image](https://user-images.githubusercontent.com/20149493/146400522-cc910e14-9649-4ad0-8c8f-cbaf70d62e4d.png)  
So what next ?   
Push a button on the keyboard or a pad and observed what id or name it has.  
For example here: Name is C4 and id is 48 you can use either of them. And the velocity I apply when hit is about 50%.  

So you can write in a 'default.miditoboolean' file:  
```

MPK Mini Play♦CC♦64♦0.1♦1♦Sustain♦SetTrue

MPK Mini Play♦Note♦G4♦AdditionalPowerNote♦SetTrue
MPK Mini Play♦NoteVelocity♦G4♦0♦0♦AdditionalPowerNone♦SetTrue
MPK Mini Play♦NoteVelocity♦G4♦0.0001♦0.1♦AdditionalPowerLow♦SetTrue
MPK Mini Play♦NoteVelocity♦G4♦0.1♦0.9♦AdditionalPower♦SetTrue
MPK Mini Play♦NoteVelocity♦G4♦0.9♦1♦AdditionalPowerHight♦SetTrue


```


If like me you play 3 differents champion, note that you can switch the macro with a midi controller like this:  
![image](https://user-images.githubusercontent.com/20149493/146401133-2d3df79a-c2d3-4cb6-8168-fd3cf82db2eb.png)  

'default.miditoboolean'  
```
MPK Mini Play♦CC♦48♦0.0♦0.33♦ChoGath♦SetTrue
MPK Mini Play♦CC♦48♦0.33♦0.66♦Sona♦SetTrue
MPK Mini Play♦CC♦48♦0.66♦1♦Zoe♦SetTrue
```




