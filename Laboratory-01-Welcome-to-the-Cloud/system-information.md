# ================================ System Information ================================
=======================================================================================
rcontawe@ubuntu:~$ cat /etc/os-release
PRETTY_NAME="Ubuntu 24.04.4 LTS"
NAME="Ubuntu"
VERSION_ID="24.04"
VERSION="24.04.4 LTS (Noble Numbat)"
VERSION_CODENAME=noble
ID=ubuntu
ID_LIKE=debian
HOME_URL="https://www.ubuntu.com/"
SUPPORT_URL="https://help.ubuntu.com/"
BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"
PRIVACY_POLICY_URL="https://www.ubuntu.com/legal/terms-and-policies/privacy-policy"
UBUNTU_CODENAME=noble
LOGO=ubuntu-logo
=======================================================================================
rcontawe@ubuntu:~$ uname -r
6.8.0-136-generic
=======================================================================================
rcontawe@ubuntu:~$ lscpu | grep "Model name"
Model name:                              Intel Xeon E312xx (Sandy Bridge, IBRS update)
=======================================================================================
rcontawe@ubuntu:~$ free -h
               total        used        free      shared  buff/cache   available
Mem:           1.9Gi       429Mi       845Mi       1.1Mi       796Mi       1.4Gi
Swap:          1.0Gi          0B       1.0Gi
=======================================================================================
rcontawe@ubuntu:~$ df -h
Filesystem      Size  Used Avail Use% Mounted on
tmpfs           191M 1012K  190M   1% /run
/dev/vda1        19G  5.4G   13G  30% /
tmpfs           952M   84K  952M   1% /dev/shm
tmpfs           5.0M     0  5.0M   0% /run/lock
/dev/vda16      881M  117M  703M  15% /boot
/dev/vda15      105M  6.2M   99M   6% /boot/efi
tmpfs           191M  8.0K  191M   1% /run/user/1001
rcontawe@ubuntu:~$ 
