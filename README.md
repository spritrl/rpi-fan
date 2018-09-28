# RPI-FAN
 Fan automation on RPi with GPIO
 
# Installation
1. Before : <br/>
<code>sudo apt-get update && sudo apt-get -y upgrade</code>
<br/>

2. Package :<br/>
<code>git clone https://github.com/spritrl/rpi-fan/</code>
<br/>
sudo nano /etc/init.d/rpi-fan

<code>#! /bin/sh
<code>### BEGIN INIT INFO

<code># Provides: rpi-fan
<code># Required-Start: $remote_fs $syslog
<code># Required-Stop: $remote_fs $syslog
<code># Default-Start: S
<code># Default-Stop: 
<code># Short-Description: RPI-FAN
<code># Description: Fan automation on RPi with GPIO

<code>### END INIT INFO
sudo python /home/pi/fan/rpi-fan.py &</code>
