# Bootloader

## System Requirements :

**OS:-** Ubuntu 23.10

**RAM:-** 2GB or more.

**CPU:-** 2 or more.

**Storage**:- 20GB or more.

### What is bootloader?

A boot loader is a program that is responsible for loading and starting the operating system on a computer.

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/d3749e15-d6d0-4db6-97f6-6772c0356fc3)

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/b9d56b8b-34c3-4fe5-8b17-9f0873445028)

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/ca7f5381-8d6f-4338-898d-659542be45c6)

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/1a077f63-d01d-49c5-88d2-9fd349247039)

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/535ec566-da31-4f92-9c4f-cb31f562970c)

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/c7ff07a7-d1e8-41df-a17c-03bd477e60dd)

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/7c7aa254-8bdc-4b5b-b0aa-008f7bfe741b)

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/5a3fd6ad-b061-4c3b-b240-dbce44e0f27e)

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/23c0a6a9-3ed6-49dd-b108-c3f7a04931a7)

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/6f107189-68e4-449a-a588-524a3451d1ba)

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/7cde9af3-0273-4be7-9429-2df70531b483)

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/886e2361-d684-49e8-9619-61197f161a66)

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/9995d794-a940-4e65-af54-3710325b6f4c)

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/64bb376f-8ad4-41c7-a816-ddb1808a589c)

**If you're using Virtural machine. Follow below steps while creating Virtual Machine.**

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/93526919-7155-41f6-8948-028ee6df8fb3)

**Tick option Customize Configuration before install.**

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/75db9771-c1c5-421f-818b-e4c555f40c67)

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/1f35d9e0-3300-4e64-aec4-ffcd39c3345b)

**Select UEFI firmware in overview.**

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/5444cae2-f9f7-4d4b-b1ca-2af592926e1d)

**Enable Boot Menu from Boot Option.**

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/5b80e88f-0432-45ad-9ea6-8853d70f57a5)

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/df8f6096-4c65-4132-b5e2-cf436d7d5cf4)

**Disable Secure Boot from Boot Manager by default its Enable.**


![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/fcb470d5-2609-47e8-b76c-e12da7fb8208)

### Command

```
sudo su
```
### Output

boot@boot-Standard-PC-Q35-ICH9-2009:~$ sudo su
root@boot-Standard-PC-Q35-ICH9-2009:/home/boot# cd
root@boot-Standard-PC-Q35-ICH9-2009:~# 

### Command
```
apt install tree
```
**apt:**

This is the package management tool used on Debian-based Linux distributions, including Ubuntu. It is used to handle the installation, removal, and management of software packages.

**install:**

This is the APT command used to install software packages.

**tree:**

This is the name of the package that you want to install. In this case, it refers to a command-line utility called "tree" that displays the contents of a directory in a tree-like structure.

### Output

root@boot-Standard-PC-Q35-ICH9-2009:~# apt install tree
Reading package lists... Done
Building dependency tree       
Reading state information... Done
The following NEW packages will be installed:
  tree
0 upgraded, 1 newly installed, 0 to remove and 0 not upgraded.
Need to get 43.0 kB of archives.
After this operation, 115 kB of additional disk space will be used.
Get:1 http://in.archive.ubuntu.com/ubuntu focal/universe amd64 tree amd64 1.8.0-1 [43.0 kB]
Fetched 43.0 kB in 1s (33.2 kB/s)
Selecting previously unselected package tree.
(Reading database ... 157479 files and directories currently installed.)
Preparing to unpack .../tree_1.8.0-1_amd64.deb ...
Unpacking tree (1.8.0-1) ...
Setting up tree (1.8.0-1) ...
Processing triggers for man-db (2.9.1-1) ...
root@boot-Standard-PC-Q35-ICH9-2009:~# 

### Command
```
mount | grep efi
```
**mount:**

This command is used to display information about mounted filesystems on the system. It shows details such as the device, mount point, filesystem type, and other relevant information.

**|:** 

This symbol is called a pipe. It is used to pass the output of one command as the input to another command. In this case, it takes the output of the mount command and passes it to the next command.

**grep:**

This command is used to search for patterns within text. It filters lines that match a specified pattern. In this case, it filters lines containing the term "efi."

**efi:**

This is the pattern being searched for. The grep command will only display lines that contain the term "efi."

### Output

root@boot-Standard-PC-Q35-ICH9-2009:~# mount | grep efi
efivarfs on /sys/firmware/efi/efivars type efivarfs (rw,nosuid,nodev,noexec,relatime)
/dev/vda1 on /boot/efi type vfat (rw,relatime,fmask=0077,dmask=0077,codepage=437,iocharset=iso8859-1,shortname=mixed,errors=remount-ro)
root@boot-Standard-PC-Q35-ICH9-2009:~# 

### Command

```  
tree /boot/efi/
```
**tree:**

This is the command-line utility used to display the directory structure in a tree-like format. It recursively lists the contents of directories and subdirectories, showing the hierarchical relationship of files and directories.

**/boot/efi/:**

This is the path to the directory for which you want to display the tree structure. In this case, it refers to the EFI (Extensible Firmware Interface) partition's "/boot/efi/" directory. On many Linux systems, this directory is used for storing boot-related files, especially on systems that use UEFI (Unified Extensible Firmware Interface) for booting.

### Output

root@boot-Standard-PC-Q35-ICH9-2009:~# tree /boot/efi/
/boot/efi/
└── EFI
    ├── BOOT
    │   ├── BOOTX64.EFI
    │   ├── fbx64.efi
    │   └── mmx64.efi
    └── ubuntu
        ├── BOOTX64.CSV
        ├── grub.cfg
        ├── grubx64.efi
        ├── mmx64.efi
        └── shimx64.efi

3 directories, 8 files
root@boot-Standard-PC-Q35-ICH9-2009:~# 

