# Battery Threshold

Scripts to set the battery charge threshold automatically for my ASUS laptops.

Reference: <https://wiki.archlinux.org/title/Laptop/ASUS#Battery_charge_threshold>.

Usage:

```sh
cp battery-threshold.service /etc/systemd/system/battery-threshold.service
systemctl enable battery-threshold
```

Some commands for ASUS battery management:

```sh
cat /sys/class/power_supply/BAT0/status
cat /sys/class/power_supply/BAT0/capacity
cat /sys/class/power_supply/BAT0/charge_control_end_threshold
echo 60 > /sys/class/power_supply/BAT0/charge_control_end_threshold
```
