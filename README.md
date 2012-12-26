U.A.E Universal Amiga Emulator

This is based off 0.8.29 and is targetted for SDL/ARM/UNIX so it can run on the Blackberry phones and tablets.


Status: Runs ok with kickstart1.2 and A500 ECS mode.  Requires SDL joystick support in port 1 to play games
        So a seperate modification is being made to SDL12 library to support 'joystick'.  
        Wiimote pairing in BB10 works but TCO needs updating to handle screen event 14 'gamepad' processing
        So a bit of further work on joystick proceessing is required.
        
        Slowdowns and sound glitching is still present, something I need to work on.
        The default config file sets CPU mode to 68ec020/68882 and runs slow,  68020/68882 is the expected default.
        I've ran most CPU cores but the later kickstarts don't launch properly for some reason...