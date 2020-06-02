TODO: (Inputs, outputs, variables, etc.)

Toggle Focus: Makes a list of all the lofi and binaural beats windows currently open, closes extras if there are more than 1 of each. Opens one if there isn't at least one of each. If it just opened one, it waits 4.5 seconds (how long my computer takes to open them and display the window title) before calling *Resize Lofi* and *Resize Binaural*. If no windows were opened (as determined by this script) or moved/resized (as determined by Resize Lofi and Resize Binaural) then the open windows are closed.

 - Potential Problem Areas:
	- the profile references on line 24 & 34, make sure they point to the relevant profile on YOUR computer
	- the app id's may not work for you? in which case you'll want to navigate to the [lofi](https://www.youtube.com/watch?v=5qap5aO4i9A) and [binaural beats](https://www.youtube.com/watch?v=SAyA7rfyF38&t=9368s) videos yourself, click the three dots in the upper right corner, "More Tools", "Create Shortcut", make sure to select "Open as window" and then "Create"
	- I have this script tied to the key combination "Alt + Ctrl + F", which you can do after importing it into DisplayFusion
		- If you do this also, you can use the *focus.vbs* file to essentially run this key combo without having to press the keys. Kinda neat!
	- I was running into problems with this script until I made and enabled a trigger that runs when a window of any process "." is created, with an action to Move Window to Mouse Cursor Monitor. I have had no problems since.


Resize Lofi: Gets the open lofi window by its title, resizes it to 65% of the width of the active monitor (as set by Toggle Focus), and positions it against the left side of that monitor. Indicates to Toggle Focus that something has changed if the window changes monitors, size, or location.


Resize Binaural: Same as above, except sizes to 35% the width of the active monitor and positions against the right side of that monitor. (Unless the taskbar is on the side, how I have some monitors setup, in which case it sizes according to the space not used by, and positions the window against, the taskbar.)
