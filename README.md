# HoneyPot
Created a HoneyPot that retrieves geolocations of people trying to hack into my virtual machine through RDP. I setup Azure Sentinel (SIEM) and connect it 
to a live virtual machine acting as a honey pot. We will observe live attacks (RDP Brute Force) from all around the world. I removed all firewalls to let 
attackers try and use RDP Brute Force to connect to my virtual machiene. and used a custom PowerShell script to look up the attackers Geolocation based on their IP 
information and create a log of that information. Then I imported that log onto Azure Sentinel's (Microsoft's SIEM) log analytics to pull that data
and create a geographical display of where the attacks are coming from
<img width="1440" alt="Failed RDP Map 2" src="https://user-images.githubusercontent.com/110569598/183270665-aa93ee17-b6ea-4319-b506-287a6625439c.png">

After about three hours this is the attacks I got! Each number is the amount of attempted sign in's to the computer. We see these users using RDP
Brute Force, which is just a bot that tries multiple combinations of usernames and passwords, attempting to hack the computer.
