# NAC
network access control installation guide on centos7 

 Minimum Hardware Requirements
The following provides a list of the minimum server hardware recommendations:

Intel or AMD CPU 3 GHz, 4 CPU cores
16 GB of RAM
200 GB of disk space (RAID-1 recommended)
1 network card (2 recommended)

On Red Hat-based systems

            Disable firewall
            Disable SELinux

            
Install kernel development package:

yum install kernel-devel-$(uname -r)


sudo yum localinstall http://packetfence.org/downloads/PacketFence/RHEL7/packetfence-release-7.stable.noarch.rpm



Once the repository is defined, you can install PacketFence with all its dependencies, and the required external services (Database server, DHCP server, RADIUS server) using:

yum install --enablerepo=packetfence packetfence

Once installed, the Web-based configuration interface will automatically be started. You can access it from https://@ip_of_packetfence:1443/
