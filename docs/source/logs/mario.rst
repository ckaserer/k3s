****************************
Mario's Personal log
****************************

Day 0 Kickoff
#############

At the kickoff meeting we discussed what we wanted to do and how. The Big Picture:
We want to run a kubernetes cluster.

Why
******

Because its interesting and because it turned out that we can!
Setting up your own kubernetes is a great way to get hands on experience.

How & What
**************

Cluster
=========

We choose a Raspberry Pi cluster. For a couple of reasons:

- It is very affordable
- We get the full experience of a kubernetes on bare metal installation.
- The performance should be plenty for our workload(blinking led's)
- We can get dedicated servers for infrastructure(DHCP,PXE NFS)

Kubernetes
===========

We are using k3s because it seems to be the optimal choice for our hardware

Automation
============

We want to use automation as much as reasonable.
In the first step this means providing a PXE server to automate OS installation on the other machines.
The PXE server itself should be setup via ansible or be available as docker image.
For testing and development of the PXE server we will use vm's managed by vagrant.

Day 1 PXE server exploration phase
###################################

Plan
*******

First steps
=============

* Get the PXE running on a VM
* Get another VM to install an image from the PXE

We will be using vagrant in this step to manage our vm's.

Further steps
=============
When we are happy how everything works we will write ansible roles and a dockerfile.

Work
=============
I never used vagrant or ansible before so i will need to install them and find out how everything works. The same goes for a PXE server.
There are some links that look like good starting points in the <<Links,links section>>.

Log
=============
So vagrant seems easy enough:
sudo dnf install vagrant

Resources
###########

Dev Environment
******************
I am working on a dual boot laptop fedora31/win10 mostly on fedora.

Links
**********

https://diegolemos.net/tag/vagrant/[Vagrant PXE Server]

https://blog.linuxserver.io/2019/12/16/netboot-xyz-docker-network-boot-server-pxe/[PXE Server Docker Image]
