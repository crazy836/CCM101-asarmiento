# Checkpoint 7 – Linux Investigation

## Linux Server Investigation

For this checkpoint, I launched a Linux environment using the KillerCoda Playground. I used different Linux commands to identify the operating system, CPU information, memory, and available disk space.

## 1. Operating System

I used the following command:

```bash
cat /etc/os-release
```

The command shows information about the Linux operating system installed on the server.

**My Result:**

### root@ubuntu:~$ cat /etc/os-release 
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

---

## 2. CPU Information

I used:

```bash
lscpu
```

This command displays information about the processor, including the CPU architecture, number of CPUs, cores, and other details.

**My Result:**

root@ubuntu:~$ lscpu
Architecture:                x86_64
  CPU op-mode(s):            32-bit, 64-bit
  Address sizes:             39 bits physical, 48 bits virtual
  Byte Order:                Little Endian
CPU(s):                      1
  On-line CPU(s) list:       0
Vendor ID:                   GenuineIntel
  BIOS Vendor ID:            Red Hat
  Model name:                Intel Xeon E312xx (Sandy Bridge, IBRS update)
    BIOS Model name:         RHEL-9.6.0 PC (Q35 + ICH9, 2009)  CPU @ 2.0GHz
    BIOS CPU family:         1
    CPU family:              6
    Model:                   42
    Thread(s) per core:      1
    Core(s) per socket:      1
    Socket(s):               1
    Stepping:                1
    BogoMIPS:                7008.00
    Flags:                   fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov 
                             pat pse36 clflush mmx fxsr sse sse2 syscall nx rdtscp lm const
                             ant_tsc rep_good nopl xtopology cpuid tsc_known_freq pni pclmu
                             lqdq ssse3 cx16 pcid sse4_1 sse4_2 x2apic popcnt tsc_deadline_
                             timer aes xsave avx hypervisor lahf_lm cpuid_fault pti ssbd ib
                             rs ibpb stibp tsc_adjust xsaveopt arat md_clear
Virtualization features:     
  Hypervisor vendor:         KVM
  Virtualization type:       full
Caches (sum of all):         
  L1d:                       32 KiB (1 instance)
  L1i:                       32 KiB (1 instance)
  L2:                        4 MiB (1 instance)
  L3:                        16 MiB (1 instance)
NUMA:                        
  NUMA node(s):              1
  NUMA node0 CPU(s):         0
Vulnerabilities:             
  Gather data sampling:      Not affected
  Indirect target selection: Mitigation; Aligned branch/return thunks
  Itlb multihit:             KVM: Mitigation: VMX unsupported
  L1tf:                      Mitigation; PTE Inversion
  Mds:                       Mitigation; Clear CPU buffers; SMT Host state unknown
  Meltdown:                  Mitigation; PTI
  Mmio stale data:           Unknown: No mitigations
  Reg file data sampling:    Not affected
  Retbleed:                  Not affected
  Spec rstack overflow:      Not affected
  Spec store bypass:         Mitigation; Speculative Store Bypass disabled via prctl
  Spectre v1:                Mitigation; usercopy/swapgs barriers and __user pointer saniti
                             zation
  Spectre v2:                Mitigation; Retpolines; IBPB conditional; IBRS_FW; STIBP disab
                             led; RSB filling; PBRSB-eIBRS Not affected; BHI Retpoline
  Srbds:                     Not affected
  Tsa:                       Not affected
  Tsx async abort:           Not affected
  Vmscape:                   Not affected


---

## 3. Memory

I used:

```bash
free -h
```

This command displays the total, used, and available memory of the Linux server.

**My Result:**

root@ubuntu:~$ free -h
               total        used        free      shared  buff/cache   available
Mem:           1.9Gi       427Mi       829Mi       1.1Mi       814Mi       1.4Gi
Swap:          1.0Gi          0B       1.0Gi


---

## 4. Disk Space

I used:

```bash
df -h
```

This command shows the disk space available on the Linux server, including the amount of storage that is used and available.

**My Result:**

root@ubuntu:~$ df -h
Filesystem      Size  Used Avail Use% Mounted on
tmpfs           191M  996K  190M   1% /run
/dev/vda1        19G  5.4G   13G  30% /
tmpfs           952M   84K  952M   1% /dev/shm
tmpfs           5.0M     0  5.0M   0% /run/lock
/dev/vda16      881M  117M  703M  15% /boot
/dev/vda15      105M  6.2M   99M   6% /boot/efi



---

# Cloud Migration

If this Linux server were migrated to the cloud, it could be hosted using virtual machine services from AWS, Microsoft Azure, or Google Cloud.

| Cloud Provider      | Service That Could Host the Linux Server | Why I Chose It                                                            |
| ------------------- | ---------------------------------------- | ------------------------------------------------------------------------- |
| **AWS**             | **Amazon EC2**                           | EC2 provides virtual machines that can run Linux operating systems.       |
| **Microsoft Azure** | **Azure Virtual Machines**               | Azure Virtual Machines can run Linux-based workloads in the cloud.        |
| **Google Cloud**    | **Compute Engine**                       | Compute Engine provides configurable virtual machines that can run Linux. |

## My Understanding

Based on my investigation, the Linux server could be migrated to any of the three major cloud platforms. **Amazon EC2, Azure Virtual Machines, and Google Compute Engine** can all provide virtual machines capable of running Linux.

As a college student, I think the main idea is that the physical or virtual Linux server does not necessarily have to remain on the original infrastructure. Its workload can be moved to a cloud virtual machine, where the organization can choose computing resources such as CPU, memory, storage, and networking.

The best provider would depend on the organization's existing cloud environment, budget, performance requirements, and other business needs. This activity helped me understand the connection between a Linux server and cloud computing because the same type of operating system can run on virtual machines provided by different cloud platforms.

