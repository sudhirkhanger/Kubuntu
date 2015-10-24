## lm-sensors

    sudo apt-get install lm-sensors
    sudo sensors-detect
    
## Thinkfan

    sudo apt-get install thinkfan
    echo "options thinkpad_acpi fan_control=1" | sudo tee /etc/modprobe.d/thinkfan.conf

    /etc/default/thinkfan
    START=yes
    DAEMON_ARGS="-q -b 1 -s 3"

    /etc/thinkfan.conf
    find /sys/devices -type f -name "temp*_input"

    cat /proc/acpi/ibm/thermal
	
[Source](http://thinkwiki.de/Thinkfan)

## Temperature Sensors Widget

    sudo apt-get install lm-sensors plasma-scriptengine-python
    sudo sensors-detect

## Nvidia Optimus

    sudo apt-get install bumblebee bumblebee-nvidia primus linux-headers-generic
    
## VDPAU VAAPI

    sudo apt-get install libvdpau1 vdpau-va-driver i965-va-driver vdpauinfo vainfo libvdpau-va-gl1
    echo 'export VDPAU_DRIVER=va_gl' > ~/.bash_aliases
  
## Plasma Widgets

    sudo apt-get install plasma-widget-homerun-kicker plasma-widget-redshift redshift
  
## Emacs

    sudo apt-get install emacs markdown emacs-goodies-el
  
## Plasma Apps

	sudo apt-get install konversation kwrite
  
## Multimedia
  
	sudo apt-get install kubuntu-restricted-extras vlc banshee easytag soundkonverter kffmpegthumbnailer kdegraphics-thumbnailers kdesdk-thumbnailers
  
## Development

	sudo apt-get install git
  
## Others

	sudo apt-get install keepassx ksshaskpass libreoffice-style-sifr kdeconnect deja-dup skype handbrake wine htop powertop
  
## Remove

	sudo apt-get remove kate quassel-data brasero-common

## Calibre

	sudo -v && wget -nv -O- https://raw.githubusercontent.com/kovidgoyal/calibre/master/setup/linux-installer.py | sudo python -c "import sys; main=lambda:sys.stderr.write('Download failed\n'); exec(sys.stdin.read()); main()"

## Hibernate

	/etc/polkit-1/localauthority/50-local.d/com.ubuntu.enable-hibernate.pkla

	[Re-enable hibernate by default in upower]
	Identity=unix-user:*
	Action=org.freedesktop.upower.hibernate
	ResultActive=yes

	[Re-enable hibernate by default in logind]
	Identity=unix-user:*
	Action=org.freedesktop.login1.hibernate
	ResultActive=yes

[Source](http://blog.mafr.de/2014/05/01/enabling-hibernate-support-in-ubuntu-14-04/)

## ownCloud

[Source](https://software.opensuse.org/download/package?project=isv:ownCloud:desktop&package=owncloud-client)

## Oracle Java 8

[Source](http://www.webupd8.org/2012/09/install-oracle-java-8-in-ubuntu-via-ppa.html)

## Android

### Install

	sudo dpkg --add-architecture i386
	sudo apt-get update
	sudo apt-get install libncurses5:i386 libstdc++6:i386 zlib1g:i386

### KVM
	sudo apt-get install qemu-kvm libvirt-bin ubuntu-vm-builder bridge-utils
	
[Source](https://software.intel.com/en-us/blogs/2012/03/12/how-to-start-intel-hardware-assisted-virtualization-hypervisor-on-linux-to-speed-up-intel-android-x86-emulator)

### udev Rules

	cd /etc/udev/rules.d
	wget https://raw.githubusercontent.com/M0Rf30/android-udev-rules/master/51-android.rules
	chmod a+r /etc/udev/rules.d/51-android.rules

## Ksuperkey

	sudo add-apt-repository ppa:mehanik/ksuperkey
	sudo apt-get update
	sudo apt-get install ksuperkey

	ksuperkey -e 'Super_L=Alt_L|F2'

## VirtualBox

	wget -q https://www.virtualbox.org/download/oracle_vbox.asc -O- | sudo apt-key add -
	sudo apt-get update
	sudo sh -c "echo 'deb http://download.virtualbox.org/virtualbox/debian trusty contrib' >> /etc/apt/sources.list.d/oracle-virtualbox.list"
	sudo apt-get update
	sudo apt-get install virtualbox-5.0
	sudo usermod -a -G vboxusers $USER

## Genymotion

	chmod +x genymotion-2.5.2_x64.bin
	./genymotion-2.5.2_x64.bin

## Qt Creater

	sudo add-apt-repository ppa:ubuntu-sdk-team/ppa
	sudo apt-get update
	sudo apt-get install qtdeclarative5-examples qtdeclarative5-dev qmlscene qtcreator

## SimpleScreenReader

	http://www.maartenbaert.be/simplescreenrecorder/#download
	sudo add-apt-repository ppa:maarten-baert/simplescreenrecorder
	sudo apt-get update
	sudo apt-get install simplescreenrecorder simplescreenrecorder-lib:i386

## Import GPG Keys

	gpg --import secretkey.asc
	gpg --edit-key KEYID trust
	gpg --edit-key KEYID > Chose primary uid > primary > save

## Inkscape

	sudo add-apt-repository ppa:inkscape.dev/stable
	sudo apt-get update
	sudo apt-get install inkscape

## GIMP

	sudo add-apt-repository ppa:otto-kesselgulasch/gimp
	sudo apt-get update
	sudo apt-get install gimp gimp-gmic gimp-plugin-registry
	
## TLP

	sudo add-apt-repository ppa:linrunner/tlp
	sudo apt-get update
	sudo apt-get install tlp tlp-rdw tp-smapi-dkms acpi-call-dkms
	
[Source](http://linrunner.de/en/tlp/docs/tlp-linux-advanced-power-management.html#installation)
	