### Command

```
apt install build-essential uuid-dev iasl git  nasm  python-is-python3
```
**apt:**

This is the package management tool used on Debian-based Linux distributions, including Ubuntu. It is used to handle the installation, removal, and management of software packages.

**install:**

This is the APT command used to install software packages.

**build-essential:**

This is a meta-package that includes a collection of essential tools and libraries needed for building and compiling software. It typically includes essential development tools such as compilers, libraries, and build utilities.

**uuid-dev:**

This package provides development files and headers for working with UUIDs (Universally Unique Identifiers) in C programs.

**iasl:**

This is the Intel ACPI (Advanced Configuration and Power Interface) compiler and decompiler. It is used for working with ACPI tables.

**git:**

This is a version control system used for tracking changes in source code during software development.

**nasm:**

This is the Netwide Assembler, an assembler and disassembler for the x86 architecture.

**python-is-python3:**

On some systems, there is a distinction between the default Python 2 and Python 3 versions. This package is likely used to ensure that references to the python command point to Python 3, as Python 2 is deprecated.

### Output

root@boot-Standard-PC-Q35-ICH9-2009:~# apt install build-essential uuid-dev iasl git  nasm  python-is-python3
Reading package lists... Done
Building dependency tree       
Reading state information... Done
Note, selecting 'acpica-tools' instead of 'iasl'
The following additional packages will be installed:
  binutils binutils-common binutils-x86-64-linux-gnu dpkg-dev fakeroot g++ g++-9 gcc gcc-9 git-man
  libalgorithm-diff-perl libalgorithm-diff-xs-perl libalgorithm-merge-perl libasan5 libbinutils
  libc-dev-bin libc6-dev libcrypt-dev libctf-nobfd0 libctf0 liberror-perl libfakeroot libgcc-9-dev
  libitm1 liblsan0 libquadmath0 libstdc++-9-dev libtsan0 libubsan1 linux-libc-dev make manpages-dev
Suggested packages:
  binutils-doc debian-keyring g++-multilib g++-9-multilib gcc-9-doc gcc-multilib autoconf automake
  libtool flex bison gcc-doc gcc-9-multilib gcc-9-locales git-daemon-run | git-daemon-sysvinit git-doc
  git-el git-email git-gui gitk gitweb git-cvs git-mediawiki git-svn glibc-doc libstdc++-9-doc
  make-doc
The following NEW packages will be installed:
  acpica-tools binutils binutils-common binutils-x86-64-linux-gnu build-essential dpkg-dev fakeroot
  g++ g++-9 gcc gcc-9 git git-man libalgorithm-diff-perl libalgorithm-diff-xs-perl
  libalgorithm-merge-perl libasan5 libbinutils libc-dev-bin libc6-dev libcrypt-dev libctf-nobfd0
  libctf0 liberror-perl libfakeroot libgcc-9-dev libitm1 liblsan0 libquadmath0 libstdc++-9-dev
  libtsan0 libubsan1 linux-libc-dev make manpages-dev nasm python-is-python3 uuid-dev
