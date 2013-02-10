README:
Work in progress to bootstrap a Raspberry Pi.  First cookbooks to add include:

1. vim
2. chromium
3. vnc

NOTES:
Using a slightly modified version of the debian6-gems bootstrap from GitHub: 
	https://github.com/webtatic/configuration/blob/master/chef/bootstrap/debian6-gems.erb

To run:
You will need to add your own validation.pem file to the application directory.  Additionally, I have added a hosts entry to /etc/hosts for:
	raspberrypi 192.168.0.10
Command:
	knife bootstrap raspberrypi -x pi -Praspberry -d debian6-gems --sudo 

