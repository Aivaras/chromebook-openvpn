Chromebooks have a weird way of managing network interfaces.
Service shill, by default kills all new interfaces if finds... weird.
So if you would like to start openvpn from terminal you will get an error "No device". Because shill kills it.

To avoid it there is a way:

	1. "sudo stop shill" it stops shill service and you will lose connection.

	2. "sudo shill --device-black-list=tun0" start service and blacklist tun0 device so shill won't kill it.

	3. "sudo openvpn ~/Downloads/client.ovpn"


I also provided sample config file for my vpn setup. 
