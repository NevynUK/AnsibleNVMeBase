# Ansible Variables

<i>all.yml</i> contains the variable definitions that will be applied to all of the scripts. The variables are as follows:

```yaml
---
default_user: clusteruser
nvmebase_mount_point: nvme0
format_nvmebase: false
```

## default_user: clusteruser

Name of the default user for the device.  This is used as part of the Samba installation.

## nvmebase_mount_point: nvme0

This is the name of the mount point for the NVMe drive.

## format_nvmebase: false

This determines if the NVMe drive should be formatted (have a new file system created on the drive) as part of the installation process.

Set this to <i>true</i> for new drives (or drives where the data is to be discarded.  Set this to <i>false</i> to preserve the contents of the drive.

Setting <i>format_nvmebase</i> to <i>false</i> for an unformatted (new) drive will cause the <i>ConfigureNVMeBase.yml</i> script to fail.
