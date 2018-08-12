This script is intended as an automated universal snapshot tool used with either [own-backup](https://github.com/m-k-r/own-backup) or cron.

It uses config files to define mode, names, timestamp format, intervalls and source with independant retention for each intervall.

It has a build in snapshot management and can be used with btrfs, zfs, kvm (qm), files, directories, mysql and postgresql.

zfs, btrfs, lxd and qm use their own tools, directories and files use rsync to copy and files, mysql and pgsql can be encrypted. They are encrypted on the source server before they are copied to the targetserver and disk.

### usage

**own-snapshot -e** $CONFIG **-f** $INTERVALL **-d** $DEBUG

**additional:**  
-c : **initial** config, **upgrade** elements, **rollback/cleanup** backups from upgrade   
-i : don't create new snapshots.  
-f : the frequency.  
-l : either date-string (list) or complete label (single).

Example configs can be found in the template directory.
