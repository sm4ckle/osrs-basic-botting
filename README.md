# osrs-basic-botting
A few python scripts for simple botting in OSRS. I would recommend running these on a virtual machine so they can run in the background while you do other things.

# Miner.py

This script is set to mine iron ore from the Al Kharid mine, then once your inventory is full, it paths back to the Al Kharid bank to deposit, and then paths back and repeats. Fully functional, but you __might__ run into some bugs. At some point, I'll add a video tutorial for setup and configuration.

You can find a video of the script in action here: https://www.youtube.com/watch?v=p-4p_eerk34&ab_channel=spackle

To use this, you'll need the following RuneLite plugins - Object Markers, Ground Markers, Status Socket, Shortest Path, Camera Points


Object Markers is used to mark the bank and ore, Ground Markers is used to mark out the path, Camera Points is used to setup the camera for each stage, Shortest Path is used initially to help with marking out the most efficient tile path, and Status Socket is a plugin that sends info to a local server, and is used to update the current tile. You'll need to run server.py to collect that info.


1. Use Object Markers to mark the following:

  Ore - Pure Pink = (Red - 255, Green - 0, Blue - 255)

  Bank - Pure Red = (Red - 255, Green - 0, Blue - 0)

  Also, in the Object Markers settings, select Highlight Clickbox only, and set Border Width to 3.


2. Next, you'll need to use Ground Markers to mark out your path:

  For the settings, set color to Pure Blue = (Red - 0, Green - 0, Blue - 255), set Border Width to 5, Fill Opacity to 100, and check Draw Tiles On Minimap.

  You can use Shortest Path to find the most efficient pathing. For this script, simply stand next to the Al Kharid bank stall, open the world map, right click where   the iron ore is, and click Set Target. You'll see a red line leading you to the tile you selected, simply mark the starting tile, then follow the path marking tiles about every 10 tiles or so (just need to have every next tile viewable from the minimap). Once your path is set, you're good to go!


3. For Camera Points, set it up like the following image:

![Camera Points](https://user-images.githubusercontent.com/31822308/233782849-cd761bf8-b480-47a8-8bc8-d4a5ab447f1b.PNG)

Also, make sure you do the following:

1. Line 10 - Make sure your pytesseract path is correct

2. Line 12 - Replace UsernameHere with your username

Then, all you need to do is run server.py, then run miner.py.


# Fighter.py

This script simply fights cows and eats lobsters when low. Rough script, works but it's messy. I'll likely rewrite this soon.

For this you'll need the following Runelite plugins - Object Marker, Health Notifications

1. Use Object Markers to mark the cows in Pure Red (Red - 255, Green - 0, Blue - 0)

2. In Health Notifications, set the Hitpoint Threshold to whatever you think is best (for leveling combat on new accounts and fighting cows, I set this to 4). Also, set the Overlay Color to Pure Blue (Red - 0, Green - 0, Blue - 255), and check Disable Notification.

Then, run the script.


