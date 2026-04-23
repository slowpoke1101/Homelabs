This project documents my transition from a Raspberry Pi–based all‑in‑one server to a proper router‑based home network using OpenWRT on a Flint router, along with a new NAS setup on the Pi.


File Key:
NASgul2.txt - VMware rehearsal of the 2nd deployment of NASgul
Screenshots - flintnet.jpg: router and openmediavault running on the pi
              dockerps.jpg: shows first few containers i tried
              vw+ph.jpg: shows the web UI's from client VM(sora)

#PLANNED FILES
#DEPLOYMENT
#network diagram


Explanation/Blog: 
After i passed the A+ (so happy, i was nervous haha) i began to study for network+ and got to vlans and deeper subnetting. I thought i had subnets all figured out but my brain broke when i had to recreate my mental model of the network. vlans in relation to subnets also really confused me so i tried for days to grasp these topics and FINALLY i think i get it. this guided my decision to buy a router to add to my network. i chose a modest one that supported openwrt which is basically a purpose built Linux os for routers, that way i wouldn't be restricted by proprietary software and could manually configure my firewall and learn to touch other settings. i was especially excited since i learned that openwrt can use LUCI which is a ui that let's you configure switch/routing settings! up until then i was cli only. i got into LUCI and became more confused lol, i had trouble understanding the separation between wap, switch, and router. that wap has 2 interfaces, one is the wifi ssid which is basically a wireless ethernet port, and the other is a trunk port connected to a trunk port on the switch. this was hard to visualize for me since all 3 are smushed together in the router. i couldn't understand what bridged meant.
	I had/have no real plan for the network at the moment as i am focused on the network+. the only thing i needed a solution to was nextcloud crashing during bulk file transfers, as well as not being able to generate file previews for heic and heiv files. 
	Sadly and with much deliberation i decided to let go of mimiserver and try openmediavault to turn my pi into a nas. letting go of mimiserver was tough, but I wanted a cleaner architecture where the router handled networking and the pi focused on storage.


STATE SO FAR: Basic router hardening. Router configured with 2 bridged networks; trusted and guest. guest lan devices are unable to communicate with eachother, the router, and the trusted net. pi4 rebuilt with manual SMB and docker stack including VaultWarden, Grafana, NodeExporter, CAdvisor, UptimeKuma, Nginx Proxy Manager, AdguardHome, Immich, Memos(PWD), Draw.io, and OpenSpeedTest. ssh disabled but can be manually enabled when i need to administer from my laptop. 3-2-1 manual backups weekly and monthly.