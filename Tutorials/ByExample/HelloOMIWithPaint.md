

One way to request OMI to press a zone of the screen is to use JOMI
If you send a network message on JOMI like this on `ms:l`:
you are requesting a **m**ouse  '**s**trike: left button'  
And the `jomiraw` means: "Could you send that to the JOMI through udp on the network as I exactly write it `ms:l`

`paint.stringtocommmands`
```
// Note that jomiraw use the java orientation by default, left to right and top to bottom
paint:useselection ♦jomiraw:mm:0.0773%:0.05%♦jomiraw:ms:l
```



`paint.screenlocations`
```
Center♦rlbt♦0.5♦0.5
CornerBotLeft♦0.01♦0.01
CornerTopRight♦1.0♦1.0
CenterScreenZone♦0.3♦0.3♦0.7♦0.7
MainScreen♦0.01♦0.01♦0.99♦0.99
```
In 1000|mouseutility:click:CornerBotLeft

In 1000|mouseutility:leftclick:lrbt:0.5:0.5  
mouseutility:click:CornerBotLeft  
mouseutility:leftclick:lrbt:0.5:0.5  
mouseutility:rightclick:lrbt:0.5:0.5  
mouseutility:moveto:lrbt:0.5:0.5  


mouseutility:click:lrbt:pct:pct  
mouseutility:click:nameofpoint  
mouseutility:click:lrbt:pct:pct  
mouseutility:moveto:lrbt:pct:pct  
mouseutility:moveto:nameofpoint  
mouseutility:randomclick:nameofzone  
mouseutility:randommoveto:nameofzone  
mouseutility:gridleftclick:nameofzone:counthorizontal:countvertical:timebetweeninMs  
mouseutility:gridrightclick:nameofzone:counthorizontal:countvertical:timebetweeninMs  
//
            if (action == "gridclick" || action == "gridrightclick" || action == "gridleftclick" || action == "gridmove")




Now that you know that you can target a screen position and move or click.
It is boring to comeback each time where we were before we moved the mouse.

So we will use the in `screenrec:save:mymouse` & in `1000|screenrec:recover:mymouse` command.


