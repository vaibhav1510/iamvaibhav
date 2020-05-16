---
layout: post
title:  "Update Installation Guide - The softwares to install"
date:   2016-07-31 21:03:36 +0530
categories: Javascript NodeJS
---

Installation steps

* mkdir dump work installationfiles
* sudo apt-get install vim
* sudo apt-get in
* stall meld
* sudo apt-get install ant
* sudo apt-get install maven (32 bit)
* sudo apt-get install maven2 (64 bit)
* sudo apt-get install gimp
* sudo apt-get install vlc
* sudo apt-get install openssl
* sudo apt-get install password-gorilla
* mysql-server install
	* sudo apt-get install mysql-server (Don’t Give Any Password, Just Press ‘Enter’ if it asks)
* Install DropBox
	* Follow https://www.dropbox.com/install?os=lnx OR
	* cd ~ && wget -O - "https://www.dropbox.com/download?plat=lnx.x86" | tar xzf -
* sudo apt-get install build-essential
* sudo apt-get install bison
* sudo apt-get install cmake cmake-gui
* sudo apt-get install libncurses5-dev
* sudo apt-get install libaio1 libaio-dev
* sudo apt-get install xpad
* sudo apt-get install curl
* install ruby and compass
	* sudo apt-get install ruby
	* \curl -L https://get.rvm.io | bash -s stable --ruby
	* source ~/.rvm/scripts/rvm  
	* gem install compass
* github
* install git
	* sudo apt-get install git
	* http://help.github.com/linux-set-up-git/   for setting up ssh keys.
	* git config --global core.editor "vim"
	* git clone git@github.com:chargebee/chargebee-app.git
	* git clone git://github.com/chargebee/chargebee-java.git
* jdk download n install
* Follow this link (http://www.devsniper.com/ubuntu-12-04-install-sun-jdk-6-7/)
* OR
* Download the sun jdk 6 bin from here
* (http://www.oracle.com/technetwork/java/javase/downloads/jdk-6u32-downloads-1594644.html)
* chmod +x jdk-6u32-linux-x64.bin
* ./jdk-6u32-linux-x64.bin
* sudo mv jdk1.6.0_32 /usr/lib/jvm/
* sudo update-alternatives --install /usr/bin/javac javac /usr/lib/jvm/jdk1.6.0_32/bin/javac 1
* sudo update-alternatives --install /usr/bin/java java /usr/lib/jvm/jdk1.6.0_32/bin/java 1
* sudo update-alternatives --install /usr/bin/javaws javaws /usr/lib/jvm/jdk1.6.0_32/bin/javaws 1
* sudo update-alternatives --config javac
* sudo update-alternatives --config java
* sudo update-alternatives --config javaws
* java -version
* netbeans download and install.
* mysql install
* Download mysql source -> http://forge.mysql.com/wiki/CMake

* make
* make install
* ./scripts/mysql_install_db
* http://beginrescueend.com/rvm/install/
* https://rvm.beginrescueend.com/packages/zlib/ (before installing ruby)
* http://compass-style.org/install/
* :~/work/chargebee-java$ mvn clean package

# Setting Up Git Steps
* git config --global user.name "Your Name Here"
* git config --global user.email "your_email@youremail.com"       
* ssh-keygen -t rsa -C "your_email@youremail.com"
* cd ~/.ssh

For compass if above is not working(execute all of them even if they show  error)
* sudo apt-get install ruby-full
* sudo apt-get install rubygems1.8
* sudo gem install rails
* sudo gem install sqlite3
* sudo gem update --system  
* sudo gem install compass
* sudo gem install sass
* 

Upgrade to mysql 5.5 from 5.1 in ubuntu
* http://www.krishnasrikanth.com/blog/post.php?id=360
