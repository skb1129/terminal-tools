# Terminal Tools :

### Create a bootable DD USB Drive :
- `sudo fdisk -l` to list all partitions.
- Find your drive in the list. EX - `/dev/sdb1`.
- `sudo umount /dev/sdb1` to unmount the drive.
- `sudo dd bs=4M if=input.iso of=/dev/sdb` to create the DD.
- `sync` to sync drive data again.
- `sudo eject /dev/sdb` eject the completed drive.
- Now the USB Drive is ready to use.
