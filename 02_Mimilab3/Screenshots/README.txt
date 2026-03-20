Screeshots Key:

dns-adblock-docker.jpg: shows ssh from client vm swordofelendil to mimilab3. unbound active and a successful dig @ localhost where i configured a listening pihole container pointing to unbound for dns

iptableschains-ss.jpg: shows firewall rules enabling only the client vm to access https, http, ssh, and dns from mimilab3 through wireguard and block everything else.

mimilab3-ss.jpg: shows server and client with ip's on server's subnet and both pihole web ui and nextcloud accessible in a browser.

services-ss.jpg: shows active listening services on mimilab3

P.S.
if you were wondering why the ss's show VMware instead of vbox, it's because i moved on to VMware a while ago and exported mimilab3 from vbox to be able to take these screenshots