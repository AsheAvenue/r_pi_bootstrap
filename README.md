README:
========
Work in progress to bootstrap a Raspberry Pi.  First cookbooks to add include:

1. vim
2. chromium
3. vnc

NOTES:
--------
Using a slightly modified version of the debian6-gems bootstrap from GitHub: 
> https://github.com/webtatic/configuration/blob/master/chef/bootstrap/debian6-gems.erb

Also had to install "ohai" from apt-get instead of the gem as the gem did not install the proper /bin directory under the gem, so /usr/local/bin/ohai was failing.  Fixed by adding ln -s from the /usr/bin/ohai that is installed from aptitude

###To run:

You will need to add your own validation.pem file to the application directory.  Additionally, I have added a hosts entry to /etc/hosts for:
> raspberrypi 192.168.0.10

###Command:
> knife bootstrap raspberrypi -x pi -Praspberry -d debian6-gems --sudo 

Alternately, I have added a bootstrap__pi.sh script, however it requires the hosts file entry noted above.

PROGRESS:
=========
Currently failing on
> Creating a new client identity for raspberrypi using the validator key.

> raspberrypi 

> raspberrypi [2013-02-10T18:58:20+00:00] INFO: Client key /etc/chef/client.pem is not present - registering

> raspberrypi 

> raspberrypi 

> raspberrypi 

> raspberrypi ================================================================================

> raspberrypi 

> raspberrypi Chef encountered an error attempting to create the client "raspberrypi"

> raspberrypi 

> raspberrypi ================================================================================
