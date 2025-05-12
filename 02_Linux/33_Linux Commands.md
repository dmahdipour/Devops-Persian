Based on your usage you have to learn new commands.
```shell
vmstat            #Check memory state 
iotop             #Check whtich proces use more IO
tar -czvf FILENAME.tar.gz DIRECTORY   #Compress Dirs
file FILENAME     #Display info about a file
#Copy all iso file or partition data to another one bit-by-bit, Be careful about input and output path
dd if=INPUT_FILE_PATH of=OUTPUT_FILE_PATH.img
watch ll .        #Execute ex. ll command each 2 seconds
which ll          #Display if there is ex. ll command or not
wheris ll         #Display path of ex. ll command
whatis ll         #Display detailed info about ex. ll command
man ll            #Display manual of ex. ll command
info ll           #Display manual of ex. ll command
uname -a          #All info about OS
lsb_release -a    #Info OS version 
env               #Display global environment variables
ulimit -a         #Display lots of info about cpu time, process, file licker, etc.
#If you have trouble with yout Os, you can plug it into other pc and by chroot you can use partition of it as local partition and repair it.
chroot
lsmod             #Display status of modules in Linux Kernel
lspci             #Display List of PCI devices
lsusb             #Display List of USB devices
htpasswd          #Manage user file for basic authentication
nmap              #Network exploration tool and security / port scanner
zenmap            #GUI form of nmap
opessl            #Working by certificates
```

**Note:** Read Linux in action Book