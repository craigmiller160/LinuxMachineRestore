# Mounting Drives

To mount the two important drives, do the following:

## Get List of Disks

Use the following command to get a list of all available disks. Then identify `MediaDrive` based on its 7.3TB size and `OtherDrive` based on its 1.8TB size. The specific thing that's needed is the partition address, ie `/dev/sdd1`. The numbered part is important.

```
sudo fdisk -l
```

## Get the Disk UUID

Use the following command to get the UUID of the disk. Replace the disk name with the appropriate one.

```
sudo blkid /dev/sdd1
```

## Create the directories

Use these commands to create the directories to mount the drives to:

```
mkdir /home/craig/MediaDrive
mkdir /home/craig/OtherDrive
```

## Update Fstab

Edit the `/etc/fstab` file to mount the drives. Put the following two lines in it, changing the UUIDs to match the correct ones:

```
UUID=52B2859EB2858767 /home/craig/MediaDrive ntfs-3g nls-utf8,permissions,users,auto,locale=en_US.utf8 0 2
UUID=32BA86B2BA8671E1 /home/craig/OtherDrive ntfs-3g nls-utf8,permissions,users,auto,locale=en_US.utf8 0 2
```