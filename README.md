# VM-Screen-Size
script to help setting screen size of a linux vm  
replace resolution with your own values (used in script is 1920x1080)

```bash
# First, get the actual Modeline
cvt 1920 1080
# Copy the cvt modeline to the below command
xrandr --newmode "1920x1080_60.00"  173.00  1920 2048 2248 2576  1080 1083 1088 1120 -hsync +vsync
xrandr --addmode Virtual-1 1920x1080_60.00
xrandr --output Virtual-1 --mode 1920x1080_60.00
```

you'd want to run that as boot to make it persistent
