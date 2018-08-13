# Defcon 26 Badge info (from a totes n00b)

## About the badge
    * the silver defcon logo on the bottom left of the badge is a `d-pad`
    * the two silver circles on the bottom right of the badge are `+/-` buttons

## Connecting to the badge
* plug micro USB into computer
* look for device in `/dev/`
    * look for a `/dev/tty*` file that looks fishy (ex: `/dev/tty.usbmodemFD121`)
* screen into it (ex `screen /dev/tty.usbmodemFD121`)
    * when you do this you'll see a maze that you can control with the defcon logo in the bottom right (it's a `d-pad` 😺)
* to disconnect run  (`ctrl + a`) then release and hit `d`
    * NOTE: when you do this, if you run `screen /dev/tty.usbmodemFD121` you'll get the following error `Sorry, could not find a PTY.`
        * to fix just unplug your badge and plug it a back in then run `screen /dev/tty.usbmodemFD121` again and you should see the maze \o/

## The maze
    * the blinking cursor in the maze is controlled by the `d-pad` on the badge
### arcade room
    * text: 
        ```
        You're in an arcade room screaming of the 80s. Good games, good times!
        A poster says "0x2BFC8E2B3561C04FBBC73FA43D5D96540D0AA008B30924CE47DA0EC67530D3"
        ```
    * testing:
        * I think this might be a hex dealio, so I did some stuffs in node based on what the googles told me to do to parse
            ```
            > var thing = '0x2BFC8E2B3561C04FBBC73FA43D5D96540D0AA008B30924CE47DA0EC67530D3'
            undefined
            > var bytestring = Number(thing).toString(10);
            undefined
            > bytestring
            '7.771749672767704e+73'
            > parseInt(bytestring, 2).toString(16);
            'NaN'
            > parseInt(bytestring, 2)
            NaN
            > bytestring
            '7.771749672767704e+73'
            > Number(bytestring)
            7.771749672767704e+73
            > parseInt(Number(bytestring), 2)
            NaN
            > var numbs = Number(bytestring)
            undefined
            > typeof(numbs)
            'number'
            > parseInt(numbs)
            7
            > parseInt(numbs, 2)
            NaN
            ```
### ????? room
    * text: 
        ```
        A monolithic humanoid robot towers with cables fanning from its back!
        A paper tape is draped into the machine: "0xFEED B0B0 DEAD BEEF".
        ```
