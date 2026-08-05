# System Information

## Linux Distribution
Ubuntu 24.04 LTS

## Kernel Version
asarmiento@ubuntu:~$ uname -r
6.8.0-136-generic

## CPU Information
asarmiento@ubuntu:~$ lscpu
Architecture:          x86_64
CPU op-mode(s):        32-bit, 64-bit
Address sizes:         39 bits physical, 48 bits virtual
Byte Order:            Little Endian
CPU(s):                1
On-line CPU(s) list:   0
Vendor ID:             GenuineIntel
Model name:            Intel Xeon E312xx (Sandy Bridge, IBRS update)
CPU family:            6
Model:                 42
Thread(s) per core:    1
Core(s) per socket:    1
Socket(s):             1
Stepping:              7
BogoMIPS:              7000.00
Flags:                 fpu vme de pse tsc ...
Vulnerability Gather data sampling: Not affected
Indirect branch speculation: Mitigation
L1TF: Mitigation
MDS: Mitigation
Meltdown: Mitigation
Retbleed: Not affected
Spec store bypass: Mitigation
Spectre v1: Mitigation
Spectre v2: Mitigation
SRBDS: Not affected
TSX async abort: Not affected

## Total Memory
asarmiento@ubuntu:~$ free -h

               total   used   free   shared  buff/cache  available
Mem:           1.9Gi  452Mi  374Mi   1.1Mi      825Mi      1.4Gi
Swap:          1.0Gi     0B   1.0Gi

## Available Disk Space
asarmiento@ubuntu:~$ df -h

Filesystem      Size  Used  Avail  Use%  Mounted on
tmpfs           191M  1012K 190M    1%   /run
/dev/vda1       19G   5.4G   13G   30%   /
tmpfs           952M   84K  952M    1%   /dev/shm
tmpfs           5.0M     0  5.0M    0%   /run/lock
/dev/vda16      881M  117M 703M    15%   /boot
/dev/vda15      105M  6.2M  99M     6%   /boot/efi
tmpfs           191M  8.0K 191M     1%   /run/user/1001
