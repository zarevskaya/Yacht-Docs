---
title: ARM
description: Arm Caviats
hide_table_of_contents: true
id: ARM
---

## Memory support in graphs
If you're on arm and graphs aren't showing up add the following to your cmdline.txt:

```
sudo nano /boot/cmdline.txt
```

     ```
Add: cgroup_enable=cpuset cgroup_enable=memory cgroup_memory=1
     ```
like this: console=serial0,115200 console=tty1 root=PARTUUID=xxxxxx rootfstype=ext4 fsck.repair=yes rootwait cgroup_enable=cpuset cgroup_enable=memory

Then, reboot:

```
sudo reboot
```

