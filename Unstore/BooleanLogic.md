

```
    "[AND left up right]", //All forward
            "[AND left up right down]", // All down
            "[AND left down right]", // all backward
            "[OR left up right down]", // IsMoving
            "[AND left up right down]", // IsMoving
            "[XOR left right]", // One is down but not the other
            "[NAND left right]", // All but not both true
            "[NOR left right]", // Non are used
            "[NXOR left right]", // Are both equal false false or true true
            "[XOR up down]", // One is down but not the other
            "[XEQ up down]", // equivalent all are true
            "[NXEQ up down]", // equivalent all are false
            "[â left right]",//One of them must be true
            "[â left right up top]",//One of them must be true
            "[& left right]",
            "[| left right]",
            "[| left right]",
            "[â¡ left right]", // equivalent all true or all false
            "[left right ð²  up ]", // left and right are false and up is true
            "[up down ð¸ left right]", // up and down are true. Left and right are false.
            //INVERSE
            "Â¬up",
            "!left",

            //SEPARATOR and PRIORITY
            "(left | right) && (up | down)", // Diagonal
            "(left â¨ right) â§ (up â¨ down)", // Diagonal
            "(left or right) and (up or down)", // Diagonal
            "(left or right) and (up or down)", // Diagonal

            "left < right",// true if left is false and right true
            "up > down", // true if left is true and right false
            
            //Or and Priority
            "left || right |||| up + down ++ up",
            "(left | (right | up) ) + (down + up)",
            

            //Or and Priority upper then 3-4
            // + ++ +++ ++++ +5 +8 +12
            // - -- --- ---- -5 -8 -12
            // â ââ âââ â5 â8 â12
            // â¡ â¡ â¡ â¡5 â¡8 â¡12
            "left 4| right ++ up + down 5+ up",
            "((( (left | right) + up )  + (down + up))",
        
            //ITEM
            "shiftâ200",// pressed since 200ms
            "shiftâ200",// released since 200ms
            "shiftâ200", //switch true since 200ms
            "shiftâ200",//switch false since 200ms
            "shiftâ200:400",// maintaining true between 200ms and 400ms
            "shiftâ200:400",// pressed since 200 ms
            "shiftâ1.453s",//switch false since 1453ms
            "shiftâ1.5m",//switch false since 1m 30 seconds
            "shiftâ¾200", //was false there is 200ms
            "shift_200",//Was true there is 200ms
            "shiftâ¾â°12h45m30s456",//was false at 12 h 45m 30s 456 millisecond base on DateTime.Now
            "shift_â°14:20:30",//Was true at 14 h 20m 30s base on DateTime.Now
            "shift_â°14:20",//Was true at 14 h 20m  base on DateTime.Now
            
            "[ ]",
            "[ ]",
            ""
```
