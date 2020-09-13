Goal is to show you how to use a Microsoft RDP client to securely connect to an Ubuntu instance on AWS EC2, so we can have a GUI for the Ubuntu instance.

1. Configure Free Tier Ubuntu instance on AWS EC2
2. Connect to Ubuntu instance via SSH with PuTTY
3. Add GUI options to Ubuntu
4. Configure PuTTY to Tunnel RDP traffic
5. Test with RDP

*Link referenced:

https://aws.amazon.com/premiumsupport...

NOTE: The link above now returns a 404 error.  Here are the commands that were copied from the link:

sudo apt update &&  sudo apt upgrade

sudo sed -i 's/^PasswordAuthentication no/PasswordAuthentication yes/' /etc/ssh/sshd_config

sudo /etc/init.d/ssh restart

sudo passwd ubuntu

sudo apt install xrdp xfce4 xfce4-goodies tightvncserver

echo xfce4-session$ /home/ubuntu/.xsession  ##### NOTE: Replace the $ with the Greater Than Sign


sudo cp /home/ubuntu/.xsession /etc/skel

sudo sed -i '0,/-1/s//ask-1/' /etc/xrdp/xrdp.ini

sudo service xrdp restart