0 upgraded, 38 newly installed, 0 to remove and 0 not upgraded.
Need to get 43.6 MB of archives.
After this operation, 216 MB of additional disk space will be used.
Do you want to continue? [Y/n] y
Get:1 http://in.archive.ubuntu.com/ubuntu focal/universe amd64 acpica-tools amd64 20190509-1 [868 kB]
Get:2 http://in.archive.ubuntu.com/ubuntu focal-updates/main amd64 binutils-common amd64 2.34-6ubuntu1.8 [208 kB]
Get:3 http://in.archive.ubuntu.com/ubuntu focal-updates/main amd64 libbinutils amd64 2.34-6ubuntu1.8 [475 kB]
Get:4 http://in.archive.ubuntu.com/ubuntu focal-updates/main amd64 libctf-nobfd0 amd64 2.34-6ubuntu1.8 [48.1 kB]
Get:5 http://in.archive.ubuntu.com/ubuntu focal-updates/main amd64 libctf0 amd64 2.34-6ubuntu1.8 [46.7 kB]
Get:6 http://in.archive.ubuntu.com/ubuntu focal-updates/main amd64 binutils-x86-64-linux-gnu amd64 2.34-6ubuntu1.8 [1,614 kB]
Get:7 http://in.archive.ubuntu.com/ubuntu focal-updates/main amd64 binutils amd64 2.34-6ubuntu1.8 [3,384 B]
Get:8 http://in.archive.ubuntu.com/ubuntu focal-updates/main amd64 libc-dev-bin amd64 2.31-0ubuntu9.14 [71.8 kB]
Get:9 http://in.archive.ubuntu.com/ubuntu focal-updates/main amd64 linux-libc-dev amd64 5.4.0-172.190 [1,131 kB]
Get:10 http://in.archive.ubuntu.com/ubuntu focal/main amd64 libcrypt-dev amd64 1:4.4.10-10ubuntu4 [104 kB]
Get:11 http://in.archive.ubuntu.com/ubuntu focal-updates/main amd64 libc6-dev amd64 2.31-0ubuntu9.14 [2,519 kB]
Get:12 http://in.archive.ubuntu.com/ubuntu focal-updates/main amd64 libitm1 amd64 10.5.0-1ubuntu1~20.04 [26.2 kB]
Get:13 http://in.archive.ubuntu.com/ubuntu focal-updates/main amd64 libasan5 amd64 9.4.0-1ubuntu1~20.04.2 [2,752 kB]
Get:14 http://in.archive.ubuntu.com/ubuntu focal-updates/main amd64 liblsan0 amd64 10.5.0-1ubuntu1~20.04 [835 kB]
Get:15 http://in.archive.ubuntu.com/ubuntu focal-updates/main amd64 libtsan0 amd64 10.5.0-1ubuntu1~20.04 [2,016 kB]
Get:16 http://in.archive.ubuntu.com/ubuntu focal-updates/main amd64 libubsan1 amd64 10.5.0-1ubuntu1~20.04 [785 kB]
Get:17 http://in.archive.ubuntu.com/ubuntu focal-updates/main amd64 libquadmath0 amd64 10.5.0-1ubuntu1~20.04 [146 kB]
Get:18 http://in.archive.ubuntu.com/ubuntu focal-updates/main amd64 libgcc-9-dev amd64 9.4.0-1ubuntu1~20.04.2 [2,359 kB]
Get:19 http://in.archive.ubuntu.com/ubuntu focal-updates/main amd64 gcc-9 amd64 9.4.0-1ubuntu1~20.04.2 [8,276 kB]
Get:20 http://in.archive.ubuntu.com/ubuntu focal/main amd64 gcc amd64 4:9.3.0-1ubuntu2 [5,208 B]
Get:21 http://in.archive.ubuntu.com/ubuntu focal-updates/main amd64 libstdc++-9-dev amd64 9.4.0-1ubuntu1~20.04.2 [1,722 kB]
Get:22 http://in.archive.ubuntu.com/ubuntu focal-updates/main amd64 g++-9 amd64 9.4.0-1ubuntu1~20.04.2 [8,421 kB]
Get:23 http://in.archive.ubuntu.com/ubuntu focal/main amd64 g++ amd64 4:9.3.0-1ubuntu2 [1,604 B]       
Get:24 http://in.archive.ubuntu.com/ubuntu focal/main amd64 make amd64 4.2.1-1.2 [162 kB]              
Get:25 http://in.archive.ubuntu.com/ubuntu focal-updates/main amd64 dpkg-dev all 1.19.7ubuntu3.2 [679 kB]
Get:26 http://in.archive.ubuntu.com/ubuntu focal-updates/main amd64 build-essential amd64 12.8ubuntu1.1 [4,664 B]
Get:27 http://in.archive.ubuntu.com/ubuntu focal/main amd64 libfakeroot amd64 1.24-1 [25.7 kB]         
Get:28 http://in.archive.ubuntu.com/ubuntu focal/main amd64 fakeroot amd64 1.24-1 [62.6 kB]            
Get:29 http://in.archive.ubuntu.com/ubuntu focal/main amd64 liberror-perl all 0.17029-1 [26.5 kB]      
Get:30 http://in.archive.ubuntu.com/ubuntu focal-updates/main amd64 git-man all 1:2.25.1-1ubuntu3.11 [887 kB]
Get:31 http://in.archive.ubuntu.com/ubuntu focal-updates/main amd64 git amd64 1:2.25.1-1ubuntu3.11 [4,605 kB]
Get:32 http://in.archive.ubuntu.com/ubuntu focal/main amd64 libalgorithm-diff-perl all 1.19.03-2 [46.6 kB]
Get:33 http://in.archive.ubuntu.com/ubuntu focal/main amd64 libalgorithm-diff-xs-perl amd64 0.04-6 [11.3 kB]
Get:34 http://in.archive.ubuntu.com/ubuntu focal/main amd64 libalgorithm-merge-perl all 0.08-3 [12.0 kB]
Get:35 http://in.archive.ubuntu.com/ubuntu focal/main amd64 manpages-dev all 5.05-1 [2,266 kB]         
Get:36 http://in.archive.ubuntu.com/ubuntu focal/universe amd64 nasm amd64 2.14.02-1 [362 kB]          
Get:37 http://in.archive.ubuntu.com/ubuntu focal/main amd64 python-is-python3 all 3.8.2-4 [2,364 B]    
Get:38 http://in.archive.ubuntu.com/ubuntu focal-updates/main amd64 uuid-dev amd64 2.34-0.1ubuntu9.4 [33.6 kB]
Fetched 43.6 MB in 10s (4,320 kB/s)                                                                    
Extracting templates from packages: 100%
Selecting previously unselected package acpica-tools.
(Reading database ... 157486 files and directories currently installed.)
Preparing to unpack .../00-acpica-tools_20190509-1_amd64.deb ...
Unpacking acpica-tools (20190509-1) ...
Selecting previously unselected package binutils-common:amd64.
Preparing to unpack .../01-binutils-common_2.34-6ubuntu1.8_amd64.deb ...
Unpacking binutils-common:amd64 (2.34-6ubuntu1.8) ...
Selecting previously unselected package libbinutils:amd64.
Preparing to unpack .../02-libbinutils_2.34-6ubuntu1.8_amd64.deb ...
Unpacking libbinutils:amd64 (2.34-6ubuntu1.8) ...
Selecting previously unselected package libctf-nobfd0:amd64.
Preparing to unpack .../03-libctf-nobfd0_2.34-6ubuntu1.8_amd64.deb ...
Unpacking libctf-nobfd0:amd64 (2.34-6ubuntu1.8) ...
Selecting previously unselected package libctf0:amd64.
Preparing to unpack .../04-libctf0_2.34-6ubuntu1.8_amd64.deb ...
Unpacking libctf0:amd64 (2.34-6ubuntu1.8) ...
Selecting previously unselected package binutils-x86-64-linux-gnu.
Preparing to unpack .../05-binutils-x86-64-linux-gnu_2.34-6ubuntu1.8_amd64.deb ...
Unpacking binutils-x86-64-linux-gnu (2.34-6ubuntu1.8) ...
Selecting previously unselected package binutils.
Preparing to unpack .../06-binutils_2.34-6ubuntu1.8_amd64.deb ...
Unpacking binutils (2.34-6ubuntu1.8) ...
Selecting previously unselected package libc-dev-bin.
Preparing to unpack .../07-libc-dev-bin_2.31-0ubuntu9.14_amd64.deb ...
Unpacking libc-dev-bin (2.31-0ubuntu9.14) ...
Selecting previously unselected package linux-libc-dev:amd64.
Preparing to unpack .../08-linux-libc-dev_5.4.0-172.190_amd64.deb ...
Unpacking linux-libc-dev:amd64 (5.4.0-172.190) ...
Selecting previously unselected package libcrypt-dev:amd64.
Preparing to unpack .../09-libcrypt-dev_1%3a4.4.10-10ubuntu4_amd64.deb ...
Unpacking libcrypt-dev:amd64 (1:4.4.10-10ubuntu4) ...
Selecting previously unselected package libc6-dev:amd64.
Preparing to unpack .../10-libc6-dev_2.31-0ubuntu9.14_amd64.deb ...
Unpacking libc6-dev:amd64 (2.31-0ubuntu9.14) ...
Selecting previously unselected package libitm1:amd64.
Preparing to unpack .../11-libitm1_10.5.0-1ubuntu1~20.04_amd64.deb ...
Unpacking libitm1:amd64 (10.5.0-1ubuntu1~20.04) ...
Selecting previously unselected package libasan5:amd64.
Preparing to unpack .../12-libasan5_9.4.0-1ubuntu1~20.04.2_amd64.deb ...
Unpacking libasan5:amd64 (9.4.0-1ubuntu1~20.04.2) ...
Selecting previously unselected package liblsan0:amd64.
Preparing to unpack .../13-liblsan0_10.5.0-1ubuntu1~20.04_amd64.deb ...
Unpacking liblsan0:amd64 (10.5.0-1ubuntu1~20.04) ...
Selecting previously unselected package libtsan0:amd64.
Preparing to unpack .../14-libtsan0_10.5.0-1ubuntu1~20.04_amd64.deb ...
Unpacking libtsan0:amd64 (10.5.0-1ubuntu1~20.04) ...
Selecting previously unselected package libubsan1:amd64.
Preparing to unpack .../15-libubsan1_10.5.0-1ubuntu1~20.04_amd64.deb ...
Unpacking libubsan1:amd64 (10.5.0-1ubuntu1~20.04) ...
Selecting previously unselected package libquadmath0:amd64.
Preparing to unpack .../16-libquadmath0_10.5.0-1ubuntu1~20.04_amd64.deb ...
Unpacking libquadmath0:amd64 (10.5.0-1ubuntu1~20.04) ...
Selecting previously unselected package libgcc-9-dev:amd64.
Preparing to unpack .../17-libgcc-9-dev_9.4.0-1ubuntu1~20.04.2_amd64.deb ...
Unpacking libgcc-9-dev:amd64 (9.4.0-1ubuntu1~20.04.2) ...
Selecting previously unselected package gcc-9.
Preparing to unpack .../18-gcc-9_9.4.0-1ubuntu1~20.04.2_amd64.deb ...
Unpacking gcc-9 (9.4.0-1ubuntu1~20.04.2) ...
Selecting previously unselected package gcc.
Preparing to unpack .../19-gcc_4%3a9.3.0-1ubuntu2_amd64.deb ...
Unpacking gcc (4:9.3.0-1ubuntu2) ...
Selecting previously unselected package libstdc++-9-dev:amd64.
Preparing to unpack .../20-libstdc++-9-dev_9.4.0-1ubuntu1~20.04.2_amd64.deb ...
Unpacking libstdc++-9-dev:amd64 (9.4.0-1ubuntu1~20.04.2) ...
Selecting previously unselected package g++-9.
Preparing to unpack .../21-g++-9_9.4.0-1ubuntu1~20.04.2_amd64.deb ...
Unpacking g++-9 (9.4.0-1ubuntu1~20.04.2) ...
Selecting previously unselected package g++.
Preparing to unpack .../22-g++_4%3a9.3.0-1ubuntu2_amd64.deb ...
Unpacking g++ (4:9.3.0-1ubuntu2) ...
Selecting previously unselected package make.
Preparing to unpack .../23-make_4.2.1-1.2_amd64.deb ...
Unpacking make (4.2.1-1.2) ...
Selecting previously unselected package dpkg-dev.
Preparing to unpack .../24-dpkg-dev_1.19.7ubuntu3.2_all.deb ...
Unpacking dpkg-dev (1.19.7ubuntu3.2) ...
Selecting previously unselected package build-essential.
Preparing to unpack .../25-build-essential_12.8ubuntu1.1_amd64.deb ...
Unpacking build-essential (12.8ubuntu1.1) ...
Selecting previously unselected package libfakeroot:amd64.
Preparing to unpack .../26-libfakeroot_1.24-1_amd64.deb ...
Unpacking libfakeroot:amd64 (1.24-1) ...
Selecting previously unselected package fakeroot.
Preparing to unpack .../27-fakeroot_1.24-1_amd64.deb ...
Unpacking fakeroot (1.24-1) ...
Selecting previously unselected package liberror-perl.
Preparing to unpack .../28-liberror-perl_0.17029-1_all.deb ...
Unpacking liberror-perl (0.17029-1) ...
Selecting previously unselected package git-man.
Preparing to unpack .../29-git-man_1%3a2.25.1-1ubuntu3.11_all.deb ...
Unpacking git-man (1:2.25.1-1ubuntu3.11) ...
Selecting previously unselected package git.
Preparing to unpack .../30-git_1%3a2.25.1-1ubuntu3.11_amd64.deb ...
Unpacking git (1:2.25.1-1ubuntu3.11) ...
Selecting previously unselected package libalgorithm-diff-perl.
Preparing to unpack .../31-libalgorithm-diff-perl_1.19.03-2_all.deb ...
Unpacking libalgorithm-diff-perl (1.19.03-2) ...
Selecting previously unselected package libalgorithm-diff-xs-perl.
Preparing to unpack .../32-libalgorithm-diff-xs-perl_0.04-6_amd64.deb ...
Unpacking libalgorithm-diff-xs-perl (0.04-6) ...
Selecting previously unselected package libalgorithm-merge-perl.
Preparing to unpack .../33-libalgorithm-merge-perl_0.08-3_all.deb ...
Unpacking libalgorithm-merge-perl (0.08-3) ...
Selecting previously unselected package manpages-dev.
Preparing to unpack .../34-manpages-dev_5.05-1_all.deb ...
Unpacking manpages-dev (5.05-1) ...
Selecting previously unselected package nasm.
Preparing to unpack .../35-nasm_2.14.02-1_amd64.deb ...
Unpacking nasm (2.14.02-1) ...
Selecting previously unselected package python-is-python3.
Preparing to unpack .../36-python-is-python3_3.8.2-4_all.deb ...
Unpacking python-is-python3 (3.8.2-4) ...
Selecting previously unselected package uuid-dev:amd64.
Preparing to unpack .../37-uuid-dev_2.34-0.1ubuntu9.4_amd64.deb ...
Unpacking uuid-dev:amd64 (2.34-0.1ubuntu9.4) ...
Setting up manpages-dev (5.05-1) ...
Setting up acpica-tools (20190509-1) ...
update-alternatives: using /usr/bin/acpixtract-acpica to provide /usr/bin/acpixtract (acpixtract) in aut
o mode
update-alternatives: using /usr/bin/acpidump-acpica to provide /usr/bin/acpidump (acpidump) in auto mode
Setting up libalgorithm-diff-perl (1.19.03-2) ...
Setting up binutils-common:amd64 (2.34-6ubuntu1.8) ...
Setting up linux-libc-dev:amd64 (5.4.0-172.190) ...
Setting up libctf-nobfd0:amd64 (2.34-6ubuntu1.8) ...
Setting up libfakeroot:amd64 (1.24-1) ...
Setting up fakeroot (1.24-1) ...
update-alternatives: using /usr/bin/fakeroot-sysv to provide /usr/bin/fakeroot (fakeroot) in auto mode
Setting up liberror-perl (0.17029-1) ...
Setting up libasan5:amd64 (9.4.0-1ubuntu1~20.04.2) ...
Setting up make (4.2.1-1.2) ...
Setting up libquadmath0:amd64 (10.5.0-1ubuntu1~20.04) ...
Setting up nasm (2.14.02-1) ...
Setting up libubsan1:amd64 (10.5.0-1ubuntu1~20.04) ...
Setting up libcrypt-dev:amd64 (1:4.4.10-10ubuntu4) ...
Setting up git-man (1:2.25.1-1ubuntu3.11) ...
Setting up libbinutils:amd64 (2.34-6ubuntu1.8) ...
Setting up libc-dev-bin (2.31-0ubuntu9.14) ...
Setting up python-is-python3 (3.8.2-4) ...
Setting up libalgorithm-diff-xs-perl (0.04-6) ...
Setting up liblsan0:amd64 (10.5.0-1ubuntu1~20.04) ...
Setting up libitm1:amd64 (10.5.0-1ubuntu1~20.04) ...
Setting up libalgorithm-merge-perl (0.08-3) ...
Setting up libtsan0:amd64 (10.5.0-1ubuntu1~20.04) ...
Setting up libctf0:amd64 (2.34-6ubuntu1.8) ...
Setting up libgcc-9-dev:amd64 (9.4.0-1ubuntu1~20.04.2) ...
Setting up git (1:2.25.1-1ubuntu3.11) ...
Setting up libc6-dev:amd64 (2.31-0ubuntu9.14) ...
Setting up binutils-x86-64-linux-gnu (2.34-6ubuntu1.8) ...
Setting up libstdc++-9-dev:amd64 (9.4.0-1ubuntu1~20.04.2) ...
Setting up binutils (2.34-6ubuntu1.8) ...
Setting up dpkg-dev (1.19.7ubuntu3.2) ...
Setting up uuid-dev:amd64 (2.34-0.1ubuntu9.4) ...
Setting up gcc-9 (9.4.0-1ubuntu1~20.04.2) ...
Setting up gcc (4:9.3.0-1ubuntu2) ...
Setting up g++-9 (9.4.0-1ubuntu1~20.04.2) ...
Setting up g++ (4:9.3.0-1ubuntu2) ...
update-alternatives: using /usr/bin/g++ to provide /usr/bin/c++ (c++) in auto mode
Setting up build-essential (12.8ubuntu1.1) ...
Processing triggers for man-db (2.9.1-1) ...
Processing triggers for libc-bin (2.31-0ubuntu9.14) ...
root@boot-Standard-PC-Q35-ICH9-2009:~# 

