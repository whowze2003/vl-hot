vl-hot is a purely udev based automount system for any kind of pluggable storage device that conforms to the block device specification and so uses scsi emulation. It was officially included in Vector Linux 5.1 SOHO and subsequent releases. Hardware known to work with vl-hot are USB pendrives, hard disks, digital cameras and memory card readers, PCCARD (or PCMCIA) memory cards and drives; Firewire devices should work, but there are no user reports on this kind of hardware yet.

A graphical configurator utility (vl-hot-config) is included.

NOTE: This project will be renamed vxmount for the release of VectorLinux 6.0
http://code.google.com/p/vxmount/

![http://www.image-upload.net/files/5316/websitepics/vxmount/vl-hot-config-104.png](http://www.image-upload.net/files/5316/websitepics/vxmount/vl-hot-config-104.png)

Working specifications of vl-hot:
  * The mount base directory will be "/mnt/vl-hot/".
  * Each drive will have a "sd?" directory (where "?" represents a letter of the alphabet).
  * Each mounted partition will have a "vol#" directory (where "#" represents a number) within the drive directory. An exception to this rule is in the case of non-MBR devices, where there is no partition table.
  * Desktop icons are dynamically created/deleted. In KDE these have unmount options in the context (right-click) menu.  There is a choice of conventional unmount (recommended), as well as unmount with signalling (sends SIGHUP to the process that is holding open the mount) and unmount with kill (sends SIGKILL). The last two should be tried in that order, only when the normal unmount fails. In XFCE there is a separate unmount icon due to limitations in the actions support in this desktop environment.
  * The unmount operation has completed succesfully once the desktop icon dissapears.