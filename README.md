# Kubuntu

#lm-sensors

    sudo apt-get install lm-sensors
    sudo sensors-detect

#Thinkfan
    
    sudo apt-get install thinkfan
    echo "options thinkpad_acpi fan_control=1" | sudo tee /etc/modprobe.d/thinkfan.conf
    /etc/default/thinkfan START=yes  DAEMON_ARGS="-q -b 1 -s 3"
    find /sys/devices -type f -name "temp*_input"

http://thinkwiki.de/Thinkfan

#Multimedia
    
    sudo apt-get install kubuntu-restricted-extras

# Random software

  ##Text Editor

    sudo apt-get install kwrite emacs

  ##IRC Client
    
    sudo apt-get install konversation

  ## Multimedia
  
    sudo apt-get install vlc banshee juk easytag soundkonverter 
    sudo apt-get install kffmpegthumbnailer kdegraphics-thumbnailers kdesdk-thumbnailers
    
  ## Random
  
    sudo apt-get install plasma-scriptengine-python redshift plasma-widget-redshift plasma-widget-smooth-tasks plasma-widget-homerun-kicker libreoffice-style-sifr
    
  ## Wine
  
    sudo apt-get install wine
    
  ## Qt
    
    sudo apt-get install qtdeclarative5-examples qtdeclarative5-dev qmlscene qtcreator
    
  ## Ksuperkey
  
    sudo add-apt-repository ppa:mehanik/ksuperkey
    sudo apt-get update
    sudo apt-get install ksuperkey
    ksuperkey -e 'Super_L=Alt_L|F2'
    
  ## owncloud
  
    sudo sh -c "echo 'deb http://download.opensuse.org/repositories/isv:/ownCloud:/desktop/xUbuntu_14.04/ /' >> /etc/apt/sources.list.d/owncloud-client.list"
    sudo apt-get update
    sudo apt-get install owncloud-client
    
    wget http://download.opensuse.org/repositories/isv:ownCloud:desktop/xUbuntu_14.04/Release.key
    sudo apt-key add - < Release.key
    
    
#Bumblebee

  sudo apt-get install bumblebee bumblebee-nvidia primus linux-headers-generic
  
  https://wiki.ubuntu.com/Bumblebee
  
#Hibernation

  /etc/polkit-1/localauthority/50-local.d/com.ubuntu.enable-hibernate.pkla
  
  [Re-enable hibernate by default in upower]
  Identity=unix-user:*
  Action=org.freedesktop.upower.hibernate
  ResultActive=yes

  [Re-enable hibernate by default in logind]
  Identity=unix-user:*
  Action=org.freedesktop.login1.hibernate
  ResultActive=yes
  
  http://blog.mafr.de/2014/05/01/enabling-hibernate-support-in-ubuntu-14-04/