### Command

```
cd /home/boot/Downloads/
```
**cd:** 

This stands for "change directory." It is a command used to change the current working directory in the command line.

**/home/boot/Downloads/:**

This is the path to the directory you want to change into. In this case, it specifies the absolute path to the "Downloads" directory located within the "boot" user's home directory.
### Output

root@boot-Standard-PC-Q35-ICH9-2009:~# cd /home/boot/Downloads/
root@boot-Standard-PC-Q35-ICH9-2009:/home/boot/Downloads# 

### Command

```
wget -c http://security.ubuntu.com/ubuntu/pool/universe/n/nasm/nasm_2.15.05-1_amd64.deb
```
**wget:**

This is a command-line utility for downloading files from the web. It is often used to retrieve files and content from web servers.

**-c:**

This option stands for "continue." If the download is interrupted or if the file already exists locally, this option allows wget to resume the download from where it left off.

**http://security.ubuntu.com/ubuntu/pool/universe/n/nasm/nasm_2.15.05-1_amd64.deb:**

This is the URL of the Debian package file you want to download. In this case, it is the NASM (Netwide Assembler) package with version 2.15.05-1 for the AMD64 architecture.

### Output

root@boot-Standard-PC-Q35-ICH9-2009:/home/boot/Downloads# wget -c http://security.ubuntu.com/ubuntu/pool/universe/n/nasm/nasm_2.15.05-1_amd64.deb
--2024-02-21 14:54:16--  http://security.ubuntu.com/ubuntu/pool/universe/n/nasm/nasm_2.15.05-1_amd64.deb
Resolving security.ubuntu.com (security.ubuntu.com)... 185.125.190.36, 91.189.91.81, 185.125.190.39, ...
Connecting to security.ubuntu.com (security.ubuntu.com)|185.125.190.36|:80... connected.
HTTP request sent, awaiting response... 200 OK
Length: 375168 (366K) [application/x-debian-package]
Saving to: ‘nasm_2.15.05-1_amd64.deb’

