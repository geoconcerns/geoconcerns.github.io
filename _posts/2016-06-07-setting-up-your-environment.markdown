---
layout: walkthrough
title:  "Setting Up Your Environment - Part 1 - Walkthrough of GeoConcerns"
date:   2016-06-07 11:29:00
categories: tutorial
author: 'Eliot Jordan'
author_link: 'https://github.com/eliotjordan'
snippet: 'Setting up your development environment for GeoConcerns. Created as part of a tutorial series given in a Walkthrough of GeoConcerns'
---

## Setting up your environment
  - Development requirements
  - Local attendees setup VirtualBox/Vagrant

### Development requirements

GeoConcerns has similar prerequisites to the Hydra [Curation Concerns][curationconcerns] project. There are additional dependencies related to processing geospatial data.

#### Software you should have installed on your development computer

  - [Ruby > 1.9.3][installruby]
  - [Rails > 4][installrails]
  - [Git][installgit]
  - [Redis][installredis]
  - [Oracle Java JDK > 8][installjava]
  - [ImageMagick][installimagemagick]
  - [GDAL][installgdal]
  - [Mapnik][installmapnik]


Local attendees of the workshop have the option of just using the pre-created environment on the provided thumb-drive. If you are not at the workshop, you can create the virtual machine for the workshop, by following [this guide](https://github.com/geoconcerns/geo-concerns-vagrant).

### Local attendees setup VirtualBox/Vagrant
  
Good news for local workshop participants, this is already done for you using VirtualBox and Vagrant. On the thumb-drive underneath a directory titled 'geo-concerns-vagrant'.

 - [Vagrant for OS X and Linux](#vagrant-for-os-x-and-linux)
 - [Vagrant for Windows](#vagrant-for-windows)

#### Vagrant Quick Tips
After you have your virtual machine up and going, you will want to stop it. Here are a few commands that will help out.

```sh
$ vagrant halt # stops the virtual machine
$ vagrant destroy # stops and deletes the virtual machine
```

#### Vagrant for OS X and Linux
  1. Install the Mac (.dmg) version of VirtualBox and Vagrant on your machine. If you are using Linux, please download and install appropriately. [VirtualBox Downloads](https://www.virtualbox.org/wiki/Downloads), [Vagrant Downloads](https://www.vagrantup.com/downloads.html)

  1. If not already on your Desktop, copy the `geo-concerns-vagrant` directory to your `~/Desktop` directory

  1. Move to your `~/Desktop/geo-concerns-vagrant` directory
 
     ```sh
     $ cd ~/Desktop/geo-concerns-vagrant
     ```

  1. Start vagrant

     ```sh
     $ vagrant up # This command creates and configures guest machines according to your Vagrantfile.
     ```

  1. SSH to the VM

     ```sh
     $ vagrant ssh # This will SSH into a running Vagrant machine and give you access to a shell.
     ```

#### Vagrant for Windows

Thanks to Zach Vowell who contributed this guide for Windows.

Note: Please install a Windows ssh client installed such as [ PuTTY](http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html).

  1. Install the Windows (.exe) version of VirtualBox and Vagrant on your machine.

  1. If not already on your Desktop, copy the `geo-concerns-vagrant` directory to your Desktop `C:\Users\[username]\Desktop` (for Windows 7)

  1. Open a [Windows Command Prompt (cmd)](http://www.digitalcitizen.life/7-ways-launch-command-prompt-windows-7-windows-8)

  1. Move to the `geo-concerns-vagrant` directory on the Desktop

     ```
     C:\Users\[username]> cd Desktop\geo-concerns-vagrant
     ```

  1. Start Vagrant

     ```
     C:\Users\[username]\Desktop\geo-concerns-vagrant> vagrant up
     # This command creates and configures guest machines according to your Vagrantfile.
     ```

  1. Open up PuTTY

  1. SSH into the Vagrant box by entering the following parameters into the "Basic Options for Your PuTTY session" window:
    - Host Name (or IP address): 127.0.0.1
    - Port: 2222

  1. When PuTTY shell prompts for a username and password, enter "vagrant" for both. You should now see a command prompt.

<div class='flash-notice'>
  <a href="{% post_url 2016-06-07-starting-the-application %}">Next → Starting the application</a>
</div>

[curationconcerns]:     https://github.com/projecthydra/curation_concerns
[installruby]:          https://gorails.com/setup#ruby
[installrails]:         https://gorails.com/setup#rails
[installgit]:           https://gorails.com/setup#git
[installredis]:         http://redis.io/
[installimagemagick]:   http://www.imagemagick.org/
[installgdal]:          http://www.gdal.org/
[installmapnik]:        http://mapnik.org/pages/downloads.html
[installjava]:          http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html
[rubyonrails]:          http://rubyonrails.org/
