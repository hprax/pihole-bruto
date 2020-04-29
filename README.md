# pihole-bruto
Instructions to setup a Raspberry Pi running PiHole + DoH

Overview:

	1 - Raspberry Pi (3B+ or 4) - se vc for um arrombado mao de vaca, um Pi zero ou 2 funciona (mas beeemm lento)
	2 - Raspbian (base OS)
	3 - Cloudflared - DoH (Dns over HTTPS)
	4 - Pihole
	5 - Network settings / changes 
 
 
1 - Raspberry Pi
	Recommended to run a decent SD card (Sandisk Extreme or Samsung Evo) 16GB or bigger
	Decent Power supply (Original one is great)
  
2 - Raspbian
	- Download and install the balenaEtcher - https://www.balena.io/etcher/
	- Download the latest raspbian image (Lite version) - https://www.raspberrypi.org/downloads/raspbian/
	- "Burn" the img to the SD card with Balena Etcher
	- If using Wifi (Not recommended for your Network DNS server) you need to setup the wpa_supplicant.conf (example in the repo)
	- Enable ssh access - add a file named "ssh" to the boot directory (mount the SD)
  