nasm_2.15.05-1_amd64.deb  100%[=====================================>] 366.38K   436KB/s    in 0.8s    

2024-02-21 14:54:17 (436 KB/s) - ‘nasm_2.15.05-1_amd64.deb’ saved [375168/375168]

root@boot-Standard-PC-Q35-ICH9-2009:/home/boot/Downloads# 

### Command

```
apt install /home/boot/Downloads/nasm_2.15.05-1_amd64.deb
```
**apt:**

This is the package management tool used on Debian-based Linux distributions, including Ubuntu. It is used to handle the installation, removal, and management of software packages.

**install:**

This is the APT command used to install software packages.

**/home/boot/Downloads/nasm_2.15.05-1_amd64.deb:**

This is the path to the Debian package file you want to install. In this case, it specifies the absolute path to the NASM (Netwide Assembler) package with version 2.15.05-1 for the AMD64 architecture.

### Output

root@boot-Standard-PC-Q35-ICH9-2009:/home/boot/Downloads# apt install /home/boot/Downloads/nasm_2.15.05-1_amd64.deb
Reading package lists... Done
Building dependency tree       
Reading state information... Done
Note, selecting 'nasm' instead of '/home/boot/Downloads/nasm_2.15.05-1_amd64.deb'
The following packages will be upgraded:
  nasm
