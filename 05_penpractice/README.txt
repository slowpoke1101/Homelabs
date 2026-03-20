This project documents my first real dive into security: building a vulnerable VM, setting up DVWA, and trying to hack my own systems to understand how pentesting actually works


File Key:
DAMNvulnerableWEBapp.md - installation steps
WordpressINSTALL.md - installation steps
wp-dvwa-scan.jpg shows both web apps accessible on attacker vm browser. nmap shows all 3 devices on the same sandboxed subnet


Explanation/Blog
After building mimiserver, mimilab3, and Netopia, I started getting more curious about security. I had always been interested in hacking, but up until this point i didnt really understand what pentesting actually involved. I figured the best way to learn was to try attacking something i built myself.
	I created a vulnerable VM with services like SSH, vsFTPd, and Apache, and then used another VM to try to enumerate and break in. i learned that you need to understand how web developers design and build their web apps before you could begin to try to break them so i learned about wordpress and installed it on the vulnerable vm and now have a platform to try to build my own website. Shortly after i learned about DVWA which is a web server built to be intentionally vulnerab. It was everything i had been tryng to do myself all this time! I then made a new VM with lamp + dvwa and now the stage was finally set! This was my first real exposure to things like service banners, open ports, weak configurations, and how attackers actually gather information. Again i quickly I realized how much i still didnt know. Modern applications are hardened, and you can’t just 'hack Nextcloud' or 'hack Pi‑hole' as a beginner. I also learned that pentesting is not like 'movie hacking' it's a lot more thoughtful and slower paced, You have to be patient, understand the network, the OS, the services, the configs, and the vulnerabilities
	Even though I didnt get very far with actual exploitation, I learned about how to safely isolate attack labs, how to set up intentionally vulnerable machines, how to use nmap and other enumeration tools, how services expose information, andhow much foundational knowledge I still need
	I will continue pursue my current passions; networking and Linux, and hopefully in time, as i continue to revisit pentesting, things will grow clearer

State So Far:
Necessary packages downloaded and installed before sandboxing the netowrk+vms. Vulnerable VM created with ssh, vsftpd, Apache2. DVWA vm is up and working. ubuntu attacker vm configured with basic network tools and some kali packages installed. Simple enumeration performed from attacker VM. I am currently rotating between studying for network+, building out my new home network, learning Linux, and trying basic web enumeration and attacks.
