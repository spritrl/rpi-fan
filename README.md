# RPI-FAN
 Fan automation on RPi with GPIO
 
# Installation
1. Before : <br/>
```
sudo apt-get update && sudo apt-get -y upgrade
```
<br/>

2. Package :<br/>
```
git clone https://github.com/spritrl/rpi-fan/
```
<br/>

3. To run the script in the background :
*Execute :
```
sudo nano /etc/init.d/rpi-fan
```
*Past :

 ```
 #! /bin/sh
 ### BEGIN INIT INFO

 # Provides: rpi-fan
 # Required-Start: $remote_fs $syslog
 # Required-Stop: $remote_fs $syslog
 # Default-Start: S
 # Default-Stop: 
 # Short-Description: RPI-FAN
 # Description: Fan automation on RPi with GPIO

 ### END INIT INFO
 sudo python /home/pi/fan/rpi-fan.py &
 ```