1 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
Need to get 0 B/375 kB of archives.
After this operation, 28.7 kB disk space will be freed.
Get:1 /home/boot/Downloads/nasm_2.15.05-1_amd64.deb nasm amd64 2.15.05-1 [375 kB]
(Reading database ... 163890 files and directories currently installed.)
Preparing to unpack .../nasm_2.15.05-1_amd64.deb ...
Unpacking nasm (2.15.05-1) over (2.14.02-1) ...
Setting up nasm (2.15.05-1) ...
Processing triggers for man-db (2.9.1-1) ...
root@boot-Standard-PC-Q35-ICH9-2009:/home/boot/Downloads# 

### Command

```
nasm --version
```
**nasm:**

This is the command for the NASM assembler. NASM is a popular assembler used for x86 and x86-64 architectures.

**--version:**

It is used to display version information. 

### Output

root@boot-Standard-PC-Q35-ICH9-2009:/home/boot/Downloads# nasm --version
NASM version 2.15.05
root@boot-Standard-PC-Q35-ICH9-2009:/home/boot/Downloads# 

### Command

```
mkdir ~/src
```
**mkdir:**

This stands for "make directory." It is a command in Unix-like operating systems used to create a new directory or folder.

**~/src:**

This specifies the path where the new directory should be created. The tilde (~) is a shorthand notation for the user's home directory. So, ~/src refers to a directory named "src" within the user's home directory.   

### Output

root@boot-Standard-PC-Q35-ICH9-2009:/home/boot/Downloads# mkdir ~/src
root@boot-Standard-PC-Q35-ICH9-2009:/home/boot/Downloads# 

### Command
```   
cd ~/src/
```
**cd:** 

This stands for "change directory." It is a command used to change the current working directory in the command line.

**~/src:**

This specifies the path where the new directory should be created. The tilde (~) is a shorthand notation for the user's home directory. So, ~/src refers to a directory named "src" within the user's home directory. 

### Output

root@boot-Standard-PC-Q35-ICH9-2009:/home/boot/Downloads# cd ~/src/
root@boot-Standard-PC-Q35-ICH9-2009:~/src# 

### Command

```
git clone https://github.com/tianocore/edk2
```
**git:** 

This is the command-line interface for the Git version control system. Git is used for tracking changes in source code during software development.

**clone:**

This is a Git command used to create a copy or clone of a remote Git repository.

**https://github.com/tianocore/edk2:** 

This is the URL of the Git repository you want to clone. In this case, it's the EDK II (Extensible Firmware Interface Development Kit) repository hosted on GitHub. EDK II is an open-source project that provides a set of development tools and firmware libraries for UEFI (Unified Extensible Firmware Interface) development.

### Output

root@boot-Standard-PC-Q35-ICH9-2009:~/src# git clone https://github.com/tianocore/edk2
Cloning into 'edk2'...
remote: Enumerating objects: 387665, done.
remote: Counting objects: 100% (295/295), done.
remote: Compressing objects: 100% (154/154), done.
remote: Total 387665 (delta 165), reused 224 (delta 136), pack-reused 387370
Receiving objects: 100% (387665/387665), 312.56 MiB | 9.97 MiB/s, done.
Resolving deltas: 100% (281517/281517), done.
root@boot-Standard-PC-Q35-ICH9-2009:~/src# 

### Command

 ``` 
cd edk2/
 ```
Change directory to edk2 directory.

### Output

root@boot-Standard-PC-Q35-ICH9-2009:~/src# cd edk2/
root@boot-Standard-PC-Q35-ICH9-2009:~/src/edk2#

### Command

