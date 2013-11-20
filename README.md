Skype4 ports for FreeBSD
========================

Description
-----------
Skype is a free program that uses the latest P2P technology to bring
affordable and high-quality voice communications to people all over
the world.

http://www.skype.com/

Installation
------------
You will need to make sure you have latest ports tree before you attempt to install `net-im/skype4`. The FreeBSD Handbook is a place where you need to visit and read. 

First you should uninstall linux-f10* ports and its dependencies. To make it easier, you can use portmaster(8) for that purpose:

    # portmaster -e target_port

Before starting to install, be sure that you add both lines to /etc/make.conf:

    OVERRIDE_LINUX_BASE_PORTS=c6
    OVERRIDE_LINUX_NONBASE_PORTS=c6
    
Change the compatibility level of the Linux kernel OS release by running the following command:

    # sysctl compat.linux.osrelease=2.6.18

Also add this sysctl(8) variable to /etc/sysctl.conf to make the change permanent:

    # echo 'compat.linux.osrelease=2.6.18' >> /etc/sysctl.conf

Note that it's necessary have enabled LBC before you can install Skype4 port. Read for further details the corresponding Chapter 11. Linux Binary Compatibility of the FreeBSD Handbook.
    
You will need to merge the skype4-ports into your /usr/ports. Now you are ready to install `net-im/skype4`.

    # portmaster net-im/skype4

