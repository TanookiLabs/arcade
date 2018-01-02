## Using the Tanooki Retro Arcade
We hope you're having fun with your Tanooki Retro Arcade! If you haven't gotten yours up and running yet, setup is easy.
- Plug in the controllers
- Plug in the HDMI and turn on the TV
- Select the correct video input on your TV
- THEN plug in the PI

## Full Documentation
- Your Tanooki Retro Arcade is built on RetroPie, full documentation for that awesome project is here: https://retropie.org.uk/docs/

## Advanced Manuevers
- The "Select" hotkey lets you do all sorts of fun stuff when used in combination with other keys.  
- **Select + Right-Shoulder** will create a "save state" of exactly where you are in the game. 
- **Select + Left-Shoulder** reloads that save state. Handy for beating tough sections of a game!
- **Select + Right/Left** will change which "save state slot" you're using. You can create multiple save states! 
- I sometimes save crucial moments in both Save State Slot 0 and 1 in case I accidentally save over state 0. 

## Wifi & SSH Access
- You can configure wifi by plugging in a keyboard and then going into the RetroPie menu. 
- To connect, ssh into the new IP address of your device
   - **Username:** pi
   - **Password:** tanookipi
   - example ssh pi@retropie.localdomain
   - once your pi is on your network, it will generally be available at the hostname retropie or retropie.localdomain
- Your pi is running a flavor of Debian linux called Raspian
- Want to avoid entering your password all the time? Copy your public key to your pi
```
ssh-copy-id pi@retropie.localdomain
```

## Adding more Games (roms) 
- So you're really into this thing and want to add some more games? Awesome! You can load up everything from Atari, Amiga, C64, and more. BUT, many computer based systems are a bit harder to get to work easily with joystick only and will require keyboard and mouse as well, which is why I left them out of the default build. 
- There are a number of ways to add roms to your system. In general, Simply drop the files in the ~/RetroPie/roms/$CONSOLE folder, where $CONSOLE is the name of the target console, e.g. snes or arcade and they'll appear after a restart.
  - Samba Share: Your pi should appear as a network share called RetroPie once you've connected to Wifi. 
  - SSH/SCP: copy files via the commandline with scp filename pi@retropie.localdomain:~/RetroPie/roms/$CONSOLE where $CONSOLE is the name of the target console

## Troubleshooting: What to do when something went wrong!
- Have you tried turning it off and on again ;)
- If your controller gets misconfigured, hit Start -> Configure input and go through the setup process again. Just hold any button to skip the controls you down have on that controller. 

## Shutting down the retro arcade
- The best way to shut down your arcade is to hit start, then go to "shutdown" on the menu. Once it's off, you can unplug it. 
- If you're in a hurry, you can just unplug it, but that has a small possibility of corrupting your SD card. If that happen, we can rewrite it, but it's a small pain (16gb download and writing the SD card)

## What's "ScummVM" ?
- Scumm as the scripting language that LucasArts created their games in, and covers everything from Maniac Mansion and Day of the Tentacle up through Monkey Island, Full Throttle, Sam and Max and more. These were some of the best games for PC in the 90s, and they're funny, challenging, and smart.
- You'll need a keyboard and mouse to play these games!
- Hit F5 to bring up a system menu which will let you change options and exit the game if needed
- You may need to hold a button on the joystick or mouse to trigger additional options in the game (Full Throttle has many options in a "wheel" once you hold the button. 

## Bluetooth Controllers
- Is your controller cable a bit too short? RetroPie works with a variety of remote controllers, but they can be a bit tricky to set up. 
### EASIEST SOLUTION:
- XBox 360 controllers with the USB receiver work out of the box. Just plug in the receiver via USB and pair the controllers to it. 
### Best bluetooth controller
- 8bitdo makes amazing retro-styled bluetooth controllers with decent support. Their newest entry is apparently the best:
- https://www.amazon.com/dp/B0748S1VDC?th=1
- Setting up a bluetooth controller can be a bit of a dance, you'll need to use the RetroPie Setup menu, pick the device from the list, and then set it up to auto-connect at startup. Once you get it working after a reboot it tends to stay working, but your mileage may vary