```
git checkout tags/edk2-stable202208
```
**git:** 

This is the command-line interface for the Git version control system. Git is used for tracking changes in source code during software development.

**checkout:** This is a Git command used for switching branches or tags. In this case, it is used to switch to a specific tag.

tags/edk2-stable202208: This specifies the tag you want to check out. Tags in Git are used to label specific points in the commit history, often denoting releases or important milestones.

### Output

root@boot-Standard-PC-Q35-ICH9-2009:~/src/edk2# git checkout tags/edk2-stable202208
Note: switching to 'tags/edk2-stable202208'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at ba0e0e4c6a BaseTools: Fix DevicePath GNUmakefile for macOS
root@boot-Standard-PC-Q35-ICH9-2009:~/src/edk2# 

### Command
```
git switch -c niteshboot
```
**git switch:** This is the main command for switching branches in Git.

**-c:** This option is used to create a new branch.

**niteshboot:** This is the name of the new branch that will be created. In this case, the branch will be named "niteshboot."

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/9e878014-bbe3-4457-b200-143f1ea58082)

```   
git branch
```
**git branch:** It is used to list all the branches in the repository.

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/8c8c7fde-b98f-4bbb-a1d6-112edc98bda3)


```   
git submodule update --init
```
**git submodule:**

This is the main command for working with Git submodules.

**update:** 

This is a submodule subcommand that is used to update the submodules to the latest commit in their respective repositories.

**--init:**

This option is used to initialize any submodules that are not initialized yet. If a submodule has already been initialized, this option has no effect.

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/8c68c54c-5abb-4898-beca-16acc115896d)

```   
make -C BaseTools
```
**make:**

make is a build automation tool that is used to compile and build projects. It reads a file called Makefile to determine how to build a program or a set of programs.

**-C:**

This option is used to specify the directory where make should change to before looking for the Makefile. In this case, it specifies the "BaseTools" directory.

**BaseTools:**

This is the directory where make should change to before attempting to build. It's the target directory where the build process will take place.

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/1ef1a0b4-afb8-443e-9c6e-c66417a40659)

```  
. edksetup.sh
```
**. (dot):** 

This is a shell built-in command that is used to run commands from a script in the current shell environment. When you run a script using . or source, it executes the commands in the current shell rather than spawning a new subshell. In this case, it's used to execute the commands in the edksetup.sh script within the current shell.

**edksetup.sh:**

This is a shell script provided by the EDK II framework. It typically sets up the necessary environment variables and configurations required for building UEFI firmware with the EDK II tools.

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/48e8fc4d-920c-4cda-abb5-27a9ef391901)

```   
export EDK_TOOLS_PATH=$HOME/src/edk2/BaseTools
```
**export:** 

This command is used to set an environment variable in the shell.

**EDK_TOOLS_PATH:**

This is the name of the environment variable being set. It represents the path to the BaseTools directory in the EDK II framework.

**$HOME/src/edk2/BaseTools:**

This is the value assigned to the EDK_TOOLS_PATH variable. $HOME is a shell variable that represents the user's home directory. So, this command sets EDK_TOOLS_PATH to the absolute path of the BaseTools directory within the user's home directory.

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/7432f6ea-0933-44c2-abbd-c83892938f17)

```   
echo $EDK_TOOLS_PATH
```
**echo:** This command is used to print the value of a variable or a specified string to the terminal.

**$EDK_TOOLS_PATH:**

This is a reference to the EDK_TOOLS_PATH environment variable. The $ sign is used to indicate that the following text is the name of a variable, and the shell should substitute it with its current value.

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/ccff8c29-9a5b-4eca-9774-43ec0eb679bd)

```   
. edksetup.sh BaseTools
```
**. (dot):**

This is a shell built-in command used to execute commands from a script within the current shell environment. It is also known as the "source" command. When you run a script using . or source, it runs the commands in the current shell instead of creating a new shell.

**edksetup.sh:**

This is a shell script provided by the EDK II framework. It is typically used to set up the environment variables and configurations required for building UEFI firmware with the EDK II tools.

**BaseTools:**

This argument is passed to the edksetup.sh script, and it likely specifies a subcomponent or submodule of the EDK II framework, such as the "BaseTools" submodule. It indicates which specific components need to be configured.

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/aa819c39-06f0-46fd-8955-7f948a34f116)

```   
cp Conf/target.txt Conf/target.org
```
**cp:**

This is the command for copying files or directories.

**Conf/target.txt:**

This is the source file. It specifies the file named target.txt in the Conf directory.

**Conf/target.org:**

This is the destination file. It specifies the file named target.org in the Conf directory.
![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/d8566788-6f60-49d3-834d-288887ade855)

```   
nano Conf/target.txt
```
**nano:**

This is the name of the text editor. Nano is a simple, command-line-based text editor that is easy to use for basic text editing tasks.

**Conf/target.txt:**

This specifies the file to be edited. It indicates the file named target.txt located in the Conf directory.


```   
diff Conf/target.txt Conf/target.org
```
**diff:** 

This is the command for performing file comparisons.

**Conf/target.txt:** 

This is the first file for comparison. It specifies the file named target.txt in the Conf directory.

**Conf/target.org:**

This is the second file for comparison. It specifies the file named target.org in the Conf directory.

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/dca618b7-2463-4785-9445-a69bebe0527a)

```   
ls MdeModulePkg/Application/HelloWorld/
```
**ls:**

This is the command for listing files and directories.

**MdeModulePkg/Application/HelloWorld/:**

This is the directory path for which you want to list the contents. It specifies the "HelloWorld" directory within the "Application" directory inside the "MdeModulePkg" directory.

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/a2168eb2-ea1d-4103-83e9-b498690fb89e)

```   
 cd MdeModulePkg/Application/HelloWorld/
```
**cd:** 

