#Vexilla on Vagrant#

If you have a Mac Air you should probably just install the native Mac
tools (per vexilla instructions).  If you don't want to use the cloud
server option (vexilla.herlein.com) and your computer is reasonably
modern you can choose to run a virtual machine.

##Installation##

You will need to install:

    https://www.virtualbox.org/wiki/Downloads
      - install VirtualBox 5.1.0 or later
      - also install the VitualBox Extension Pack
    https://www.vagrantup.com/downloads.html
      - install Vagrant for your computer type

In a terminal, create a folder for this.  I tend to put all my vagrant
files together under ~/vagrant.  Clone this repo into that folder.

      git clone 
      vagrant up

Vagrant will start a virtual machine running linux.  Once it completes
launching you can ssh to that virtual machine by typing:

      vagrant ssh

You will then be logged into a linux computer running virtually on
your computer.

##Installing Vexilla##

First we need to get it ready by installing tools and generating
keys.  From the command line in the linux shell:

      ssh-keygen -b 2048
      cat .ssh/id.id_rsa.pub
      (copy and paste that into github as a new ssh key)
      sudo apt install -y git build-essential
      git clone git@github.com:SHC-Robotics-Team-8255/vexilla.git

Follow the directions per Vexilla to get the tools installed

##Notes##

This vagrant file has the necessary commands to support USB
passthrough so that you can install code onto the robot.  Some
troubleshooting of that may be needed to make settings in VirtualBox
to allow this.  If it complains about no USB ports being available
then you probably did not install the VirtualBox extensions.  Check
that before you do anything else.

