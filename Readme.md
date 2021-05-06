# Firmware Release Notes

## S5Z42109 (03-30-2021)

### This firmware provides the following

- Fixed an issue that might cause the drive to become unresponsive on Linux systems
- Fixed a compatibility issue with the Asus Armoury Crate tool

### Instructions

1. Ensure linux distribution has latest ```nvme-cli``` installed
2. Gain root access ```sudo -s```
3. Copy the binary zip file attached into a local directory
4. Extract the zip file that contains the firmware binary
5. Execute ```fw-download``` command to prestage the firmware for commit. Note: Use the ```S5Z42109.bin``` binary file

```
nvme fw-download /dev/nvme[device] --fw=[S5Z42109.bin]
```

6. Activate the firmware

```
nvme fw-activate /dev/nvme[device] --slot=1 --action=1
```

7. Reboot the system
8. Issue the following command to verify that the firmware is committed

```
nvme id-ctrl /dev/nvme[device]
```

### Disclaimer

KINGSTON EXPRESSLY DISCLAIMS ALL SUCH WARRANTIES OF ANY KIND, WHETHER EXPRESS, IMPLIED OR STATUTORY, WITH RESPECT TO THE FIRMWARE AND FIRMWARE UPDATES INCLUDING, WITHOUT LIMITATION, WARRANTIES OR CONDITIONS OF QUALITY, PERFORMANCE, NON-INFRINGEMENT, MERCHANTABILITY, OR FITNESS FOR USE FOR A PARTICULAR PURPOSE.

KINGSTON DOES NOT REPRESENT OR WARRANT THAT THE FIRMWARE OR FIRMWARE UPDATES WILL ALWAYS BE AVAILABLE, ACCESSIBLE, UNINTERRUPTED, TIMELY, SECURE, ACCURATE, COMPLETE OR ERROR-FREE, INCLUDING BUT NOT LIMITED TO THE ACCURACY OR COMPLETENESS OF ANY INFORMATION, TEXT, GRAPHICS, LINKS OR OTHER ITEMS CONTAINED WITHIN THE FIRMWARE.
