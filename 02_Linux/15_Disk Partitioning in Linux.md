### Partition Table
* **MBR (Master Boot Record):** First 512B is for BootLoader,  Up to 4 Primary Partitions (466B for Bootloader, 4x16B Partition Metadata for 4 Primary Partitions)
* **GPT (Guide Partition Table):** Up to 128 Primary Partitions, Can use more than 2TB Hard Disk

### File System Formats for Linux
* *ext2*
* *ext3*
* *ext4* -> more efficient performance especially for small but numerous files
* *xfs* -> Big data but less files

**Note:** After booting, Linux read <u>/etc/fstab</u> file to get which partition is for which job. It is better to have UUID for each partition. 

### INODE (Index Node)
The Index of what saved where in Partitoins. It has limit count (Not volume), so you will see out of space errors when the count limitation is reached. 

**Note:** Use <u><i>df -h</i></u> for get partitions volumes and info.

### Dispractice
All partitions are sub-partition of /. We can just have it but it is not good. We have to separate all partitions that can have side-effects on each others ex. **boot**(2 GB), **/**(LVM: 30~50 GB), **var**(LVM: Logs place) and **/home** if use in Desktop mode.

Other partitions is used for:
* **etc:** Saving configuration files
* **mnt:** Mount other partitions and disks
* **opt:** Build application and dependencies
* **bin - sbin:** Commands list
