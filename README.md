# Temperature Probe
 DS18B20 temperature probe to raspi data logger

# Wiring for SSH output
DAT -> GPIO 7
VCC -> GPIO 1
GND -> GPIO 6

# Enable one-wire
sudo nano/boot/config.txt
dtoverlay=w1-gpio
sudo reboot

sudo modprobe w1-gpio
sudo modprobe w1-therm
cd /sys/bus/w1/devices
ls
cd <THERM-ADDRESS>
cat w1_slave
cd

# Run basic temperature output program temp.py

sudo python temp.py
prints (C, F) once/second