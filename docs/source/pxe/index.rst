************
PXE Server
************

Overview
########

The Acronym
------------

PXE stands for Pre-boot eXecution Environment

Why
-----

The PXE server provides bootfiles and OS images over LAN.
This means you don't have to copy images to usb sticks and go from machine to machine anymore.
That's great if you have seven machines that will be setup again and again until you get everything working right.

Goals
------
* The PXE module provides a PXE server.
* The PXE server can be setup via ansible.
* The PXE server is also available as a docker image.
