
## About the badge
    * furry with scrolly!!!1 \o/

## Connecting to the badge
* plug micro USB into computer
* look for device in `/dev/`
    * look for a `/dev/tty*` file that looks fishy (ex: `/dev/tty.usbmodemFD121`)
* screen into it (ex `screen /dev/tty.usbmodemFD121`)
    * when you do this you'll see a maze that you can control with the defcon logo in the bottom right (it's a `d-pad` 😺)
* to disconnect run  (`ctrl + a`) then release and hit `d`
    * NOTE: when you do this, if you run `screen /dev/tty.usbmodemFD121` you'll get the following error `Sorry, could not find a PTY.`
        * to fix just unplug your badge and plug it a back in then run `screen /dev/tty.usbmodemFD121` again and you should see the maze \o/
ctrl - d soft reset

## Using the badge
* connect to badge and see `Booting` string
    * use `ctrl - c` to start python comand propt
    * use `ctrl - d` soft reset and see your changes
    * `dcfurs.clear()`
    * `dcfurs.set_pixel(1, 1, 255)`
    * nose is `boop()` in `emote.py` (has hex stuffs you need to like mirror)
