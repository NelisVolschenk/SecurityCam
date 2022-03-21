## Installing

Create two files on the boot partition:
1. ssh - This should be empty.
2. wpa_supplicant.conf which should contain the following
```
country=us
update_config=1
ctrl_interface=/var/run/wpa_supplicant

network={
 scan_ssid=1
 ssid="MyNetworkSSID"
 psk="Pa55w0rd1234"
}
```
3. SSH into your pi and run the following command:
```
curl -s https://raw.githubusercontent.com/ParagonIntegrations/SecurityCam/master/install.sh?$(date +%s) | sudo bash
```