This is the command for changing the current working directory.

**MdeModulePkg/Application/HelloWorld/:**

This is the directory path to which you want to change the current working directory. It specifies the "HelloWorld" directory within the "Application" directory inside the "MdeModulePkg" directory.

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/ba3706a7-1e9b-4369-bff2-21757df11c47)
```
ls
```
**ls:**
List the files within MdeModulePkg/Application/HelloWorld/ directory.

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/d72a0cdd-4d0e-4e19-af7b-c0d29e41cb1c)

``` 
cat HelloWorld.c
```
**cat:**

This is the command for concatenating and displaying the content of files.

**HelloWorld.c:** 

This is the file whose content you want to display. 

```
nano HelloWorld.c
```
**nano:**

This is the name of the text editor. Nano is a simple, command-line-based text editor that is easy to use for basic text editing tasks.

**HelloWorld.c:**

This is the file you want to edit. Paste the below code in the HelloWorld.c file to get desire output.
```
/** @file
  This sample application bases on HelloWorld PCD setting
  to print "Custom text" to the UEFI Console.

  Copyright (c) 2006 - 2018, Intel Corporation. All rights reserved.<BR>
  SPDX-License-Identifier: BSD-2-Clause-Patent

**/

#include <Uefi.h>
#include <Library/PcdLib.h>
#include <Library/UefiLib.h>
#include <Library/UefiBootServicesTableLib.h>  // Include for Stall function

// Removed the unnecessary global variable for help message

/**
  The user Entry Point for Application. The user code starts with this function
  as the real entry point for the application.

  @param[in] ImageHandle    The firmware allocated handle for the EFI image.
  @param[in] SystemTable    A pointer to the EFI System Table.

  @retval EFI_SUCCESS       The entry point is executed successfully.
  @retval other             Some error occurs when executing this entry point.

**/
EFI_STATUS
EFIAPI
UefiMain (
  IN EFI_HANDLE        ImageHandle,
  IN EFI_SYSTEM_TABLE  *SystemTable
  )
{
  UINT32  Index;

  Index = 0;

  //
  // Three PCD types (FeatureFlag, UINT32, and String) are used as the sample.
  //
  if (FeaturePcdGet (PcdHelloWorldPrintEnable)) {
    for (Index = 0; Index < PcdGet32 (PcdHelloWorldPrintTimes); Index++) {
      //
      // Use UefiLib Print API to print string to UEFI console
      //
      // The following line was commented out, as it was causing an issue
      // Print ((CHAR16 *)PcdGetPtr (PcdHelloWorldPrintString));

      // The following lines were added to set text color and print a string
      SystemTable->ConOut->SetAttribute(SystemTable->ConOut, EFI_YELLOW);
      Print(L"my name is Nitesh");

      // Stall for a while (15 seconds) to see the output on the console
      SystemTable->BootServices->Stall(15 * 1000000);  // 15 seconds in microseconds
    }
  }

  return EFI_SUCCESS;
}

```
![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/6364dfc9-925b-42b8-95fc-e698c2fed01e)

```   
cd ~/src/edk2/
```
**cd ~/src/edk2/:**
Change directory to ~/src/edk2/

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/a6902140-4369-4b5f-94ec-817cc5940948)

```   
build
```
The build command is used to initiate the build process for the UEFI project. The *.dsc file specifies the project configuration, dependencies, and build settings.

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/d63af7f7-e6d8-40aa-9c1d-ca5ed4e81c99)

```
ls Build/MdeModule/DEBUG_GCC5/X64/HelloWorld.*
```
List all the files and diectories in the Build/MdeModule/DEBUG_GCC5/X64/HelloWorld.*path whose name is HelloWorld.

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/f3441473-a8ea-4555-9bca-977bcacc34f9)
```
mkdir /boot/efi/EFI/nitesh_booting
```
Create a directory named nitesh_booting in /boot/efi/EFI/

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/5b2ebccf-589e-4e4c-8f22-0fbfa9e4fc3b)
```
cp Build/MdeModule/DEBUG_GCC5/X64/HelloWorld.efi /boot/efi/EFI/nitesh_booting
```
Copy the HelloWorld.efi file from  Build/MdeModule/DEBUG_GCC5/X64/HelloWorld.efi into /boot/efi/EFI/nitesh_booting.

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/a3e7cd58-2137-420e-a46a-72883bbc55ea)
```
tree /boot/efi/
```
Showing directory and files it contains in /boot/efi/ path.

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/b57f99f8-9721-4bc6-9c3f-04c2146e05b9)
   
```
efibootmgr -c -d /dev/vda1 -p 1 -L HelloWorldLoader -l \\EFI\\nitesh_booting\\HelloWorld.efi
```
**efibootmgr:**

This is the command-line tool for interacting with the UEFI boot manager.

**-c:**

This option is used to create a new boot entry.

**-d /dev/vda1:**

This specifies the device (disk) where the EFI System Partition (ESP) is located. In this case, it's set to /dev/vda1.

**-p 1:**

This specifies the partition number of the EFI System Partition (ESP) on the specified disk. In this case, it's set to partition 1.

**-L HelloWorldLoader:**

This sets the label or description for the new boot entry. In this case, it's set to "HelloWorldLoader."

**-l \\EFI\\nitesh_booting\\HelloWorld.efi:** 

This specifies the file path of the EFI application that should be loaded as the bootloader for the new entry. The double backslashes (\\) are used to escape the backslashes in the file path. 

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/6288ddd7-e150-4a9b-ae2d-9c203a37fc58)

reboot system and go to boot manager

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/e744ec1e-50f6-4b56-8723-9ce2ff441125)

Select HelloLodaer

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/4a5d2a55-fe38-4cea-8a02-544009325b9d)

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/ab3eed6c-ba42-489f-a5f0-7fb787b082d0)
