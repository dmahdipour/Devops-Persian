### Commands for working with Disk
```shell
# -h make the commands Humanize (Display in GB or K means Thousand)
df              #Get disk info in Byte       
df -i           #Display INODE of each partition
lsblk           #Display Block list of partitions
blkid           #Display UUID list of partitions
ll  or  ls -al  #Display content of Dir and their info
du -sh          #Display real volume of current dir (Hiiden files are included)
ncdu             #Nice and Graphical view of du {sudo apt install ncdu}
fdisk /dev/sd*   #Work with disks and chanage their partitions
fdisk -l         #List of Partition and their info
mount PARTITION_LOCATION FOLDER_NAME_FOR_MOUNT
mkfs FILE_SYSTEM PARTITION_PATH  #Format partition
```

**Note:** After getting into fdisk, do this steps:
1) Create a new label -> g: GPT, o: MBR, etc.
2) Generic                   -> n: Add new Partition
3) Generic                   ->  t: Change a partition type -> ex. 30 for LVM
4) Save & Exit              -> w: Write table disk
