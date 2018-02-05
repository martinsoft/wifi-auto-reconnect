# wifi-auto-reconnect
A simple script intended for use on Mac OS devices connected to a network with wifi only. 

The script periodically checks whether an IP address (ideally a router) is reachable. If 
unreachable, the script switches the device's wifi off and back on again - which causes the
Mac to attempt to reconnect to the last used network. 

This is useful for headless Macs which might drop off of a network if, for example, the wifi
router is restarted. (For some reason Mac OS does not automatically reconnect if a wifi 
network becomes discconected). 


## Configuration
* Save the `wifiautoreconnect` script to a suitable location on your Mac.
* Update the `wifiautoreconnect` script - speciying the IP address that the script should check against (typically your router's IP):
  `ROUTER_IP_ADDRESS="10.0.1.1"`
  
## Usage
* You can run the script directly - simply execute `./wifiautoreconnect` from the command line.
* Or you can configure the script to launch automatically when your Mac restarts using launchctl
  * Install the launch agent using the included install script, which attempts to install wifiautoreconnect into `~/Library/Scripts`
  * If you change the location in the install script, be sure to update the path in the included `net.martinsoft.wifiautoreconnect.plist` (you can edit this using a text editor). 

