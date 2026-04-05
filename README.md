Обновление ядра  ОС Linux.

Описание домашнего задания
1) Запустить ВМ c Ubuntu.
2) Обновить ядро ОС на новейшую стабильную версию из mainline-репозитория.
3) Оформить отчет в README-файле в GitHub-репозитории.

Дополнительное задание:
•	Собрать ядро самостоятельно из исходных кодов.


- основные команды (с сокращенным выводом, если это требуется, иначе без вывода);

uname -r
6.8.0-107-generic

uname –p
x86_64

wget https://kernel.ubuntu.com/mainline/v6.18.20/amd64/linux-headers-6.18.20-061820-generic_6.18.20-061820.202603251312_amd64.deb

wget https://kernel.ubuntu.com/mainline/v6.18.20/amd64/linux-headers-6.18.20-061820_6.18.20-061820.202603251312_all.deb

wget https://kernel.ubuntu.com/mainline/v6.18.20/amd64/linux-image-unsigned-6.18.20-061820-generic_6.18.20-061820.202603251312_amd64.deb

wget https://kernel.ubuntu.com/mainline/v6.18.20/amd64/linux-modules-6.18.20-061820-generic_6.18.20-061820.202603251312_amd64.deb
	
sudo dpkg -i *.deb
alex@ubuntuserver:~/kernel$ sudo dpkg -i *.deb
Selecting previously unselected package linux-headers-6.18.20-061820.
(Reading database ... 174297 files and directories currently installed.)
Preparing to unpack linux-headers-6.18.20-061820_6.18.20-061820.202603251312_all.deb ...
Unpacking linux-headers-6.18.20-061820 (6.18.20-061820.202603251312) ...
Selecting previously unselected package linux-headers-6.18.20-061820-generic.
Preparing to unpack linux-headers-6.18.20-061820-generic_6.18.20-061820.202603251312_amd64.deb ...
Unpacking linux-headers-6.18.20-061820-generic (6.18.20-061820.202603251312) ...
Selecting previously unselected package linux-image-unsigned-6.18.20-061820-generic.
Preparing to unpack linux-image-unsigned-6.18.20-061820-generic_6.18.20-061820.202603251312_amd64.deb ...
Unpacking linux-image-unsigned-6.18.20-061820-generic (6.18.20-061820.202603251312) ...
Selecting previously unselected package linux-modules-6.18.20-061820-generic.
Preparing to unpack linux-modules-6.18.20-061820-generic_6.18.20-061820.202603251312_amd64.deb ...
Unpacking linux-modules-6.18.20-061820-generic (6.18.20-061820.202603251312) ...
Setting up linux-headers-6.18.20-061820 (6.18.20-061820.202603251312) ...
Setting up linux-headers-6.18.20-061820-generic (6.18.20-061820.202603251312) ...
Setting up linux-modules-6.18.20-061820-generic (6.18.20-061820.202603251312) ...
Setting up linux-image-unsigned-6.18.20-061820-generic (6.18.20-061820.202603251312) ...
I: /boot/vmlinuz.old is now a symlink to vmlinuz-6.8.0-107-generic
I: /boot/initrd.img.old is now a symlink to initrd.img-6.8.0-107-generic
I: /boot/vmlinuz is now a symlink to vmlinuz-6.18.20-061820-generic
I: /boot/initrd.img is now a symlink to initrd.img-6.18.20-061820-generic
Processing triggers for linux-image-unsigned-6.18.20-061820-generic (6.18.20-061820.202603251312) ...
/etc/kernel/postinst.d/initramfs-tools:
update-initramfs: Generating /boot/initrd.img-6.18.20-061820-generic
/etc/kernel/postinst.d/zz-update-grub:
Sourcing file `/etc/default/grub'
Generating grub configuration file ...
Found linux image: /boot/vmlinuz-6.18.20-061820-generic
Found initrd image: /boot/initrd.img-6.18.20-061820-generic
Found linux image: /boot/vmlinuz-6.8.0-107-generic
Found initrd image: /boot/initrd.img-6.8.0-107-generic
Found linux image: /boot/vmlinuz-6.8.0-106-generic
Found initrd image: /boot/initrd.img-6.8.0-106-generic
Found linux image: /boot/vmlinuz-6.8.0-101-generic
Found initrd image: /boot/initrd.img-6.8.0-101-generic
Warning: os-prober will not be executed to detect other bootable partitions.
Systems on them will not be added to the GRUB boot configuration.
Check GRUB_DISABLE_OS_PROBER documentation entry.
Adding boot menu entry for UEFI Firmware Settings ...
done

 ls -al /boot
linux-headers-6.18.20-061820_6.18.20-061820.202603251312_all.deb
linux-headers-6.18.20-061820-generic_6.18.20-061820.202603251312_amd64.deb
linux-image-unsigned-6.18.20-061820-generic_6.18.20-061820.202603251312_amd64.deb
linux-modules-6.18.20-061820-generic_6.18.20-061820.202603251312_amd64.deb

sudo shutdown -r now

uname -r
6.18.20-061820-generic
