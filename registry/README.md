## Create registry directory to keep your images
mkdir /registry

## Note: it's recommended to add another disk and mount it in fstab as persistent volume
vim /etc/fstab
/dev/sdb1                               /registry       xfs     defaults        0 0
