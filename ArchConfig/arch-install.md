Installing Arch Linux
=== 

# Prereq
## Virtualbox
- New
- Add Arch iso as a disk drive
- Enable EFI

# On First Boot
1. `
loadkeys dvorak
  `

2. Test EFI `
ls /sys/firmware/efi/efivars
  `

3. Test Internet `
ping google.com
  `
  https://wiki.archlinux.org/index.php/Network_configuration

4. `
timedatectl set-ntp true
`

# Partitioning
https://wiki.archlinux.org/index.php/Partitioning

- Use `
parted
`

* /dev/sda1 - 900 MB ext4 or fat32 partition for grub 
* /dev/sda2 - 100 MB EFI partition
* /dev/sda3 - Main
* /dev/sda4 - RAM swap space partition should be at end of disk. 8-16GB