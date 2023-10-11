# Install Arch
A guide to install Arch Linux using the `archinstall` script.

## Partitioning Drive
This step can be skipped if not dual booting

**Partitions required**
- /boot \[FAT32] ~ 1GiB
- /root \[ext4 or btrfs]
- swap space (optional)
#### Making the Partitions
1. Locate the drive to partition
```
lsblk
```
Look for the drive that you want to partition. Usually `sda` or `nvme0`

2.  Go to the partition Utility
```
cfdisk /dev/<drive_name>
```

3.  Create the Required Partitions
- Navigate to the `Free space` partition, or delete existing partitions to create Free space.
- Select `[New]` and enter the partition size at the prompt. Eg. 4G for 4GiB
- Select `[Type]` to select the partition type.
	- Linux filesystem for /root
	- EFI system for /boot
	- Linux swap for swap space
4. Confirm the partition by selecting `[Write]` and confirming by typing yes.

## Mounting Partitions

Locate the newly created partitions with 
```
lsblk
```
Note the names of the EFI, swap and root partitions
### Format the partitions with File Systems
**Root Partition**
```
mkfs.ext4 /dev/<root_partition_name>
```

**Boot Partition**
```
mkfs.fat -F32 /dev/<boot_partition_name>
```

**Swap space**
```
swapon /dev/<swap_partition_name>
```

### Mounting the Partitions

**Root partition**
```
mount --mkdir /dev/<partition_name> /mnt/archinstall
```

**Boot partition**
```
mount --mkdir /dev/<boot_partition_name> /mnt/archinstall/boot
```

## Connect to Wi-fi
```
iwctl
```
You should be in the iwctl cli

## ArchInstall Script

 