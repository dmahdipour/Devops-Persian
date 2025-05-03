v### Logical Partition Management
Resize partition based on physical resize.  Partition types':
* **PV** (Physical Volume): Partitions   
* **LV** (Logical Volume): A Layer above PV -> ex. divide 3 PV in 2 MV
* **VG** (Volume Group): List of Logical Volumes

```shell
sudo pvs
sudo lvs
sudo vgs
```
**Note:** When we add VG, a new disk will be added. Then we can divide it to partitions.

```shell
sudo apt install bash-completion
```

### Steps to extend a partition size
Example: "ubuntu--vg-ubuntu--lv" is / partition and sdb is second disk was added.
```shell
1) Add a new Hard Disk
2) sudo fdisk /dev/sdb
	1) g
	2) n (+30G) -> n (+20G)
	3) t (1 -> 30)   -> t (2 -> 30)
	4) w
3) sudo vgextend ubuntu-vg /dev/sdb1                    #Extend Volume Group
4) sudo lvextend /dev/ubuntu-vg/ubuntu-lv /dev/sdb1     #Extend Logical Volume
5) sudo resize2fs   /dev/mapper/ubuntu--vg-ubuntu--lv   #Resize Logical Volume
6) sudo mkfs.ext4 /dev/sdb2                       #Change partition filesystem of second partition
7) sudo vim /etc/fstab -> i > /dev/sdb2 /mnt ext4 defaults 0 0 -> Esc -> :wq        #Add record to fstab for remounting after boot automatically
8) sudo mount -a        #Mount all partition based on fstab file
```