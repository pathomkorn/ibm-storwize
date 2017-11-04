# Drive Firmware Update

* Reference
https://www.ibm.com/support/knowledgecenter/STLM5A_7.8.1/com.ibm.storwize.v3700.781.doc/tbrd_upgradedrivefirmware.html

* Upload Drive Firmware
```bash
pscp IBM2072_DRIVE_20170901 superuser@storwize:/home/admin/upgrade
```

* Show Drive Firmware
```bash
IBM_Storwize:storwize:superuser>lsdrive 0
id 0
status online
...
firmware_level B56U
...
```

* Apply Drive Firmware
```bash
IBM_Storwize:storwize:superuser>applydrivesoftware -file /tmp/IBM2072_DRIVE_20170901 -type firmware -drive 0
```
