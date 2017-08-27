# Ubuntu-Dual-Screen-Configuration
This is a guide for Macbook Pro 2014 (15-inch) users, who want to use an external monitor.

 # Problem Description:
I wanted to connect my external monitor to my Macbook Pro. When I connected it, I disappointedly realized that everything on the external monitor had a different scaling factor than that of my Macbook Pro. As a result of that everything was extremely big making the external monitor unusable. My first step was to go to the "System Settings" to play with them in the "Screen Display" menu. The only thing I found for scalling was the "Scale for menu and title bars" slider, which reduced the problem, but again the text was very large. After a small research, I found the "Tweak Tool", which would allow me to change the HiDPI scaling factor, or at least in theory, but it was buggy and I could not do what I wanted to do. The problem was that it was very difficult for the operating system to handle and set the HiDPI screen (Retina Display) and the regular monitor variables at the same time. A HiDPI screen is a high resolution screen in a relatively small format.

 # Solution:
The solution was to do it by hand. I went over to the Arch Linux community's forum and I tried to find a way to deal with HiDPI screens and they were suggesting to use the xrand. After playing a little bit with this tool I managed to get the result I wanted with these two commands in this order.

Command 1:
`xrandr --output HDMI-3 --scale 1.5x1.665 --mode 1920x1080 --fb 2880x1800 --pos 0x0`

Command 2:
`xrandr --output eDP-1 --scale 1x1 --pos 0x1798`

 # Explantion of my Solution:
 
