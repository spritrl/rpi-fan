#!/usr/bin/env python
# released under the GNU General Public License version 3.0 (GPLv3)

import io 
import RPi.GPIO as GPIO
import time

pin = int(2) #Your GPIO Pin
tempMax = 45.0 #Your Temp max
i = int(0)

GPIO.setmode(GPIO.BCM)
GPIO.setup(pin, GPIO.OUT)

while True: 
	dir = open("/sys/class/thermal/thermal_zone0/temp", "r")
	temp = float( dir.readline ())
	temp = temp/1000
	
	print "Tour : ",+i

	if i>1 :
		print(temp)
		i=0

	if temp > tempMax:
		GPIO.output(pin, 1)
		print "ON"
		time.sleep(60.0)
	else:
			GPIO.output(pin, 0)
			print "OFF"	
	i = i+1
	time.sleep(30.0)
