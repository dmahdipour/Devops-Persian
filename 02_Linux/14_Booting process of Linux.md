### Linux boot steps:
* BIOS Load (Initial Hardware) or EFI (in newer versions, If there is)
* Boot Loader (1st sector): 
	* Load Kernel (Initial whole hardware, Call essential partition and Load systemd)
	* Use it for debugging and restoring login password -> ex: Grub, lido
