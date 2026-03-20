This project documents my attempt to build a simulated enterprise network using VMware Workstation


File Key:
netopia.md - raw notes and steps
Plan.md - original plan for the network
shellHR.md - html for hr.netopia.lan
shopbuiiild.md - html for show.netopia.lan
rockyserver2.md - instructions to lighten rockylinux and disable ipv6
boockstackdocker.md - failed attempt to install
Screenshots - screenshots with descriptions
#Network diagram


Explanation/Blog: 
While studying for the core 1 and 2 exams( the exam objectives are very broad!) and learning about enterprise topics, i wanted to try to simulate an enterprise network. i also found out that VMware workstation was free and decided to switch to it from vbox. it was unpleasant at first; leaving a familiar environment, but once i got used to VMware it was pretty great. I'd describe the switch as trying to learn professional video editing software after only having used windows movie maker lol. i was falling more and more in love with vms and drooling over being able to run proxmox on bare metal and everything i would be able to learn from that! 
	The plan was to create 3 networks, core infrastructure, employee, and management. i would create a gateway Linux vm that would act as dns dhcp and firewall since that was all i knew how to do. i didnt know if you could create virtual switches or routers in VMware let alone that that's what i had been trying to simulate all along by enabling ipv4 forwarding on my Linux builds.
        I would then create a directory server since i was learning about AD and ldap, as well as an application server and a monitoring node. lastly, i could test segmentation and access with by creating a 'employee' workstation and a 'management' workstation.
	FreeIPA didn't work on ubuntu server which was all i had used at this point, so i had to pivot to rockylinux which was cool. i read about DAC and MAC and sort of understand MAC conceptually but i haven't touched selinux commands yet.
	At this point in my journey i was amazed at discovering wireshark and what i was excited for the most was to get the monitoring tools up and running to be able to inspect network traffic, service usage, hardware stats, etc but i haven't gotten to it yet. tied with that excitement i also wanted to create a vulnerable backend for a fake shopping site so i could exercise an sql injection that i had seen in a youtube video but again, i still didn't realize what i was asking for and how far away i was from understanding what i wanted to know.


STATE SO FAR: gateway is up, directory server is up and serving domain dns, app server is up and running fake portal, hr, shop, and gitea. basic firewall rules in place. tested with domain joined client vm.