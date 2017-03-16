# duckdns
Instead of using cronjobs and/or any other loop script, let us use Systemd timers to update our domains at DuckDNS. The default Systemd timers are set on every 5 minutes, you can change this yourself

## Installation

### Arch/AUR
info coming soon, probably will be packaged under the name [duckdns](https://aur.archlinux.org/packages/?O=0&K=duckdns)

### Other Linux distro's

Execute these comments

Clone/download this repo on your computer

	cp duckdns.sh /usr/local/bin/duckdns
	cp duckdns.service /usr/lib/systemd/system/
	cp duckdns.timer /usr/lib/systemd/system/
	
	mkdir -p /etc/duckdns.d
	cp default.conf /etc/duckdns.d/
	
	systemctl enable duckdns.timer
	systemctl start duckdns.timer


### Configuration

the **default.conf** file shows perfectly what options you must enter, you can create new files if you have multiple domains with the same setup.

	duckdns_hostname=
	duckdns_token=

Nothing more is needed.

Config files must be placed inside the `/etc/duckdns.d`  folder

