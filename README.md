# Vagrant automated VM for QA Automation development

This repo documents how was create the image fransimo/ubuntu-16.04-desktop-development

To use the already done image you only need to do:
  -  *vagrant init fransimo/ubuntu-16.04-desktop-development*
  -  uncomment config.vm.provider section in Vagrantfile to make vb.gui = true
  -  *vagrant up --provider virtualbox*
  -  default keyboard layout is Spanish to change it edit ~/autostart.sh en change *setxkbmap es* to *setxkbmap en*

This image is an Ubuntu Desktop 16.04 LTS plus:
  -  Oracle Java 8
  -  maven,  ant  
  -  git, git-flow, smartGit, subversion 
  -  eclipse, eclipse-egit, eclipse-maven, eclipse-testng
  -  IntelliJ
  -  testng 
  -  selenium stand alone server
  -  firefox, chromium, chromium-chromedriver
  -  groovy
  -  es and en languajes packs

Base image is: 
  *vagrant init bento/ubuntu-16.04*

Pre:
  -  Image is optimized for Virtual Box, but not restricted to
  -  Make sure ssh and VBox are in path
  -  Default configuration for VM es 4G RAM, 4 core, bidireccional clipboard, active GUI

If you want to generate a new image based on this one:
  -  clone this repo
  -  vagrant plugin install vagrant-reload
  -  vagrant up
  -  to add SQL Developer (need an Oracle account)
    - go to http://www.oracle.com/technetwork/developer-tools/sql-developer/downloads/index.html
	- download Other Platforms .zip
	- sudo unzip Downloads/sqldeveloper-*-no-jre.zip -d /opt/
	- sudo chmod a+x /opt/sqldeveloper/sqldeveloper.sh
	- close session and logon
  -  vagrant package
