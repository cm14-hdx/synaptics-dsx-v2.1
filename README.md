**IMPORTANT:** The process here is for apollo
**IMPORTANT:** Use the thor firmware if you have that device

# Requirements:

1. synaptics_fw_updater
2. Synaptics.3.B.apollo.img from the kernel source
3. Reboot into recovery (twrp)


# Method: (This works using linux)

1. Push synaptics_fw_updater to /data

```
adb push synaptics_fw_updater /data
```

2. Push firmware to /data

```
adb push Synaptics.3.B.apollo.img /data
```

3. Change permissions of synaptics_fw_updater

```
adb shell
cd /data
chmod 777 synaptics_fw_updater
```

4. Flash the firmware

```
./synaptics_fw_updater -v -f -b Synaptics.3.B.apollo.img
```

5. Reboot and voila touchscreen should be good.
