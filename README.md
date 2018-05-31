# fritzbox-api
Bash script to collect various information from your Fritzbox via its SOAP api

As I could not find much information on this in english, this is a combination of a few scripts I found online from some european blogs (not in my native language)
So lets give a thanks to
- http://www.gtkdb.de/index_36_2458.html
- http://blog.gmeiners.net/2013/09/fritzbox-mit-nagios-uberwachen.html#
and
- https://github.com/Harrdy/pimatic-fritzbox-upnp

Script can output:
- link uptime 
- connection status
- maximum upstream sync speed on current connection
- maximum downstream sync speed on current connection
- Current downstream bandwidth usage
- Current upstream bandwidth usage
- Total download usage on current connection
- Total upload usage on current connection

This can also output all of the above in  JSON format, useful for ingesting into another program and when running via cron (e.g I read this information into openHAB)

The purpose for this was so I could get the current bandwidth usage across the WAN link into openHAB, for monitoring and for making pretty graphs on usage during the day. And I could see the current bandwidth usage at a glance, incase I was having some issues and quick diagnosis. I have made this script a little more bare, without all the openHAB specific stuff in it

#### dependancies
- bc
- curl
