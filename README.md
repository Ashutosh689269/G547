# G547
Using insmod, load the driver dof.ko. On 512 KB of RAM, block device files 
representing the disc would be created, with two major partitions. 
• Examine the /dev/dof* block device files that were produced automatically. 
The full disc, which is 512 KB in size, is represented by /dev/dof. The 
principal partitions are dof1 and dof2. 
• Using the disc dump utility dd, read the whole disc (/dev/dof). 
• Using dd, zero off the first sector of the disk's first partition 
(/dev/dof1). 
• Using cat, enter some text into the disk's first partition (/dev/dof1). 
• The xxd software may be used to display the contents of the first 
partition (/dev/dof1). For xxd output, check the log. 
• Display the information about the partitions on the CD using fdisk. The log 
contains the output of fdisk. 
• Using mkfs.vfat, quickly format the second primary partition (/dev/dof2) 
into a vfat filesystem (like your pen drive). 
• Use mount to mount the freshly formatted partition at /mnt, for example. 
• According to the disc utilisation utility df, this partition is now 
mounted at /mnt. There is space to store files there. 
• After unmounting the partition with umount /mnt, unload the 
driver using rmmod dof. The whole contents of the disc will be 
erased.
