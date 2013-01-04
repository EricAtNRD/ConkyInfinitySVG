# InfinitySVG: A Theme for Conky


## About

InfinitySVG is a theme for the "conky" system monitor for X. It is mostly based on the Infinity theme by Harshit Yadav.

![InfinitySVG screenshot](images/InfinitySVG-screencap-960w.png)

For Harshit Yadav's original theme, please see: [Infinity on Deviantart.com](http://harshit1990.deviantart.com/art/Infinity-306921086)


## Acknowledgements

As best I can tell, the following people had a hand in the creation of this theme.  Thank you!

- InfinitySVG by: Eric Weik
	- [http://www.newriversdigital.com/](http://www.newriversdigital.com/)
- Vector icons used in the background: "Iconic" by P.J. Onori
	- [http://somerandomdude.com/work/iconic/](http://somerandomdude.com/work/iconic/)
	- [https://github.com/somerandomdude/Iconic](https://github.com/somerandomdude/Iconic)
- Original Infinity theme by:	Harshit Yadav
	- [http://harshit1990.deviantart.com/art/Infinity-306921086](http://harshit1990.deviantart.com/art/Infinity-306921086)
- Includes lua code: Clock Rings by londonali1010 (2009)
	- [http://londonali1010.deviantart.com/](http://londonali1010.deviantart.com/)


## Installation Instructions

1. Install Conky
	- Ubuntu:   apt-get install conky-all
	- Fedora: yum install conky
	- Other: see your local documentation or try [the Conky documentation](http://conky.sourceforge.net/documentation.html).

2. Extract the InfinitySVG tar file into its own directory somewhere.

3. Copy .conkyrc, .lua, and .conky to your home directory:
	- cp --archive .conkyrc ~/
	- cp --archive .conky ~/
	- cp --archive .lua ~/

4. Open ~/.conkyrc in your favorite editor and adjust the screen resolution:
	- minimum_size 1920 1080

5. (optional) This theme uses Compiz for partial transparency of the conky output. If you are **not** using a compositing window-manager such as compiz, you can make the conky window transparent by altering the following settings in ~/.conkyrc (if you are using compiz, skip this step and use step 9 instead).

		# Allow conky to handle transparency
		own_window_type conky
		own_window_transparent yes
		
		# Allow compiz to handle transparency (you will need to add Conky to compiz)
		# own_window_type normal
		# own_window_transparent no
		
6. (optional) Check haunted.lua for any additional adjustments required for your screen resolution.

7. Now you are ready to run conky.  Open a terminal and run the following:

		chmod a+x ~/.conky/startconky.sh
		sh ~/.conky/startconky.sh
		(Conky will start after 5 seconds.)

8. Add ~/.conky/startconky.sh as a startup application.

	- Ubuntu: Dash > (search) Startup Applications > Add
	- Other: see your location documentation to add this as a startup application.

9. We can use Compiz to make the conky window partially transparent.  This can be accomplished via ccsm - CompizConfig Settings Manager, use with caution (it is fairly easy to render your desktop unusable with ccsm).  If use set up conky to handle transparency in step 5, skip this step.
	- If not installed, install compizconfig-settings-manager 
	- Run ccsm
	- Go to: Accessibility > Opacity, Brightness and Saturation > (enable if not already)
	- In the Opacity tab, click "New"
	- In "Windows" enter "name=Conky" (exactly as shown -- do not just type "Conky")
	- In "Window values" enter "66" or so (higher for less transparent, lower for more)

10. Tweak the background image if you wish.
	- A vector based version of .conky/background.png is available for Inkscape in: images/background.svg
	- If you edit the svg, simply export the "page" at 90dpi and replace: .conky/background.png

11. Extras - Included in extras/terminator/config is a config file for the "Terminator" terminal program.  This sets up Terminator with a color scheme that matches this Conky theme.  To install it, back up your existing terminator configuration (~/.config/terminator/config) and copy in the one from extras/terminator/config.  ** If you have your own terminator config, you may wish to manually merge the title colors and profile colors from the supplied file into your own configuration.

12. Other notes:
	- The following scripts were written separately and currently are not used. You can delete them if you wish:
	
		- cpu
		- mail
		- mem
		- rings (this is an earlier version of the rings clock by 
		Ken Berns <ken.berns@yahoo.de>)
		- weather

	- For testing:  if you are testing changes to your background or the configuration files, you can skip using startconky.sh, and simply run conky directly.  In the distribution .conkyrc it is set to run in the background (via: background yes).  This means you'll need to run "killall conky;conky" to restart it.
	- A few random items in .conkyrc you might want to look at:
		
		- update_interval 5.0 (update interval in seconds)
		- default_color b7b7b7 (color of most of the text and graph outlines)
		- At the very bottom are a few examples of static text (a logo and multi-line text) that can be uncommented
	

