# domoticz-bluetooth-ping
Bluetooth device ping (l2ping) python plugin for Domoticz
Plugin is based on Xorfor's MAC presence
## ONLY TESTED FOR Raspberry Pi
## please note the new version requiring 2 additional installations below (python-bluez and pybluez)!!!

This Domoticz Python Plugin scans bluetooth for the existance of the specified bluetooth mac addresses.
## Prerequisites
You need the latest beta version of Domoticz for the best support of Python plugins and `l2ping` to use this plagin. This tool can be installed by:
```bash
sudo apt-get install -y bluez
sudo pip3 install pybluez
sudo apt-get install -y python-bluez
cd ~/domoticz/plugins
git clone https://github.com/heggink/domoticz-bluetooth-ping
# downloads the plugin into your plugins folder
# restart domoticz:
sudo service domoticz.sh restart
# from the domoticz interface: hardware -> add new hardware -> Bluetooth address presence
```
## Parameters
| Parameter | Description |
| :--- | :--- |
| **MAC address** | Single bluetooth MAC address in de format xx:xx:xx:xx:xx:xx |
| **Minutes between check** | Polling time in minutes to check for the presence of the specified mac addresses |
| **Minutes for timeout** | Switch off the device when after this specified number of minutes, none of the mac addresses is found |
## Devices
| Name | Description |
| :--- | :--- |
| **BTH device** | A switch indicating whether one of the specified mac adresses was seen on the Domoticz network |

## To do
