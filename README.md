### Building

### Booting
The generated images are EFI enabled and wont boot under legacy bios

Here is a sample command line using [virt-install]

  sudo apt install virtinst
  virt-install --name myhost --memory 512 --disk <disk> --boot uefi --graphics none

To remove the VM

  virsh destroy myhost
  virsh undefine myhost --nvram

### Boot logs

  ❯ virt-install --name host --memory 512 --disk host.22.10.qcow2 --boot uefi --graphics none
  WARNING  No operating system detected, VM performance may suffer. Specify an OS with --os-variant for optimal results.

  Starting install...
  Running text console command: virsh --connect qemu:///session console host
  Connected to domain 'host'
  Escape character is ^] (Ctrl + ])
  BdsDxe: loading Boot0001 "UEFI QEMU HARDDISK QM00001 " from PciRoot(0x0)/Pci(0x1,0x1)/Ata(Primary,Master,0x0)
  BdsDxe: starting Boot0001 "UEFI QEMU HARDDISK QM00001 " from PciRoot(0x0)/Pci(0x1,0x1)/Ata(Primary,Master,0x0)















                                      Ubuntu 22.10 (Kinetic Kudu)
                                    Reboot Into Firmware Interface

                                              Boot in 1 s.

  Welcome to Ubuntu 22.10!

  [  OK  ] Created slice Slice /system/getty.
  [  OK  ] Created slice Slice /system/modprobe.
  [  OK  ] Created slice Slice /system/serial-getty.
  [  OK  ] Created slice User and Session Slice.
  [  OK  ] Started Dispatch Password …ts to Console Directory Watch.
  [  OK  ] Started Forward Password R…uests to Wall Directory Watch.
  [  OK  ] Set up automount Arbitrary…s File System Automount Point.
  [  OK  ] Reached target Local Encrypted Volumes.
  [  OK  ] Reached target Local Integrity Protected Volumes.
  [  OK  ] Reached target Path Units.
  [  OK  ] Reached target Remote File Systems.
  [  OK  ] Reached target Slice Units.
  [  OK  ] Reached target Swaps.
  [  OK  ] Reached target Local Verity Protected Volumes.
  [  OK  ] Listening on fsck to fsckd communication Socket.
  [  OK  ] Listening on initctl Compatibility Named Pipe.
  [  OK  ] Listening on Journal Audit Socket.
  [  OK  ] Listening on Journal Socket (/dev/log).
  [  OK  ] Listening on Journal Socket.
  [  OK  ] Listening on Network Service Netlink Socket.
  [  OK  ] Listening on udev Control Socket.
  [  OK  ] Listening on udev Kernel Socket.
          Mounting Huge Pages File System...
          Mounting POSIX Message Queue File System...
          Mounting Kernel Debug File System...
          Mounting Kernel Trace File System...
          Starting Journal Service...
          Starting Create List of Static Device Nodes...
          Starting Load Kernel Module chromeos_pstore...
          Starting Load Kernel Module configfs...
          Starting Load Kernel Module drm...
          Starting Load Kernel Module efi_pstore...
          Starting Load Kernel Module fuse...
          Starting Load Kernel Module pstore_blk...
          Starting Load Kernel Module pstore_zone...
  [  OK  ] Finished Load Kernel Module ramoops.
  [  OK  ] Finished File System Check on Root Device.
  [  OK  ] Finished Load Kernel Modules.
  [  OK  ] Finished Generate network units from Kernel command line.
  [  OK  ] Reached target Preparation for Network.
          Mounting FUSE Control File System...
          Mounting Kernel Configuration File System...
  [  OK  ] Started File System Check Daemon to report status.
          Starting Remount Root and Kernel File Systems...
          Starting Apply Kernel Variables...
  [  OK  ] Mounted FUSE Control File System.
  [  OK  ] Mounted Kernel Configuration File System.
  [  OK  ] Finished Remount Root and Kernel File Systems.
          Starting Flush Journal to Persistent Storage...
          Starting Load/Save Random Seed...
          Starting Create System Users...
  [  OK  ] Finished Apply Kernel Variables.
  [  OK  ] Finished Load/Save Random Seed.
  [  OK  ] Finished Coldplug All udev Devices.
  [  OK  ] Finished Flush Journal to Persistent Storage.
  [  OK  ] Finished Create System Users.
          Starting Create Static Device Nodes in /dev...
  [  OK  ] Finished Create Static Device Nodes in /dev.
  [  OK  ] Reached target Preparation for Local File Systems.
          Starting Rule-based Manage…for Device Events and Files...
  [  OK  ] Started Rule-based Manager for Device Events and Files.
          Starting Network Configuration...
  [  OK  ] Started Network Configuration.
  [  OK  ] Found device /dev/ttyS0.
  [  OK  ] Found device QEMU_HARDDISK EFI.
          Mounting /boot/efi...
  [  OK  ] Mounted /boot/efi.
  [  OK  ] Reached target Local File Systems.
          Starting Create Volatile Files and Directories...
  [  OK  ] Finished Create Volatile Files and Directories.
          Starting Network Name Resolution...
          Starting Network Time Synchronization...
          Starting Record System Boot/Shutdown in UTMP...
  [  OK  ] Finished Record System Boot/Shutdown in UTMP.
  [  OK  ] Started Network Time Synchronization.
  [  OK  ] Reached target System Time Set.
  [  OK  ] Listening on Load/Save RF …itch Status /dev/rfkill Watch.
  [  OK  ] Started Network Name Resolution.
  [  OK  ] Reached target Network.
  [  OK  ] Reached target Host and Network Name Lookups.
  [  OK  ] Reached target System Initialization.
  [  OK  ] Started Daily apt download activities.
  [  OK  ] Started Daily apt upgrade and clean activities.
  [  OK  ] Started Daily dpkg database backup timer.
  [  OK  ] Started Periodic ext4 Onli…ata Check for All Filesystems.
  [  OK  ] Started Discard unused blocks once a week.
  [  OK  ] Started Daily Cleanup of Temporary Directories.
  [  OK  ] Reached target Timer Units.
  [  OK  ] Listening on D-Bus System Message Bus Socket.
  [  OK  ] Listening on OpenBSD Secure Shell server socket.
  [  OK  ] Reached target Socket Units.
  [  OK  ] Reached target Basic System.
          Starting D-Bus System Message Bus...
          Starting Remove Stale Onli…t4 Metadata Check Snapshots...
          Starting User Login Management...
          Starting Permit User Sessions...
  [  OK  ] Finished Permit User Sessions.
  [  OK  ] Started Getty on tty1.
  [  OK  ] Started Serial Getty on ttyS0.
  [  OK  ] Reached target Login Prompts.
  [  OK  ] Reached target Login Prompts.
  [  OK  ] Finished Remove Stale Onli…ext4 Metadata Check Snapshots.
  [  OK  ] Started D-Bus System Message Bus.
  [  OK  ] Started User Login Management.
  [  OK  ] Reached target Multi-User System.
  [  OK  ] Reached target Graphical Interface.
          Starting Record Runlevel Change in UTMP...
  [  OK  ] Finished Record Runlevel Change in UTMP.

  Ubuntu 22.10 host ttyS0

  host login: admin (automatic login)

  Welcome to Ubuntu 22.10 (GNU/Linux 5.19.0-29-generic x86_64)
                .-.
          .-'``(|||)
        ,`\ \    `-`.                    _  _        _
       /   \ '``-.   `                  | || |___ __| |_
     .-.  ,       `___:                 | __ / _ (_-<  _|
    (:::) : 22.10  ___                  |_||_\___/__/\__|
     `-`  `       ,   :
       \   / ,..-`   ,
        `./ /    .-.`                 Built by Graphiant QA
          `-..-(   )
                `-`
  Last login: Thu Jan 12 16:45:21 UTC 2023 on tty1
  admin@host:~$
