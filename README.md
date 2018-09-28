# RPI-FAN
 Fan automation on RPi with GPIO
 
# Installation
### 1. Before : <br/>
```
sudo apt-get update && sudo apt-get -y upgrade
```
<br/>

### 2. Package :<br/>
Note : in /home/pi/ if you want to run the script in the background
```
git clone https://github.com/spritrl/rpi-fan/
```
<br/>

### 3. To run the script in the background :<br/>
* Execute :
```
sudo nano /etc/init.d/rpi-fan
```
* Past :
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
 sudo python /home/pi/rpi-fan/rpi-fan.py &
 ```
 * Do :
 ```
sudo chmod +x /etc/init.d/rpi-fan
 ```
 * And :
 ```
sudo update-rc.d rpi-fan defaults
 ```
# Reboot and Enjoy
