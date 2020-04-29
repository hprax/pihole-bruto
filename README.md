# pihole-bruto
Instructions to setup a Raspberry Pi running PiHole + DoH

Overview:

	1 - Raspberry Pi (3B+ or 4) - ** Pt_BR ** se vc for um arrombado mao de vaca, um Pi zero ou 2 funciona (mas beeemm lento) **/PT_BR**
	2 - Raspbian (base OS)
	3 - Cloudflared - DoH (Dns over HTTPS)
	4 - Pihole
	5 - Network settings / changes 
 
 
1 - Raspberry Pi
	
	Raspberry Pi 3B+ / 4
	Recommended to run a decent SD card (Sandisk Extreme or Samsung Evo) 16GB or bigger

  
2 - Raspbian

	- Download and install the balenaEtcher - https://www.balena.io/etcher/
	- Download the latest raspbian image (Lite version) - https://www.raspberrypi.org/downloads/raspbian/
	- "Burn" the img to the SD card with Balena Etcher
	- If using Wifi (Not recommended for your Network DNS server) you need to setup the wpa_supplicant.conf (sample into the "boot" folder of the repo)
	- Enable ssh access - add a file named "ssh" to the boot directory (mount the SD in your computer) (sample into the "boot" folder of the repo)
	- Boot the RPi with the SD that you have customized and update the system (apt-get update , apt-get upgrade)
  

3 - CloudFlared

	CloudFlared is a Opensource DoH client recommended by CloudFlare, this client will be used as a proxy to perform the DNS requests 

		*Automatic Install*
		Copy and run the following command		
		> curl -sSL https://raw.githubusercontent.com/hprax/pihole-bruto/master/install/install_cloudflared | sudo bash
			

		*Manual Install* (Basically a copy and paste of the previous install script)
		Creating the temp folder
	
		> mkdir /tmp/bruto_temp
		> cd /tmp/bruto_temp/
		