# Restore RS3621 Fan Speed

<a href="https://github.com/007revad/Restore_RS3621_Fan_Speed/releases"><img src="https://img.shields.io/github/release/007revad/Restore_RS3621_Fan_Speed.svg"></a>
![Badge](https://hitscounter.dev/api/hit?url=https%3A%2F%2Fgithub.com%2F007revad%2FRestore_RS3621_Fan_Speed&label=Visitors&icon=github&color=%23198754&message=&style=flat&tz=Australia%2FSydney)
[![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://www.paypal.com/paypalme/007revad)
[![](https://img.shields.io/static/v1?label=Sponsor&message=%E2%9D%A4&logo=GitHub&color=%23fe8e86)](https://github.com/sponsors/007revad)
<!--- [![committers.top badge](https://user-badge.committers.top/australia/007revad.svg)](https://user-badge.committers.top/australia/007revad) --->

### Description

Script to restore RS3621xs+ and RS3621RPxs Quiet mode and Cool mode fan speeds back to how it was before DSM 7.3.2

When you run the script it:
1. Creates a backup of /var/etc.defaults/scemd.xml if no backup exists.
2. Checks if /var/etc.defaults/scemd.xml contains the new DSM 7.3.2 fan speeds.
3. Edits /var/etc.defaults/scemd.xml to the previous DSM 7.3.1 fan speeds if it contains the new DSM 7.3.2 fan speeds.

So it is safe to run the script again, or have it scheduled to run at boot-up, as it will only edit scemd.xml if needed.

### Download the script

1. Download the latest version _Source code (zip)_ from https://github.com/007revad/Restore_RS3621_Fan_Speed/releases
2. Save the download zip file to a folder on the Synology.
3. Unzip the zip file.

### To run the script via task scheduler

See [How to run from task scheduler](https://github.com/007revad/Restore_RS3621_Fan_Speed/blob/main/how_to_run_from_scheduler.md)

### To run the script via SSH

[How to enable SSH and login to DSM via SSH](https://kb.synology.com/en-global/DSM/tutorial/How_to_login_to_DSM_with_root_permission_via_SSH_Telnet)

```YAML
sudo -s /volume1/scripts/restore_rs3621_fan_speed.sh
```

**Note:** Replace /volume1/scripts/ with the path to where the script is located.

### Troubleshooting

If the script won't run check the following:

1. Make sure you download the zip file and unzipped it to a folder on your Synology (not on your computer).
2. If the path to the script contains any spaces you need to enclose the path/scriptname in double quotes:
   ```YAML
   sudo -s "/volume1/my scripts/restore_rs3621_fan_speed.sh"
   ```
3. Make sure you unpacked the zip or rar file that you downloaded and are trying to run the restore_rs3621_fan_speed.sh file.
4. Set the script file as executable:
   ```YAML
   sudo chmod +x "/volume1/scripts/restore_rs3621_fan_speed.sh"
   ```

### Screenshots

<!--- <p align="center">Script output on first run</p> --->
<p align="center"><img src="/images/1st_run.png"></p>

<!--- <p align="center">Script output if run again</p> --->
<p align="center"><img src="/images/2nd_run.png"></p>

<br>

<!--- <p align="center">Description of image 2 goes here</p> --->
<p align="center"><img src="/images/IMAGE_NAME.png"></p>
