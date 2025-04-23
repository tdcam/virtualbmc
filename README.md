# virtualbmc
These are the playbooks for creating a virtual BMC (vbmc) on a RHEL 
hypervisor. Please note this is NOT designed for any sort of production 
work, it is only for demonstrating OpenShift installations on "bare 
metal." It is ABSOLUTELY not secure. I would not use this in any sort 
of production environment. I have not analyzed any of the python code 
(because I am a terrible developer and it wouldn't do a bit of good). 
I intentionally make changes to advertise the virtual BMC to the network, 
contrary to the developer's intent. This is probably catastrophically 
dumb. But it is a cool way to emulate bare metal machines.

If you use this in production, you're a silly, silly person. I guarantee 
NOTHING! If it breaks, you get to keep all the pieces. I will tease you 
mercilessly, and probably use my favorite Monty Python insults on you.

YOU HAVE BEEN WARNED. THIS IS ONLY FOR DEMONSTRATION PURPOSES!

DON'T USE IT IN PRODUCTION!

The steps are to:
 - register the machine to Red Hat (assumed, no playbook for this)
 - install EPEL
 - install some EPEL packages
 - pip install virtualbmc
 - modify the python code so the virtual BCM listens on the network (DUMB)
 - create a systemd unit file and enable it
 - define the vbmc for each machine and start it
 - open the apprioriate firewall ports
 - use ipmitool to check that the vbmc is working

I've broken this down into small playbooks so it's easy to follow.

