# openwrt-fancontrol

A replacement for /sbin/fan_ctrl.sh, based on [this post](https://forum.openwrt.org/viewtopic.php?pid=280811#p280811) from the OpenWRT wrt1900ac thread.

####To use it:

* Download the new fan controller, save it to  /etc/, and make it executable.
```
/usr/sbin/fancontrol.sh
chmod +x fancontrol.sh
```

* Test it to make sure that it runs correctly.
```
/usr/sbin/fancontrol.sh verbose
```

* Let it run in the background to keep your router cool.
```
/usr/sbin/fancontrol.sh &
```

####Disable the orginal fan controller.
*	Remove or comment out this line from /etc/crontabs/root (In LuCI, it's System > Scheduled Tasks)
```
 */5 * * * * /sbin/fan_ctrl.sh
```

####Optional
* Have this run on boot.
* Add this to /etc/rc.local (In LuCI, it's System > Startup)
```
/etc/fancontrol.sh &
```
Or place fan_control into /etc/init.d/ 


