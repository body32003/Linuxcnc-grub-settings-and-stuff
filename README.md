sudo apt-install gedit
=================================

deb http://buildbot2.highlab.com/debian/ buster master-uspace 2.9-uspace 2.8-uspace scratch-uspace

2.9-rt
=======================================================

sudo nano /etc/default/grub
=================================
GRUB_CMDLINE_LINUX_DEFAULT="quiet
-----------------------------------

The kernel parameters that worked for my machine and you could try:
isolcpus=3 intel_pstate=disable processor.max_cstate=0 idle=poll cpufreq.default_governor=performance i915.enable_dc=0 ahci.mobile_lpm_policy=1 irqaffinity=0 nomodeset quiet

sudo update-grub
----------------------------------------------------------------------------------------------------------------


sudo nano /etc/lightdm/lightdm.conf
------------------------------------
autologin-user=yourusername
autologin-user-timeout=0


-----------------------------------------------------------------------------
VGA resolution
------------------------------------
sudo nano .config/xfce4/xfconf/xfce-perchannel-xml/displays.xml  

>>>>> property name="DVI-0" <<<<

---------------------------
$ cvt 1920 1080
# Modeline "1920x1080_60.00"  173.00  1920 2048 2248 2576  1080 1083 1088 1120 -hsync +vsync

$ xrandr --newmode "1920x1080_60.00"  173.00  1920 2048 2248 2576  1080 1083 1088 1120 -hsync +vsync

$ xrandr --addmode DVI-0 1920x1080_60.00

$ xrandr --output  DVI-0 --mode 1920x1080_60.00
