### 1. Попасть в систему без пароля несколькими способами
#### debian 8
* Дописываем в загрузчике grub2 в строке linux16 `init=/bin/sh` данное выражение (`init=/sysroot/bin/sh`) не заработало на centos 7 
* `mount -o remount, rw /`
* `passwd root`
* `exec /sbin/init`

![debian8_init](https://github.com/kyourselfer/OTUS_LinuxAdmin201804/blob/master/lesson4_boot/debian8_init_.jpeg)
![debian8_init_sys](https://github.com/kyourselfer/OTUS_LinuxAdmin201804/blob/master/lesson4_boot/debian8_init_sys_.jpeg)

* Дописываем в загрузчике grub2 в строке linux16 `systemd.debug-shell=1`
* passwd root

![debian8_systemd.debug-shell](https://github.com/kyourselfer/OTUS_LinuxAdmin201804/blob/master/lesson4_boot/debian8_systemd.debug-shell.jpeg)
![debian8_systemd.debug-shell_sys](https://github.com/kyourselfer/OTUS_LinuxAdmin201804/blob/master/lesson4_boot/debian8_systemd.debug-shell_sys.jpeg)

#### centos 7
* Дописываем в загрузчике grub2 в строке linux16 `systemd.debug-shell=1 selinux=0`
* `passwd root`

![centos7_systemd.debug-shell](https://github.com/kyourselfer/OTUS_LinuxAdmin201804/blob/master/lesson4_boot/centos7_systemd.debug-shell.jpeg)
![centos7_systemd.debug-shell_sys](https://github.com/kyourselfer/OTUS_LinuxAdmin201804/blob/master/lesson4_boot/centos7_systemd.debug-shell_sys.jpeg)

