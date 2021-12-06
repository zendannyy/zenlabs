---
layout: post
title: Intro to Linux Setup 
---

This is a continuation of the post
Why would one learn Linux in the first place?
[Intro to Linux ](https://zendannyy.github.io/seventh_post/)

### Get setup with Linux 
Setup instructions 
*This was done on MacOS but the instructions are left a bit general since they don't differ much for OSes*
 
We will install the following
 
1) [Vagrant](https://www.vagrantup.com/downloads)
 
2) [Virtualbox](https://www.virtualbox.org/wiki/Downloads)

Vagrant uses a base image to quickly clone a virtual machine, and saves time and resources in the
installation process. This is faster than setting up a virtual machine manually through a virtual box 
 
 
Virtualbox is the virtualization software that we will use, it is free and platform agnostic.

3) Download the VirtualBox insaller and follow the installation prompts as shown below

<!-- ![Installer Continue](/images/VirtualBox_Install.png) -->
<img src="../images/VirtualBox_Install.png" alt="Installer Continue" width="650"/>
<br>
4) Open up your terminal

Once you get output at the terminal with the following command, you have a successful installation

vagrant -h
<br>
<!-- ![vagrant -h](/images/vagrant_h.png) -->
<img src="../images/vagrant_h.png" alt="vagrant -h" width="650"/>


I like Vagrant for its catalog of box OSes. It's also fairly fast and much more performant than using a local VM on your host machine. 
