# Wifi-Monitoring-and-Linux-Commands
How to Install Wavemon

This command to install wavemon :

    sudo apt-get install -y wavemon
    
You can run Wavemon from the command line after the Pi has booted or from within a LXTerminal :

    wavemon
    
note : this software use for single band frequency, i havent before make arithmatic some dual band of antenna. This program has to check the signal strength on dBm your antenna wireless

F2 displays a graph of you signal levels. The graph below was created using the “random data” means that the signal strength of frequency is fluctuate, if you have monitoring the signal strength you have a calculate the average of value of wave

F2 displays a graph of you signal levels. The graph below was created using the “random data” 

F7 displays the preferences page. These can be left at the default values but I changed the “override scale autodetect” to “on” and increased the signal level maximum to 30dBm.

The configuration file located in :

    /home/pi/.wavemonrc
    
and can be edit directly on this command :

    sudo nano .wavemonrc
    
# WiFi Tools for Raspberry Pi

List of Commands for Wifi Monitoring/Troubleshooting

iwconfig manipulate the basic wireless parameters

iwlist allow to initiate scanning and list frequencies, bit-rates, encryption keys...

iwspy allow to get per node link quality

iwpriv allow to manipulate the Wireless Extensions specific to a driver (private)

ifrename allow to name interfaces based on various static criteria

To scan your network SSID

    $ sudo iwlist wlan0 scan
    
iwconfig command is similar to ifconfig command, but is dedicated to the Linux wireless interfaces. It is used to manipulate the basic wireless parameters such as ssid, mode, channel, bit rates, encryption key, power and much more.

    $ iwconfig
    
    returns
    
    lo no wireless extensions.
    eth0 no wireless extensions.
    
This command to check your wifi card :

    $ iwconfig wlan0
    
See link quality continuously on screen

    $ cat /proc/net/wireless
    $ watch -n 1 cat /proc/net/wireless
    
 To scan your environment for available networks, do the following:
 
    $ sudo iwlist wlan0 scan
    
First, set the essid, which identifies the network access point you want:

    $ sudo iwconfig wlan0 essid network-essid
    
Refference : http://www.raspberrypi-spy.co.uk/2014/10/how-to-use-wavemon-to-monitor-your-wifi-connection/
http://www.linuxjournal.com/content/wi-fi-command-line
http://www.cyberciti.biz/tips/linux-find-out-wireless-network-speed-signal-strength.html
https://blog.adafruit.com/2014/10/31/wavemon-handy-command-line-utility-for-monitoring-your-raspi-wifi-connection-piday-raspberrypi-raspberry_pi/
