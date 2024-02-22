# Bootloader

# Table of content:

[What is bootloader](#What-is-bootloader)

[Creating virtual machine](#Creating-virtual-machine)

[Disable Secure Boot from Boot Manager by default its Enable](#Disable-Secure-Boot-from-Boot-Manager-by-default-its-Enable)

[Follow the sequence of commands to create bootloader](#Follow-the-sequence-of-commands-to-create-bootloader)

## System Requirements :

**OS:-** Ubuntu 22.10

**RAM:-** 2GB or more.

**CPU:-** 2 or more.

**Storage**:- 30GB or more.

### What is bootloader

A boot loader is a program that is responsible for loading and starting the operating system on a computer.

### Creating virtual machine

#### Step 1: Open the  virt-manager

Select the option of Local install media (ISO image or CD-ROM)

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/d3749e15-d6d0-4db6-97f6-6772c0356fc3)

#### Step-2: Click on browse button

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/b9d56b8b-34c3-4fe5-8b17-9f0873445028)

#### Step 3: Click on browse local

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/ca7f5381-8d6f-4338-898d-659542be45c6)

#### Step-4: Go to the directory where your ISO image is downloaded and select it.

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/1a077f63-d01d-49c5-88d2-9fd349247039)

#### Step-5: Click on forward.

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/535ec566-da31-4f92-9c4f-cb31f562970c)

#### Step-6: Choose memory and Numbers of CPU for your machine

In my machine, I choose 2GB RAM and 2 CPU

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/c7ff07a7-d1e8-41df-a17c-03bd477e60dd)

#### Step-7: Then give storage to your machine

In my machine, I gave 30GB storage

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/7c7aa254-8bdc-4b5b-b0aa-008f7bfe741b)

#### Step-8: Tick the option of customize configuaration before install

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/5a3fd6ad-b061-4c3b-b240-dbce44e0f27e)

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/23c0a6a9-3ed6-49dd-b108-c3f7a04931a7)

#### Step-9: Within Overview option, change your firmwere from BIOS to UEFI 

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/6f107189-68e4-449a-a588-524a3451d1ba)

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/7cde9af3-0273-4be7-9429-2df70531b483)

#### Step-10: Enable Boot Menu from Boot Option.

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/886e2361-d684-49e8-9619-61197f161a66)

#### Step-11: Click on apply to commit changes and begin installation from in top-left side

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/9995d794-a940-4e65-af54-3710325b6f4c)


![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/64bb376f-8ad4-41c7-a816-ddb1808a589c)



**Disable Secure Boot from Boot Manager by default its Enable**


![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/fcb470d5-2609-47e8-b76c-e12da7fb8208)

Follow the sequence of commands to create bootloader

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

root@boot-Standard-PC-Q35-ICH9-2009:~ apt install tree
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

root@boot-Standard-PC-Q35-ICH9-2009:~ mount | grep efi
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

root@boot-Standard-PC-Q35-ICH9-2009:~ apt install build-essential uuid-dev iasl git  nasm  python-is-python3

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

root@boot-Standard-PC-Q35-ICH9-2009:~/src git clone https://github.com/tianocore/edk2
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

### Output

root@boot-Standard-PC-Q35-ICH9-2009:~/src/edk2# git switch -c niteshboot

Switched to a new branch 'niteshboot'

root@boot-Standard-PC-Q35-ICH9-2009:~/src/edk2# 

### Command

```   
git branch
```
**git branch:** It is used to list all the branches in the repository.

### Output

root@boot-Standard-PC-Q35-ICH9-2009:~/src/edk2# git branch

  master
  
* niteshboot
  
root@boot-Standard-PC-Q35-ICH9-2009:~/src/edk2# 

### Command

```   
git submodule update --init
```
**git submodule:**

This is the main command for working with Git submodules.

**update:** 

This is a submodule subcommand that is used to update the submodules to the latest commit in their respective repositories.

**--init:**

This option is used to initialize any submodules that are not initialized yet. If a submodule has already been initialized, this option has no effect.

### Output

root@boot-Standard-PC-Q35-ICH9-2009:~/src/edk2 git submodule update --init
Submodule 'SoftFloat' (https://github.com/ucb-bar/berkeley-softfloat-3.git) registered for path 'ArmPkg/Library/ArmSoftFloatLib/berkeley-softfloat-3'
Submodule 'BaseTools/Source/C/BrotliCompress/brotli' (https://github.com/google/brotli) registered for path 'BaseTools/Source/C/BrotliCompress/brotli'
Submodule 'CryptoPkg/Library/OpensslLib/openssl' (https://github.com/openssl/openssl) registered for path 'CryptoPkg/Library/OpensslLib/openssl'
Submodule 'MdeModulePkg/Library/BrotliCustomDecompressLib/brotli' (https://github.com/google/brotli) registered for path 'MdeModulePkg/Library/BrotliCustomDecompressLib/brotli'
Submodule 'MdeModulePkg/Universal/RegularExpressionDxe/oniguruma' (https://github.com/kkos/oniguruma) registered for path 'MdeModulePkg/Universal/RegularExpressionDxe/oniguruma'
Submodule 'RedfishPkg/Library/JsonLib/jansson' (https://github.com/akheron/jansson) registered for path 'RedfishPkg/Library/JsonLib/jansson'
Submodule 'UnitTestFrameworkPkg/Library/CmockaLib/cmocka' (https://github.com/tianocore/edk2-cmocka.git) registered for path 'UnitTestFrameworkPkg/Library/CmockaLib/cmocka'
Cloning into '/root/src/edk2/ArmPkg/Library/ArmSoftFloatLib/berkeley-softfloat-3'...
Cloning into '/root/src/edk2/BaseTools/Source/C/BrotliCompress/brotli'...
Cloning into '/root/src/edk2/CryptoPkg/Library/OpensslLib/openssl'...
Cloning into '/root/src/edk2/MdeModulePkg/Library/BrotliCustomDecompressLib/brotli'...
Cloning into '/root/src/edk2/MdeModulePkg/Universal/RegularExpressionDxe/oniguruma'...
Cloning into '/root/src/edk2/RedfishPkg/Library/JsonLib/jansson'...
Cloning into '/root/src/edk2/UnitTestFrameworkPkg/Library/CmockaLib/cmocka'...
Submodule path 'ArmPkg/Library/ArmSoftFloatLib/berkeley-softfloat-3': checked out 'b64af41c3276f97f0e181920400ee056b9c88037'
Submodule path 'BaseTools/Source/C/BrotliCompress/brotli': checked out 'f4153a09f87cbb9c826d8fc12c74642bb2d879ea'
Submodule path 'CryptoPkg/Library/OpensslLib/openssl': checked out 'd82e959e621a3d597f1e0d50ff8c2d8b96915fd7'
Submodule path 'MdeModulePkg/Library/BrotliCustomDecompressLib/brotli': checked out 'f4153a09f87cbb9c826d8fc12c74642bb2d879ea'
Submodule path 'MdeModulePkg/Universal/RegularExpressionDxe/oniguruma': checked out 'abfc8ff81df4067f309032467785e06975678f0d'
Submodule path 'RedfishPkg/Library/JsonLib/jansson': checked out 'e9ebfa7e77a6bee77df44e096b100e7131044059'
Submodule path 'UnitTestFrameworkPkg/Library/CmockaLib/cmocka': checked out '1cc9cde3448cdd2e000886a26acf1caac2db7cf1'
root@boot-Standard-PC-Q35-ICH9-2009:~/src/edk2# 

### Command

```   
make -C BaseTools
```
**make:**

make is a build automation tool that is used to compile and build projects. It reads a file called Makefile to determine how to build a program or a set of programs.

**-C:**

This option is used to specify the directory where make should change to before looking for the Makefile. In this case, it specifies the "BaseTools" directory.

**BaseTools:**

This is the directory where make should change to before attempting to build. It's the target directory where the build process will take place.

### Output

root@boot-Standard-PC-Q35-ICH9-2009:~/src/edk2# make -C BaseTools
make: Entering directory '/root/src/edk2/BaseTools'
make -C Source/C
make[1]: Entering directory '/root/src/edk2/BaseTools/Source/C'
Attempting to detect HOST_ARCH from 'uname -m': x86_64
Detected HOST_ARCH of X64 using uname.
mkdir -p .
mkdir ./libs
make -C Common
make[2]: Entering directory '/root/src/edk2/BaseTools/Source/C/Common'
gcc  -c  -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  BasePeCoff.c -o BasePeCoff.o
gcc  -c  -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  BinderFuncs.c -o BinderFuncs.o
gcc  -c  -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  CommonLib.c -o CommonLib.o
gcc  -c  -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  Crc32.c -o Crc32.o
gcc  -c  -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  Decompress.c -o Decompress.o
gcc  -c  -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  EfiCompress.c -o EfiCompress.o
gcc  -c  -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  EfiUtilityMsgs.c -o EfiUtilityMsgs.o
gcc  -c  -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  FirmwareVolumeBuffer.c -o FirmwareVolumeBuffer.o
gcc  -c  -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  FvLib.c -o FvLib.o
gcc  -c  -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  MemoryFile.c -o MemoryFile.o
gcc  -c  -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  MyAlloc.c -o MyAlloc.o
gcc  -c  -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  OsPath.c -o OsPath.o
gcc  -c  -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  ParseGuidedSectionTools.c -o ParseGuidedSectionTools.o
gcc  -c  -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  ParseInf.c -o ParseInf.o
gcc  -c  -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  PeCoffLoaderEx.c -o PeCoffLoaderEx.o
gcc  -c  -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  SimpleFileParsing.c -o SimpleFileParsing.o
gcc  -c  -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  StringFuncs.c -o StringFuncs.o
gcc  -c  -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  TianoCompress.c -o TianoCompress.o
ar crs ../libs/libCommon.a BasePeCoff.o BinderFuncs.o CommonLib.o Crc32.o Decompress.o EfiCompress.o EfiUtilityMsgs.o FirmwareVolumeBuffer.o FvLib.o MemoryFile.o MyAlloc.o OsPath.o ParseGuidedSectionTools.o ParseInf.o PeCoffLoaderEx.o SimpleFileParsing.o StringFuncs.o TianoCompress.o
make[2]: Leaving directory '/root/src/edk2/BaseTools/Source/C/Common'
mkdir ./bin
make -C VfrCompile VfrLexer.h
make[2]: Entering directory '/root/src/edk2/BaseTools/Source/C/VfrCompile'
BIN_DIR='.' make -C Pccts/dlg
make[3]: Entering directory '/root/src/edk2/BaseTools/Source/C/VfrCompile/Pccts/dlg'
cc -O -I. -I../support/set -I../h -DUSER_ZZSYN -DZZLEXBUFSIZE=65536 -c dlg_p.c
cc -O -I. -I../support/set -I../h -DUSER_ZZSYN -DZZLEXBUFSIZE=65536 -c dlg_a.c
cc -O -I. -I../support/set -I../h -DUSER_ZZSYN -DZZLEXBUFSIZE=65536 -c main.c
cc -c -O -I. -I../support/set -I../h -DUSER_ZZSYN -DZZLEXBUFSIZE=65536  err.c -o err.o
cc -c -O -I. -I../support/set -I../h -DUSER_ZZSYN -DZZLEXBUFSIZE=65536 ../support/set/set.c
cc -c -O -I. -I../support/set -I../h -DUSER_ZZSYN -DZZLEXBUFSIZE=65536  support.c -o support.o
cc -c -O -I. -I../support/set -I../h -DUSER_ZZSYN -DZZLEXBUFSIZE=65536  output.c -o output.o
cc -c -O -I. -I../support/set -I../h -DUSER_ZZSYN -DZZLEXBUFSIZE=65536  relabel.c -o relabel.o
cc -c -O -I. -I../support/set -I../h -DUSER_ZZSYN -DZZLEXBUFSIZE=65536  automata.c -o automata.o
cc -O -I. -I../support/set -I../h -DUSER_ZZSYN -DZZLEXBUFSIZE=65536 -o ./dlg dlg_p.o dlg_a.o main.o err.o set.o support.o output.o relabel.o automata.o
make[3]: Leaving directory '/root/src/edk2/BaseTools/Source/C/VfrCompile/Pccts/dlg'
BIN_DIR='.' make -C Pccts/antlr
make[3]: Entering directory '/root/src/edk2/BaseTools/Source/C/VfrCompile/Pccts/antlr'
gcc -c -O -I. -I../support/set -I../h -DUSER_ZZSYN  -DZZLEXBUFSIZE=65536  antlr.c -o antlr.o
gcc -c -O -I. -I../support/set -I../h -DUSER_ZZSYN  -DZZLEXBUFSIZE=65536  scan.c -o scan.o
gcc -c -O -I. -I../support/set -I../h -DUSER_ZZSYN  -DZZLEXBUFSIZE=65536  err.c -o err.o
gcc -c -O -I. -I../support/set -I../h -DUSER_ZZSYN  -DZZLEXBUFSIZE=65536  bits.c -o bits.o
gcc -c -O -I. -I../support/set -I../h -DUSER_ZZSYN  -DZZLEXBUFSIZE=65536  build.c -o build.o
gcc -c -O -I. -I../support/set -I../h -DUSER_ZZSYN  -DZZLEXBUFSIZE=65536  fset2.c -o fset2.o
gcc -c -O -I. -I../support/set -I../h -DUSER_ZZSYN  -DZZLEXBUFSIZE=65536  fset.c -o fset.o
gcc -c -O -I. -I../support/set -I../h -DUSER_ZZSYN  -DZZLEXBUFSIZE=65536  gen.c -o gen.o
gcc -c -O -I. -I../support/set -I../h -DUSER_ZZSYN  -DZZLEXBUFSIZE=65536  globals.c -o globals.o
gcc -c -O -I. -I../support/set -I../h -DUSER_ZZSYN  -DZZLEXBUFSIZE=65536  hash.c -o hash.o
gcc -c -O -I. -I../support/set -I../h -DUSER_ZZSYN  -DZZLEXBUFSIZE=65536  lex.c -o lex.o
gcc -c -O -I. -I../support/set -I../h -DUSER_ZZSYN  -DZZLEXBUFSIZE=65536  main.c -o main.o
gcc -c -O -I. -I../support/set -I../h -DUSER_ZZSYN  -DZZLEXBUFSIZE=65536  misc.c -o misc.o
gcc -O -I. -I../support/set -I../h -DUSER_ZZSYN  -DZZLEXBUFSIZE=65536 -c -o set.o ../support/set/set.c
gcc -c -O -I. -I../support/set -I../h -DUSER_ZZSYN  -DZZLEXBUFSIZE=65536  pred.c -o pred.o
gcc -c -O -I. -I../support/set -I../h -DUSER_ZZSYN  -DZZLEXBUFSIZE=65536  egman.c -o egman.o
gcc -c -O -I. -I../support/set -I../h -DUSER_ZZSYN  -DZZLEXBUFSIZE=65536  mrhoist.c -o mrhoist.o
mrhoist.c: In function ‘MR_ruleNamePlusOffset’:
mrhoist.c:2220:37: warning: ‘__builtin___sprintf_chk’ may write a terminating nul past the end of the destination [-Wformat-overflow=]
 2220 |       sprintf(ruleNameStatic2,"%s/%d",ruleNameStatic1,offset+1);
      |                                     ^
In file included from /usr/include/stdio.h:867,
                 from mrhoist.c:28:
/usr/include/x86_64-linux-gnu/bits/stdio2.h:36:10: note: ‘__builtin___sprintf_chk’ output between 3 and 61 bytes into a destination of size 60
   36 |   return __builtin___sprintf_chk (__s, __USE_FORTIFY_LEVEL - 1,
      |          ^~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
   37 |       __bos (__s), __fmt, __va_arg_pack ());
      |       ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
gcc -c -O -I. -I../support/set -I../h -DUSER_ZZSYN  -DZZLEXBUFSIZE=65536  fcache.c -o fcache.o
gcc -O -I. -I../support/set -I../h -DUSER_ZZSYN  -DZZLEXBUFSIZE=65536 -o ./antlr antlr.o scan.o err.o bits.o build.o fset2.o fset.o gen.o globals.o hash.o lex.o main.o misc.o set.o pred.o egman.o mrhoist.o fcache.o
make[3]: Leaving directory '/root/src/edk2/BaseTools/Source/C/VfrCompile/Pccts/antlr'
Pccts/antlr/antlr -CC -e3 -ck 3 -k 2 -fl VfrParser.dlg -ft VfrTokens.h -o . VfrSyntax.g
Antlr parser generator   Version 1.33MR33   1989-2001
VfrSyntax.g, line 3529: warning: alts 1 and 2 of {..} ambiguous upon ( ";" RefreshGuid GuidOp Locked Image EndIf InconsistentIf DisableIf SuppressIf Default GrayOutIf )
VfrSyntax.g, line 3538: warning: alts 1 and 2 of {..} ambiguous upon ( ";" RefreshGuid GuidOp Locked Image EndIf InconsistentIf DisableIf SuppressIf Default GrayOutIf )
VfrSyntax.g, line 3547: warning: alts 1 and 2 of {..} ambiguous upon ( ";" RefreshGuid GuidOp Locked Image EndIf InconsistentIf DisableIf SuppressIf Default GrayOutIf )
VfrSyntax.g, line 3557: warning: alts 1 and 2 of {..} ambiguous upon ( ";" RefreshGuid GuidOp Locked Image EndIf InconsistentIf DisableIf SuppressIf Default GrayOutIf )
VfrSyntax.g, line 3587: warning: alts 1 and 2 of {..} ambiguous upon ( ";" RefreshGuid GuidOp Locked Image EndIf InconsistentIf DisableIf SuppressIf Default GrayOutIf )
VfrSyntax.g, line 3596: warning: alts 1 and 2 of {..} ambiguous upon ( ";" RefreshGuid GuidOp Locked Image EndIf InconsistentIf DisableIf SuppressIf Default GrayOutIf )
Pccts/dlg/dlg -C2 -i -CC -cl VfrLexer -o . VfrParser.dlg
dlg  Version 1.33MR33   1989-2001

make[2]: Leaving directory '/root/src/edk2/BaseTools/Source/C/VfrCompile'
make -C BrotliCompress
make[2]: Entering directory '/root/src/edk2/BaseTools/Source/C/BrotliCompress'
gcc  -c -I ./brotli/c/include -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  BrotliCompress.c -o BrotliCompress.o
gcc  -c -I ./brotli/c/include -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  brotli/c/common/platform.c -o brotli/c/common/platform.o
gcc  -c -I ./brotli/c/include -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  brotli/c/common/shared_dictionary.c -o brotli/c/common/shared_dictionary.o
gcc  -c -I ./brotli/c/include -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  brotli/c/common/constants.c -o brotli/c/common/constants.o
gcc  -c -I ./brotli/c/include -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  brotli/c/common/context.c -o brotli/c/common/context.o
gcc  -c -I ./brotli/c/include -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  brotli/c/enc/command.c -o brotli/c/enc/command.o
gcc  -c -I ./brotli/c/include -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  brotli/c/enc/compound_dictionary.c -o brotli/c/enc/compound_dictionary.o
gcc  -c -I ./brotli/c/include -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  brotli/c/enc/fast_log.c -o brotli/c/enc/fast_log.o
gcc  -c -I ./brotli/c/include -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  brotli/c/common/dictionary.c -o brotli/c/common/dictionary.o
gcc  -c -I ./brotli/c/include -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  brotli/c/common/transform.c -o brotli/c/common/transform.o
gcc  -c -I ./brotli/c/include -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  brotli/c/dec/bit_reader.c -o brotli/c/dec/bit_reader.o
gcc  -c -I ./brotli/c/include -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  brotli/c/dec/decode.c -o brotli/c/dec/decode.o
gcc  -c -I ./brotli/c/include -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  brotli/c/dec/huffman.c -o brotli/c/dec/huffman.o
gcc  -c -I ./brotli/c/include -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  brotli/c/dec/state.c -o brotli/c/dec/state.o
gcc  -c -I ./brotli/c/include -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  brotli/c/enc/backward_references.c -o brotli/c/enc/backward_references.o
gcc  -c -I ./brotli/c/include -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  brotli/c/enc/backward_references_hq.c -o brotli/c/enc/backward_references_hq.o
gcc  -c -I ./brotli/c/include -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  brotli/c/enc/bit_cost.c -o brotli/c/enc/bit_cost.o
gcc  -c -I ./brotli/c/include -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  brotli/c/enc/block_splitter.c -o brotli/c/enc/block_splitter.o
gcc  -c -I ./brotli/c/include -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  brotli/c/enc/brotli_bit_stream.c -o brotli/c/enc/brotli_bit_stream.o
gcc  -c -I ./brotli/c/include -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  brotli/c/enc/cluster.c -o brotli/c/enc/cluster.o
gcc  -c -I ./brotli/c/include -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  brotli/c/enc/compress_fragment.c -o brotli/c/enc/compress_fragment.o
gcc  -c -I ./brotli/c/include -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  brotli/c/enc/compress_fragment_two_pass.c -o brotli/c/enc/compress_fragment_two_pass.o
gcc  -c -I ./brotli/c/include -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  brotli/c/enc/dictionary_hash.c -o brotli/c/enc/dictionary_hash.o
gcc  -c -I ./brotli/c/include -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  brotli/c/enc/encode.c -o brotli/c/enc/encode.o
gcc  -c -I ./brotli/c/include -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  brotli/c/enc/encoder_dict.c -o brotli/c/enc/encoder_dict.o
gcc  -c -I ./brotli/c/include -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  brotli/c/enc/entropy_encode.c -o brotli/c/enc/entropy_encode.o
gcc  -c -I ./brotli/c/include -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  brotli/c/enc/histogram.c -o brotli/c/enc/histogram.o
gcc  -c -I ./brotli/c/include -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  brotli/c/enc/literal_cost.c -o brotli/c/enc/literal_cost.o
gcc  -c -I ./brotli/c/include -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  brotli/c/enc/memory.c -o brotli/c/enc/memory.o
gcc  -c -I ./brotli/c/include -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  brotli/c/enc/metablock.c -o brotli/c/enc/metablock.o
gcc  -c -I ./brotli/c/include -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  brotli/c/enc/static_dict.c -o brotli/c/enc/static_dict.o
gcc  -c -I ./brotli/c/include -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  brotli/c/enc/utf8_util.c -o brotli/c/enc/utf8_util.o
gcc -o ../bin/BrotliCompress   BrotliCompress.o brotli/c/common/platform.o brotli/c/common/shared_dictionary.o brotli/c/common/constants.o brotli/c/common/context.o brotli/c/enc/command.o brotli/c/enc/compound_dictionary.o brotli/c/enc/fast_log.o brotli/c/common/dictionary.o brotli/c/common/transform.o brotli/c/dec/bit_reader.o brotli/c/dec/decode.o brotli/c/dec/huffman.o brotli/c/dec/state.o brotli/c/enc/backward_references.o brotli/c/enc/backward_references_hq.o brotli/c/enc/bit_cost.o brotli/c/enc/block_splitter.o brotli/c/enc/brotli_bit_stream.o brotli/c/enc/cluster.o brotli/c/enc/compress_fragment.o brotli/c/enc/compress_fragment_two_pass.o brotli/c/enc/dictionary_hash.o brotli/c/enc/encode.o brotli/c/enc/encoder_dict.o brotli/c/enc/entropy_encode.o brotli/c/enc/histogram.o brotli/c/enc/literal_cost.o brotli/c/enc/memory.o brotli/c/enc/metablock.o brotli/c/enc/static_dict.o brotli/c/enc/utf8_util.o -L../libs -lm
make[2]: Leaving directory '/root/src/edk2/BaseTools/Source/C/BrotliCompress'
make -C VfrCompile
make[2]: Entering directory '/root/src/edk2/BaseTools/Source/C/VfrCompile'
g++ -c -DPCCTS_USE_NAMESPACE_STD -I Pccts/h -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/  -O2  Pccts/h/AParser.cpp -o AParser.o
g++ -c -DPCCTS_USE_NAMESPACE_STD -I Pccts/h -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/  -O2  Pccts/h/DLexerBase.cpp -o DLexerBase.o
g++ -c -DPCCTS_USE_NAMESPACE_STD -I Pccts/h -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/  -O2  Pccts/h/ATokenBuffer.cpp -o ATokenBuffer.o
g++ -c -I Pccts/h -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -Wno-unused-result -O2  EfiVfrParser.cpp -o EfiVfrParser.o
g++ -c -I Pccts/h -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -Wno-unused-result -O2  VfrLexer.cpp -o VfrLexer.o
g++ -c -DPCCTS_USE_NAMESPACE_STD -I Pccts/h -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/  -O2  VfrSyntax.cpp -o VfrSyntax.o
g++ -c -I Pccts/h -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -Wno-unused-result -O2  VfrFormPkg.cpp -o VfrFormPkg.o
g++ -c -I Pccts/h -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -Wno-unused-result -O2  VfrError.cpp -o VfrError.o
g++ -c -I Pccts/h -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -Wno-unused-result -O2  VfrUtilityLib.cpp -o VfrUtilityLib.o
g++ -c -I Pccts/h -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -Wno-unused-result -O2  VfrCompiler.cpp -o VfrCompiler.o
g++ -o ../bin/VfrCompile  AParser.o DLexerBase.o ATokenBuffer.o EfiVfrParser.o VfrLexer.o VfrSyntax.o VfrFormPkg.o VfrError.o VfrUtilityLib.o VfrCompiler.o -L../libs -lCommon
make[2]: Leaving directory '/root/src/edk2/BaseTools/Source/C/VfrCompile'
make -C EfiRom
make[2]: Entering directory '/root/src/edk2/BaseTools/Source/C/EfiRom'
gcc  -c  -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  EfiRom.c -o EfiRom.o
gcc -o ../bin/EfiRom   EfiRom.o -L../libs -lCommon
make[2]: Leaving directory '/root/src/edk2/BaseTools/Source/C/EfiRom'
make -C GenFfs
make[2]: Entering directory '/root/src/edk2/BaseTools/Source/C/GenFfs'
gcc  -c  -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  GenFfs.c -o GenFfs.o
gcc -o ../bin/GenFfs   GenFfs.o -L../libs -lCommon
make[2]: Leaving directory '/root/src/edk2/BaseTools/Source/C/GenFfs'
make -C GenFv
make[2]: Entering directory '/root/src/edk2/BaseTools/Source/C/GenFv'
gcc  -c  -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  GenFv.c -o GenFv.o
gcc  -c  -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  GenFvInternalLib.c -o GenFvInternalLib.o
gcc -o ../bin/GenFv   GenFv.o GenFvInternalLib.o -L../libs -lCommon -luuid
make[2]: Leaving directory '/root/src/edk2/BaseTools/Source/C/GenFv'
make -C GenFw
make[2]: Entering directory '/root/src/edk2/BaseTools/Source/C/GenFw'
gcc  -c  -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  GenFw.c -o GenFw.o
gcc  -c  -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  ElfConvert.c -o ElfConvert.o
gcc  -c  -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  Elf32Convert.c -o Elf32Convert.o
gcc  -c  -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  Elf64Convert.c -o Elf64Convert.o
gcc -o ../bin/GenFw   GenFw.o ElfConvert.o Elf32Convert.o Elf64Convert.o -L../libs -lCommon -luuid
make[2]: Leaving directory '/root/src/edk2/BaseTools/Source/C/GenFw'
make -C GenSec
make[2]: Entering directory '/root/src/edk2/BaseTools/Source/C/GenSec'
gcc  -c  -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  GenSec.c -o GenSec.o
gcc -o ../bin/GenSec   GenSec.o -L../libs -lCommon -luuid
make[2]: Leaving directory '/root/src/edk2/BaseTools/Source/C/GenSec'
make -C GenCrc32
make[2]: Entering directory '/root/src/edk2/BaseTools/Source/C/GenCrc32'
gcc  -c  -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  GenCrc32.c -o GenCrc32.o
gcc -o ../bin/GenCrc32   GenCrc32.o -L../libs -lCommon
make[2]: Leaving directory '/root/src/edk2/BaseTools/Source/C/GenCrc32'
make -C LzmaCompress
make[2]: Entering directory '/root/src/edk2/BaseTools/Source/C/LzmaCompress'
gcc  -c  -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  -D_7ZIP_ST LzmaCompress.c -o LzmaCompress.o
gcc  -c  -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  -D_7ZIP_ST Sdk/C/Alloc.c -o Sdk/C/Alloc.o
gcc  -c  -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  -D_7ZIP_ST Sdk/C/LzFind.c -o Sdk/C/LzFind.o
gcc  -c  -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  -D_7ZIP_ST Sdk/C/LzmaDec.c -o Sdk/C/LzmaDec.o
gcc  -c  -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  -D_7ZIP_ST Sdk/C/LzmaEnc.c -o Sdk/C/LzmaEnc.o
gcc  -c  -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  -D_7ZIP_ST Sdk/C/7zFile.c -o Sdk/C/7zFile.o
gcc  -c  -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  -D_7ZIP_ST Sdk/C/7zStream.c -o Sdk/C/7zStream.o
gcc  -c  -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  -D_7ZIP_ST Sdk/C/Bra86.c -o Sdk/C/Bra86.o
gcc -o ../bin/LzmaCompress   LzmaCompress.o Sdk/C/Alloc.o Sdk/C/LzFind.o Sdk/C/LzmaDec.o Sdk/C/LzmaEnc.o Sdk/C/7zFile.o Sdk/C/7zStream.o Sdk/C/Bra86.o -L../libs -lCommon
make[2]: Leaving directory '/root/src/edk2/BaseTools/Source/C/LzmaCompress'
make -C TianoCompress
make[2]: Entering directory '/root/src/edk2/BaseTools/Source/C/TianoCompress'
gcc  -c  -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  TianoCompress.c -o TianoCompress.o
gcc -o ../bin/TianoCompress   TianoCompress.o -L../libs -lCommon
make[2]: Leaving directory '/root/src/edk2/BaseTools/Source/C/TianoCompress'
make -C VolInfo
make[2]: Entering directory '/root/src/edk2/BaseTools/Source/C/VolInfo'
gcc  -c  -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  VolInfo.c -o VolInfo.o
gcc -o ../bin/VolInfo   VolInfo.o -L../libs -lCommon
make[2]: Leaving directory '/root/src/edk2/BaseTools/Source/C/VolInfo'
make -C DevicePath
make[2]: Entering directory '/root/src/edk2/BaseTools/Source/C/DevicePath'
gcc  -c  -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  -Wno-error=stringop-overflow DevicePath.c -o DevicePath.o
gcc  -c  -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  -Wno-error=stringop-overflow UefiDevicePathLib.c -o UefiDevicePathLib.o
gcc  -c  -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  -Wno-error=stringop-overflow DevicePathFromText.c -o DevicePathFromText.o
gcc  -c  -I .. -I ../Include/Common -I ../Include/ -I ../Include/IndustryStandard -I ../Common/ -I .. -I . -I ../Include/X64/ -MD -fshort-wchar -fno-strict-aliasing -fwrapv -fno-delete-null-pointer-checks -Wall -Werror -Wno-deprecated-declarations -Wno-stringop-truncation -Wno-restrict -Wno-unused-result -nostdlib -g -O2  -Wno-error=stringop-overflow DevicePathUtilities.c -o DevicePathUtilities.o
gcc -o ../bin/DevicePath   DevicePath.o UefiDevicePathLib.o DevicePathFromText.o  DevicePathUtilities.o -L../libs -lCommon -luuid
make[2]: Leaving directory '/root/src/edk2/BaseTools/Source/C/DevicePath'
Finished building BaseTools C Tools with HOST_ARCH=X64
make[1]: Leaving directory '/root/src/edk2/BaseTools/Source/C'
make -C Source/Python
make[1]: Entering directory '/root/src/edk2/BaseTools/Source/Python'
make[1]: Nothing to be done for 'all'.
make[1]: Leaving directory '/root/src/edk2/BaseTools/Source/Python'
make -C Tests
make[1]: Entering directory '/root/src/edk2/BaseTools/Tests'
testHelp (TianoCompress.Tests) ... ok
testRandomDataCycles (TianoCompress.Tests) ... ok
test_AmlToC_AmlToC (CheckPythonSyntax.Tests) ... ok
test_AutoGen_AutoGen (CheckPythonSyntax.Tests) ... ok
test_AutoGen_AutoGenWorker (CheckPythonSyntax.Tests) ... ok
test_AutoGen_BuildEngine (CheckPythonSyntax.Tests) ... ok
test_AutoGen_DataPipe (CheckPythonSyntax.Tests) ... ok
test_AutoGen_GenC (CheckPythonSyntax.Tests) ... ok
test_AutoGen_GenDepex (CheckPythonSyntax.Tests) ... ok
test_AutoGen_GenMake (CheckPythonSyntax.Tests) ... ok
test_AutoGen_GenPcdDb (CheckPythonSyntax.Tests) ... ok
test_AutoGen_GenVar (CheckPythonSyntax.Tests) ... ok
test_AutoGen_IdfClassObject (CheckPythonSyntax.Tests) ... ok
test_AutoGen_IncludesAutoGen (CheckPythonSyntax.Tests) ... ok
test_AutoGen_InfSectionParser (CheckPythonSyntax.Tests) ... ok
test_AutoGen_ModuleAutoGen (CheckPythonSyntax.Tests) ... ok
test_AutoGen_ModuleAutoGenHelper (CheckPythonSyntax.Tests) ... ok
test_AutoGen_PlatformAutoGen (CheckPythonSyntax.Tests) ... ok
test_AutoGen_StrGather (CheckPythonSyntax.Tests) ... ok
test_AutoGen_UniClassObject (CheckPythonSyntax.Tests) ... ok
test_AutoGen_ValidCheckingInfoObject (CheckPythonSyntax.Tests) ... ok
test_AutoGen_WorkspaceAutoGen (CheckPythonSyntax.Tests) ... ok
test_AutoGen___init__ (CheckPythonSyntax.Tests) ... ok
test_BPDG_BPDG (CheckPythonSyntax.Tests) ... ok
test_BPDG_GenVpd (CheckPythonSyntax.Tests) ... ok
test_BPDG_StringTable (CheckPythonSyntax.Tests) ... ok
test_BPDG___init__ (CheckPythonSyntax.Tests) ... ok
test_Capsule_GenerateCapsule (CheckPythonSyntax.Tests) ... ok
test_Capsule_GenerateWindowsDriver (CheckPythonSyntax.Tests) ... ok
test_Capsule_WindowsCapsuleSupportHelper (CheckPythonSyntax.Tests) ... ok
test_CommonDataClass_CommonClass (CheckPythonSyntax.Tests) ... ok
test_CommonDataClass_DataClass (CheckPythonSyntax.Tests) ... ok
test_CommonDataClass_Exceptions (CheckPythonSyntax.Tests) ... ok
test_CommonDataClass_FdfClass (CheckPythonSyntax.Tests) ... ok
test_CommonDataClass___init__ (CheckPythonSyntax.Tests) ... ok
test_Common_BuildToolError (CheckPythonSyntax.Tests) ... ok
test_Common_BuildVersion (CheckPythonSyntax.Tests) ... ok
test_Common_DataType (CheckPythonSyntax.Tests) ... ok
test_Common_Edk2_Capsule_FmpPayloadHeader (CheckPythonSyntax.Tests) ... ok
test_Common_Edk2_Capsule___init__ (CheckPythonSyntax.Tests) ... ok
test_Common_Edk2___init__ (CheckPythonSyntax.Tests) ... ok
test_Common_EdkLogger (CheckPythonSyntax.Tests) ... ok
test_Common_Expression (CheckPythonSyntax.Tests) ... ok
test_Common_GlobalData (CheckPythonSyntax.Tests) ... ok
test_Common_LongFilePathOs (CheckPythonSyntax.Tests) ... ok
test_Common_LongFilePathOsPath (CheckPythonSyntax.Tests) ... ok
test_Common_LongFilePathSupport (CheckPythonSyntax.Tests) ... ok
test_Common_Misc (CheckPythonSyntax.Tests) ... ok
test_Common_MultipleWorkspace (CheckPythonSyntax.Tests) ... ok
test_Common_Parsing (CheckPythonSyntax.Tests) ... ok
test_Common_RangeExpression (CheckPythonSyntax.Tests) ... ok
test_Common_StringUtils (CheckPythonSyntax.Tests) ... ok
test_Common_TargetTxtClassObject (CheckPythonSyntax.Tests) ... ok
test_Common_ToolDefClassObject (CheckPythonSyntax.Tests) ... ok
test_Common_Uefi_Capsule_CapsuleDependency (CheckPythonSyntax.Tests) ... ok
test_Common_Uefi_Capsule_FmpAuthHeader (CheckPythonSyntax.Tests) ... ok
test_Common_Uefi_Capsule_FmpCapsuleHeader (CheckPythonSyntax.Tests) ... ok
test_Common_Uefi_Capsule_UefiCapsuleHeader (CheckPythonSyntax.Tests) ... ok
test_Common_Uefi_Capsule___init__ (CheckPythonSyntax.Tests) ... ok
test_Common_Uefi___init__ (CheckPythonSyntax.Tests) ... ok
test_Common_VariableAttributes (CheckPythonSyntax.Tests) ... ok
test_Common_VpdInfoFile (CheckPythonSyntax.Tests) ... ok
test_Common___init__ (CheckPythonSyntax.Tests) ... ok
test_Common_caching (CheckPythonSyntax.Tests) ... ok
test_Ecc_CParser3_CLexer (CheckPythonSyntax.Tests) ... ok
test_Ecc_CParser3_CParser (CheckPythonSyntax.Tests) ... ok
test_Ecc_CParser3___init__ (CheckPythonSyntax.Tests) ... ok
test_Ecc_CParser4_CLexer (CheckPythonSyntax.Tests) ... ok
test_Ecc_CParser4_CListener (CheckPythonSyntax.Tests) ... ok
test_Ecc_CParser4_CParser (CheckPythonSyntax.Tests) ... ok
test_Ecc_CParser4___init__ (CheckPythonSyntax.Tests) ... ok
test_Ecc_Check (CheckPythonSyntax.Tests) ... ok
test_Ecc_CodeFragment (CheckPythonSyntax.Tests) ... ok
test_Ecc_CodeFragmentCollector (CheckPythonSyntax.Tests) ... ok
test_Ecc_Configuration (CheckPythonSyntax.Tests) ... ok
test_Ecc_Database (CheckPythonSyntax.Tests) ... ok
test_Ecc_EccGlobalData (CheckPythonSyntax.Tests) ... ok
test_Ecc_EccMain (CheckPythonSyntax.Tests) ... ok
test_Ecc_EccToolError (CheckPythonSyntax.Tests) ... ok
test_Ecc_Exception (CheckPythonSyntax.Tests) ... ok
test_Ecc_FileProfile (CheckPythonSyntax.Tests) ... ok
test_Ecc_MetaDataParser (CheckPythonSyntax.Tests) ... ok
test_Ecc_MetaFileWorkspace_MetaDataTable (CheckPythonSyntax.Tests) ... ok
test_Ecc_MetaFileWorkspace_MetaFileParser (CheckPythonSyntax.Tests) ... ok
test_Ecc_MetaFileWorkspace_MetaFileTable (CheckPythonSyntax.Tests) ... ok
test_Ecc_MetaFileWorkspace___init__ (CheckPythonSyntax.Tests) ... ok
test_Ecc_ParserWarning (CheckPythonSyntax.Tests) ... ok
test_Ecc_Xml_XmlRoutines (CheckPythonSyntax.Tests) ... ok
test_Ecc_Xml___init__ (CheckPythonSyntax.Tests) ... ok
test_Ecc___init__ (CheckPythonSyntax.Tests) ... ok
test_Ecc_c (CheckPythonSyntax.Tests) ... ok
test_Eot_CParser3_CLexer (CheckPythonSyntax.Tests) ... ok
test_Eot_CParser3_CParser (CheckPythonSyntax.Tests) ... ok
test_Eot_CParser3___init__ (CheckPythonSyntax.Tests) ... ok
test_Eot_CParser4_CLexer (CheckPythonSyntax.Tests) ... ok
test_Eot_CParser4_CListener (CheckPythonSyntax.Tests) ... ok
test_Eot_CParser4_CParser (CheckPythonSyntax.Tests) ... ok
test_Eot_CParser4___init__ (CheckPythonSyntax.Tests) ... ok
test_Eot_CodeFragment (CheckPythonSyntax.Tests) ... ok
test_Eot_CodeFragmentCollector (CheckPythonSyntax.Tests) ... ok
test_Eot_Database (CheckPythonSyntax.Tests) ... ok
test_Eot_EotGlobalData (CheckPythonSyntax.Tests) ... ok
test_Eot_EotMain (CheckPythonSyntax.Tests) ... ok
test_Eot_EotToolError (CheckPythonSyntax.Tests) ... ok
test_Eot_FileProfile (CheckPythonSyntax.Tests) ... ok
test_Eot_Identification (CheckPythonSyntax.Tests) ... ok
test_Eot_InfParserLite (CheckPythonSyntax.Tests) ... ok
test_Eot_Parser (CheckPythonSyntax.Tests) ... ok
test_Eot_ParserWarning (CheckPythonSyntax.Tests) ... ok
test_Eot_Report (CheckPythonSyntax.Tests) ... ok
test_Eot___init__ (CheckPythonSyntax.Tests) ... ok
test_Eot_c (CheckPythonSyntax.Tests) ... ok
test_FMMT_FMMT (CheckPythonSyntax.Tests) ... ok
test_FMMT___init__ (CheckPythonSyntax.Tests) ... ok
test_FMMT_core_BinaryFactoryProduct (CheckPythonSyntax.Tests) ... ok
test_FMMT_core_BiosTree (CheckPythonSyntax.Tests) ... ok
test_FMMT_core_BiosTreeNode (CheckPythonSyntax.Tests) ... ok
test_FMMT_core_FMMTOperation (CheckPythonSyntax.Tests) ... ok
test_FMMT_core_FMMTParser (CheckPythonSyntax.Tests) ... ok
test_FMMT_core_FvHandler (CheckPythonSyntax.Tests) ... ok
test_FMMT_core_GuidTools (CheckPythonSyntax.Tests) ... ok
test_FMMT_utils_FmmtLogger (CheckPythonSyntax.Tests) ... ok
test_FMMT_utils_FvLayoutPrint (CheckPythonSyntax.Tests) ... ok
test_FirmwareStorageFormat_Common (CheckPythonSyntax.Tests) ... ok
test_FirmwareStorageFormat_FfsFileHeader (CheckPythonSyntax.Tests) ... ok
test_FirmwareStorageFormat_FvHeader (CheckPythonSyntax.Tests) ... ok
test_FirmwareStorageFormat_SectionHeader (CheckPythonSyntax.Tests) ... ok
test_FirmwareStorageFormat___init__ (CheckPythonSyntax.Tests) ... ok
test_GenFds_AprioriSection (CheckPythonSyntax.Tests) ... ok
test_GenFds_Capsule (CheckPythonSyntax.Tests) ... ok
test_GenFds_CapsuleData (CheckPythonSyntax.Tests) ... ok
test_GenFds_CompressSection (CheckPythonSyntax.Tests) ... ok
test_GenFds_DataSection (CheckPythonSyntax.Tests) ... ok
test_GenFds_DepexSection (CheckPythonSyntax.Tests) ... ok
test_GenFds_EfiSection (CheckPythonSyntax.Tests) ... ok
test_GenFds_Fd (CheckPythonSyntax.Tests) ... ok
test_GenFds_FdfParser (CheckPythonSyntax.Tests) ... ok
test_GenFds_Ffs (CheckPythonSyntax.Tests) ... ok
test_GenFds_FfsFileStatement (CheckPythonSyntax.Tests) ... ok
test_GenFds_FfsInfStatement (CheckPythonSyntax.Tests) ... ok
test_GenFds_Fv (CheckPythonSyntax.Tests) ... ok
test_GenFds_FvImageSection (CheckPythonSyntax.Tests) ... ok
test_GenFds_GenFds (CheckPythonSyntax.Tests) ... ok
test_GenFds_GenFdsGlobalVariable (CheckPythonSyntax.Tests) ... ok
test_GenFds_GuidSection (CheckPythonSyntax.Tests) ... ok
test_GenFds_OptRomFileStatement (CheckPythonSyntax.Tests) ... ok
test_GenFds_OptRomInfStatement (CheckPythonSyntax.Tests) ... ok
test_GenFds_OptionRom (CheckPythonSyntax.Tests) ... ok
test_GenFds_Region (CheckPythonSyntax.Tests) ... ok
test_GenFds_Rule (CheckPythonSyntax.Tests) ... ok
test_GenFds_RuleComplexFile (CheckPythonSyntax.Tests) ... ok
test_GenFds_RuleSimpleFile (CheckPythonSyntax.Tests) ... ok
test_GenFds_Section (CheckPythonSyntax.Tests) ... ok
test_GenFds_UiSection (CheckPythonSyntax.Tests) ... ok
test_GenFds_VerSection (CheckPythonSyntax.Tests) ... ok
test_GenFds___init__ (CheckPythonSyntax.Tests) ... ok
test_GenPatchPcdTable_GenPatchPcdTable (CheckPythonSyntax.Tests) ... ok
test_GenPatchPcdTable___init__ (CheckPythonSyntax.Tests) ... ok
test_PatchPcdValue_PatchPcdValue (CheckPythonSyntax.Tests) ... ok
test_PatchPcdValue___init__ (CheckPythonSyntax.Tests) ... ok
test_Pkcs7Sign_Pkcs7Sign (CheckPythonSyntax.Tests) ... ok
test_Rsa2048Sha256Sign_Rsa2048Sha256GenerateKeys (CheckPythonSyntax.Tests) ... ok
test_Rsa2048Sha256Sign_Rsa2048Sha256Sign (CheckPythonSyntax.Tests) ... ok
test_Split_Split (CheckPythonSyntax.Tests) ... ok
test_Split___init__ (CheckPythonSyntax.Tests) ... ok
test_Table_Table (CheckPythonSyntax.Tests) ... ok
test_Table_TableDataModel (CheckPythonSyntax.Tests) ... ok
test_Table_TableDec (CheckPythonSyntax.Tests) ... ok
test_Table_TableDsc (CheckPythonSyntax.Tests) ... ok
test_Table_TableEotReport (CheckPythonSyntax.Tests) ... ok
test_Table_TableFdf (CheckPythonSyntax.Tests) ... ok
test_Table_TableFile (CheckPythonSyntax.Tests) ... ok
test_Table_TableFunction (CheckPythonSyntax.Tests) ... ok
test_Table_TableIdentifier (CheckPythonSyntax.Tests) ... ok
test_Table_TableInf (CheckPythonSyntax.Tests) ... ok
test_Table_TablePcd (CheckPythonSyntax.Tests) ... ok
test_Table_TableQuery (CheckPythonSyntax.Tests) ... ok
test_Table_TableReport (CheckPythonSyntax.Tests) ... ok
test_Table___init__ (CheckPythonSyntax.Tests) ... ok
test_TargetTool_TargetTool (CheckPythonSyntax.Tests) ... ok
test_TargetTool___init__ (CheckPythonSyntax.Tests) ... ok
test_Trim_Trim (CheckPythonSyntax.Tests) ... ok
test_UPT_BuildVersion (CheckPythonSyntax.Tests) ... ok
test_UPT_Core_DependencyRules (CheckPythonSyntax.Tests) ... ok
test_UPT_Core_DistributionPackageClass (CheckPythonSyntax.Tests) ... ok
test_UPT_Core_FileHook (CheckPythonSyntax.Tests) ... ok
test_UPT_Core_IpiDb (CheckPythonSyntax.Tests) ... ok
test_UPT_Core_PackageFile (CheckPythonSyntax.Tests) ... ok
test_UPT_Core___init__ (CheckPythonSyntax.Tests) ... ok
test_UPT_GenMetaFile_GenDecFile (CheckPythonSyntax.Tests) ... ok
test_UPT_GenMetaFile_GenInfFile (CheckPythonSyntax.Tests) ... ok
test_UPT_GenMetaFile_GenMetaFileMisc (CheckPythonSyntax.Tests) ... ok
test_UPT_GenMetaFile_GenXmlFile (CheckPythonSyntax.Tests) ... ok
test_UPT_GenMetaFile___init__ (CheckPythonSyntax.Tests) ... ok
test_UPT_InstallPkg (CheckPythonSyntax.Tests) ... ok
test_UPT_InventoryWs (CheckPythonSyntax.Tests) ... ok
test_UPT_Library_CommentGenerating (CheckPythonSyntax.Tests) ... ok
test_UPT_Library_CommentParsing (CheckPythonSyntax.Tests) ... ok
test_UPT_Library_DataType (CheckPythonSyntax.Tests) ... ok
test_UPT_Library_ExpressionValidate (CheckPythonSyntax.Tests) ... ok
test_UPT_Library_GlobalData (CheckPythonSyntax.Tests) ... ok
test_UPT_Library_Misc (CheckPythonSyntax.Tests) ... ok
test_UPT_Library_ParserValidate (CheckPythonSyntax.Tests) ... ok
test_UPT_Library_Parsing (CheckPythonSyntax.Tests) ... ok
test_UPT_Library_StringUtils (CheckPythonSyntax.Tests) ... ok
test_UPT_Library_UniClassObject (CheckPythonSyntax.Tests) ... ok
test_UPT_Library_Xml_XmlRoutines (CheckPythonSyntax.Tests) ... ok
test_UPT_Library_Xml___init__ (CheckPythonSyntax.Tests) ... ok
test_UPT_Library___init__ (CheckPythonSyntax.Tests) ... ok
test_UPT_Logger_Log (CheckPythonSyntax.Tests) ... ok
test_UPT_Logger_StringTable (CheckPythonSyntax.Tests) ... ok
test_UPT_Logger_ToolError (CheckPythonSyntax.Tests) ... ok
test_UPT_Logger___init__ (CheckPythonSyntax.Tests) ... ok
test_UPT_MkPkg (CheckPythonSyntax.Tests) ... ok
test_UPT_Object_POM_CommonObject (CheckPythonSyntax.Tests) ... ok
test_UPT_Object_POM_ModuleObject (CheckPythonSyntax.Tests) ... ok
test_UPT_Object_POM_PackageObject (CheckPythonSyntax.Tests) ... ok
test_UPT_Object_POM___init__ (CheckPythonSyntax.Tests) ... ok
test_UPT_Object_Parser_DecObject (CheckPythonSyntax.Tests) ... ok
test_UPT_Object_Parser_InfBinaryObject (CheckPythonSyntax.Tests) ... ok
test_UPT_Object_Parser_InfBuildOptionObject (CheckPythonSyntax.Tests) ... ok
test_UPT_Object_Parser_InfCommonObject (CheckPythonSyntax.Tests) ... ok
test_UPT_Object_Parser_InfDefineCommonObject (CheckPythonSyntax.Tests) ... ok
test_UPT_Object_Parser_InfDefineObject (CheckPythonSyntax.Tests) ... ok
test_UPT_Object_Parser_InfDepexObject (CheckPythonSyntax.Tests) ... ok
test_UPT_Object_Parser_InfGuidObject (CheckPythonSyntax.Tests) ... ok
test_UPT_Object_Parser_InfHeaderObject (CheckPythonSyntax.Tests) ... ok
test_UPT_Object_Parser_InfLibraryClassesObject (CheckPythonSyntax.Tests) ... ok
test_UPT_Object_Parser_InfMisc (CheckPythonSyntax.Tests) ... ok
test_UPT_Object_Parser_InfPackagesObject (CheckPythonSyntax.Tests) ... ok
test_UPT_Object_Parser_InfPcdObject (CheckPythonSyntax.Tests) ... ok
test_UPT_Object_Parser_InfPpiObject (CheckPythonSyntax.Tests) ... ok
test_UPT_Object_Parser_InfProtocolObject (CheckPythonSyntax.Tests) ... ok
test_UPT_Object_Parser_InfSoucesObject (CheckPythonSyntax.Tests) ... ok
test_UPT_Object_Parser_InfUserExtensionObject (CheckPythonSyntax.Tests) ... ok
test_UPT_Object_Parser___init__ (CheckPythonSyntax.Tests) ... ok
test_UPT_Object___init__ (CheckPythonSyntax.Tests) ... ok
test_UPT_Parser_DecParser (CheckPythonSyntax.Tests) ... ok
test_UPT_Parser_DecParserMisc (CheckPythonSyntax.Tests) ... ok
test_UPT_Parser_InfAsBuiltProcess (CheckPythonSyntax.Tests) ... ok
test_UPT_Parser_InfBinarySectionParser (CheckPythonSyntax.Tests) ... ok
test_UPT_Parser_InfBuildOptionSectionParser (CheckPythonSyntax.Tests) ... ok
test_UPT_Parser_InfDefineSectionParser (CheckPythonSyntax.Tests) ... ok
test_UPT_Parser_InfDepexSectionParser (CheckPythonSyntax.Tests) ... ok
test_UPT_Parser_InfGuidPpiProtocolSectionParser (CheckPythonSyntax.Tests) ... ok
test_UPT_Parser_InfLibrarySectionParser (CheckPythonSyntax.Tests) ... ok
test_UPT_Parser_InfPackageSectionParser (CheckPythonSyntax.Tests) ... ok
test_UPT_Parser_InfParser (CheckPythonSyntax.Tests) ... ok
test_UPT_Parser_InfParserMisc (CheckPythonSyntax.Tests) ... ok
test_UPT_Parser_InfPcdSectionParser (CheckPythonSyntax.Tests) ... ok
test_UPT_Parser_InfSectionParser (CheckPythonSyntax.Tests) ... ok
test_UPT_Parser_InfSourceSectionParser (CheckPythonSyntax.Tests) ... ok
test_UPT_Parser___init__ (CheckPythonSyntax.Tests) ... ok
test_UPT_PomAdapter_DecPomAlignment (CheckPythonSyntax.Tests) ... ok
test_UPT_PomAdapter_InfPomAlignment (CheckPythonSyntax.Tests) ... ok
test_UPT_PomAdapter_InfPomAlignmentMisc (CheckPythonSyntax.Tests) ... ok
test_UPT_PomAdapter___init__ (CheckPythonSyntax.Tests) ... ok
test_UPT_ReplacePkg (CheckPythonSyntax.Tests) ... ok
test_UPT_RmPkg (CheckPythonSyntax.Tests) ... ok
test_UPT_TestInstall (CheckPythonSyntax.Tests) ... ok
test_UPT_UPT (CheckPythonSyntax.Tests) ... ok
test_UPT_UnitTest_CommentGeneratingUnitTest (CheckPythonSyntax.Tests) ... ok
test_UPT_UnitTest_CommentParsingUnitTest (CheckPythonSyntax.Tests) ... ok
test_UPT_UnitTest_DecParserTest (CheckPythonSyntax.Tests) ... ok
test_UPT_UnitTest_DecParserUnitTest (CheckPythonSyntax.Tests) ... ok
test_UPT_UnitTest_InfBinarySectionTest (CheckPythonSyntax.Tests) ... ok
test_UPT_Xml_CommonXml (CheckPythonSyntax.Tests) ... ok
test_UPT_Xml_GuidProtocolPpiXml (CheckPythonSyntax.Tests) ... ok
test_UPT_Xml_IniToXml (CheckPythonSyntax.Tests) ... ok
test_UPT_Xml_ModuleSurfaceAreaXml (CheckPythonSyntax.Tests) ... ok
test_UPT_Xml_PackageSurfaceAreaXml (CheckPythonSyntax.Tests) ... ok
test_UPT_Xml_PcdXml (CheckPythonSyntax.Tests) ... ok
test_UPT_Xml_XmlParser (CheckPythonSyntax.Tests) ... ok
test_UPT_Xml_XmlParserMisc (CheckPythonSyntax.Tests) ... ok
test_UPT_Xml___init__ (CheckPythonSyntax.Tests) ... ok
test_Workspace_BuildClassObject (CheckPythonSyntax.Tests) ... ok
test_Workspace_DecBuildData (CheckPythonSyntax.Tests) ... ok
test_Workspace_DscBuildData (CheckPythonSyntax.Tests) ... ok
test_Workspace_InfBuildData (CheckPythonSyntax.Tests) ... ok
test_Workspace_MetaDataTable (CheckPythonSyntax.Tests) ... ok
test_Workspace_MetaFileCommentParser (CheckPythonSyntax.Tests) ... ok
test_Workspace_MetaFileParser (CheckPythonSyntax.Tests) ... ok
test_Workspace_MetaFileTable (CheckPythonSyntax.Tests) ... ok
test_Workspace_WorkspaceCommon (CheckPythonSyntax.Tests) ... ok
test_Workspace_WorkspaceDatabase (CheckPythonSyntax.Tests) ... ok
test_Workspace___init__ (CheckPythonSyntax.Tests) ... ok
test_build_BuildReport (CheckPythonSyntax.Tests) ... ok
test_build___init__ (CheckPythonSyntax.Tests) ... ok
test_build_build (CheckPythonSyntax.Tests) ... ok
test_build_buildoptions (CheckPythonSyntax.Tests) ... ok
test_sitecustomize (CheckPythonSyntax.Tests) ... ok
test_tests_Split_test_split (CheckPythonSyntax.Tests) ... ok
test32bitUnicodeCharInUtf8Comment (CheckUnicodeSourceFiles.Tests) ... ok
test32bitUnicodeCharInUtf8File (CheckUnicodeSourceFiles.Tests) ... ok
testSupplementaryPlaneUnicodeCharInUtf16File (CheckUnicodeSourceFiles.Tests) ... ok
testSurrogatePairUnicodeCharInUtf16File (CheckUnicodeSourceFiles.Tests) ... ok
testSurrogatePairUnicodeCharInUtf8File (CheckUnicodeSourceFiles.Tests) ... ok
testSurrogatePairUnicodeCharInUtf8FileWithBom (CheckUnicodeSourceFiles.Tests) ... ok
testUtf16InUniFile (CheckUnicodeSourceFiles.Tests) ... ok
testValidUtf8File (CheckUnicodeSourceFiles.Tests) ... ok
testValidUtf8FileWithBom (CheckUnicodeSourceFiles.Tests) ... ok

----------------------------------------------------------------------
Ran 301 tests in 2.035s

OK
make[1]: Leaving directory '/root/src/edk2/BaseTools/Tests'
make: Leaving directory '/root/src/edk2/BaseTools'
root@boot-Standard-PC-Q35-ICH9-2009:~/src/edk2# 

### Command

```  
. edksetup.sh
```
**. (dot):** 

This is a shell built-in command that is used to run commands from a script in the current shell environment. When you run a script using . or source, it executes the commands in the current shell rather than spawning a new subshell. In this case, it's used to execute the commands in the edksetup.sh script within the current shell.

**edksetup.sh:**

This is a shell script provided by the EDK II framework. It typically sets up the necessary environment variables and configurations required for building UEFI firmware with the EDK II tools.

### Output

root@boot-Standard-PC-Q35-ICH9-2009:~/src/edk2# . edksetup.sh
Using EDK2 in-source Basetools
WORKSPACE: /root/src/edk2
EDK_TOOLS_PATH: /root/src/edk2/BaseTools
CONF_PATH: /root/src/edk2/Conf
Copying $EDK_TOOLS_PATH/Conf/build_rule.template
     to /root/src/edk2/Conf/build_rule.txt
Copying $EDK_TOOLS_PATH/Conf/tools_def.template
     to /root/src/edk2/Conf/tools_def.txt
Copying $EDK_TOOLS_PATH/Conf/target.template
     to /root/src/edk2/Conf/target.txt
root@boot-Standard-PC-Q35-ICH9-2009:~/src/edk2# 

### Command

```   
export EDK_TOOLS_PATH=$HOME/src/edk2/BaseTools
```
**export:** 

This command is used to set an environment variable in the shell.

**EDK_TOOLS_PATH:**

This is the name of the environment variable being set. It represents the path to the BaseTools directory in the EDK II framework.

**$HOME/src/edk2/BaseTools:**

This is the value assigned to the EDK_TOOLS_PATH variable. $HOME is a shell variable that represents the user's home directory. So, this command sets EDK_TOOLS_PATH to the absolute path of the BaseTools directory within the user's home directory.

### Output

root@boot-Standard-PC-Q35-ICH9-2009:~/src/edk2# export EDK_TOOLS_PATH=$HOME/src/edk2/BaseTools
root@boot-Standard-PC-Q35-ICH9-2009:~/src/edk2# 

### Command

```   
echo $EDK_TOOLS_PATH
```
**echo:** This command is used to print the value of a variable or a specified string to the terminal.

**$EDK_TOOLS_PATH:**

This is a reference to the EDK_TOOLS_PATH environment variable. The $ sign is used to indicate that the following text is the name of a variable, and the shell should substitute it with its current value.

### Output

root@boot-Standard-PC-Q35-ICH9-2009:~/src/edk2# echo $EDK_TOOLS_PATH
/root/src/edk2/BaseTools
root@boot-Standard-PC-Q35-ICH9-2009:~/src/edk2# 

### Command

```   
. edksetup.sh BaseTools
```
**. (dot):**

This is a shell built-in command used to execute commands from a script within the current shell environment. It is also known as the "source" command. When you run a script using . or source, it runs the commands in the current shell instead of creating a new shell.

**edksetup.sh:**

This is a shell script provided by the EDK II framework. It is typically used to set up the environment variables and configurations required for building UEFI firmware with the EDK II tools.

**BaseTools:**

This argument is passed to the edksetup.sh script, and it likely specifies a subcomponent or submodule of the EDK II framework, such as the "BaseTools" submodule. It indicates which specific components need to be configured.

### Output

root@boot-Standard-PC-Q35-ICH9-2009:~/src/edk2# . edksetup.sh BaseTools
Loading previous configuration from /root/src/edk2/Conf/BuildEnv.sh
Using EDK2 in-source Basetools
WORKSPACE: /root/src/edk2
EDK_TOOLS_PATH: /root/src/edk2/BaseTools
CONF_PATH: /root/src/edk2/Conf
root@boot-Standard-PC-Q35-ICH9-2009:~/src/edk2# 

### Command

```   
cp Conf/target.txt Conf/target.org
```
**cp:**

This is the command for copying files or directories.

**Conf/target.txt:**

This is the source file. It specifies the file named target.txt in the Conf directory.

**Conf/target.org:**

This is the destination file. It specifies the file named target.org in the Conf directory.

#### Output

root@boot-Standard-PC-Q35-ICH9-2009:~/src/edk2# cp Conf/target.txt Conf/target.org
root@boot-Standard-PC-Q35-ICH9-2009:~/src/edk2# 

### Command

```   
nano Conf/target.txt
```
**nano:**

This is the name of the text editor. Nano is a simple, command-line-based text editor that is easy to use for basic text editing tasks.

**Conf/target.txt:**

This specifies the file to be edited. It indicates the file named target.txt located in the Conf directory.

### Command

```   
diff Conf/target.txt Conf/target.org
```
**diff:** 

This is the command for performing file comparisons.

**Conf/target.txt:** 

This is the first file for comparison. It specifies the file named target.txt in the Conf directory.

**Conf/target.org:**

This is the second file for comparison. It specifies the file named target.org in the Conf directory.

### Ouptut
root@boot-Standard-PC-Q35-ICH9-2009:~/src/edk2# diff Conf/target.txt Conf/target.org
20,21c20,21
< #ACTIVE_PLATFORM       = EmulatorPkg/EmulatorPkg.dsc
< ACTIVE_PLATFORM       = MdeModulePkg/MdeModulePkg.dsc

---
> ACTIVE_PLATFORM       = EmulatorPkg/EmulatorPkg.dsc
> 
44,45c44 
< #TARGET_ARCH           = IA32
< TARGET_ARCH           = X64
---
> TARGET_ARCH           = IA32
55,56c54,55
< #TOOL_CHAIN_TAG        = VS2015x86
< TOOL_CHAIN_TAG        = GCC5
---
> TOOL_CHAIN_TAG        = VS2015x86
> 
root@boot-Standard-PC-Q35-ICH9-2009:~/src/edk2#

### Command

```   
ls MdeModulePkg/Application/HelloWorld/
```
**ls:**

This is the command for listing files and directories.

**MdeModulePkg/Application/HelloWorld/:**

This is the directory path for which you want to list the contents. It specifies the "HelloWorld" directory within the "Application" directory inside the "MdeModulePkg" directory.

### Output

root@boot-Standard-PC-Q35-ICH9-2009:~/src/edk2# ls MdeModulePkg/Application/HelloWorld/
HelloWorld.c  HelloWorldExtra.uni  HelloWorld.inf  HelloWorldStr.uni  HelloWorld.uni
root@boot-Standard-PC-Q35-ICH9-2009:~/src/edk2#

### Command

```   
 cd MdeModulePkg/Application/HelloWorld/
```
 Change directory to MdeModulePkg/Application/HelloWorld/

### Output

root@boot-Standard-PC-Q35-ICH9-2009:~/src/edk2#  cd MdeModulePkg/Application/HelloWorld/
root@boot-Standard-PC-Q35-ICH9-2009:~/src/edk2/MdeModulePkg/Application/HelloWorld# 

### Command

```
ls
```
**ls:**
List the files within MdeModulePkg/Application/HelloWorld/ directory.

### Output

root@boot-Standard-PC-Q35-ICH9-2009:~/src/edk2/MdeModulePkg/Application/HelloWorld# ls
HelloWorld.c  HelloWorldExtra.uni  HelloWorld.inf  HelloWorldStr.uni  HelloWorld.uni
root@boot-Standard-PC-Q35-ICH9-2009:~/src/edk2/MdeModulePkg/Application/HelloWorld#

### Command

``` 
cat HelloWorld.c
```
**cat:**

This is the command for concatenating and displaying the content of files.

**HelloWorld.c:** 

This is the file whose content you want to display. 

### Output

root@boot-Standard-PC-Q35-ICH9-2009:~/src/edk2/MdeModulePkg/Application/HelloWorld# cat HelloWorld.c
/** @file
  This sample application bases on HelloWorld PCD setting
  to print "UEFI Hello World!" to the UEFI Console.

  Copyright (c) 2006 - 2018, Intel Corporation. All rights reserved.<BR>
  SPDX-License-Identifier: BSD-2-Clause-Patent

**/

#include <Uefi.h>
#include <Library/PcdLib.h>
#include <Library/UefiLib.h>
#include <Library/UefiApplicationEntryPoint.h>

//
// String token ID of help message text.
// Shell supports to find help message in the resource section of an application image if
// .MAN file is not found. This global variable is added to make build tool recognizes
// that the help string is consumed by user and then build tool will add the string into
// the resource section. Thus the application can use '-?' option to show help message in
// Shell.
//
GLOBAL_REMOVE_IF_UNREFERENCED EFI_STRING_ID  mStringHelpTokenId = STRING_TOKEN (STR_HELLO_WORLD_HELP_INFORMATION);

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
  // Three PCD type (FeatureFlag, UINT32 and String) are used as the sample.
  //
  if (FeaturePcdGet (PcdHelloWorldPrintEnable)) {
    for (Index = 0; Index < PcdGet32 (PcdHelloWorldPrintTimes); Index++) {
      //
      // Use UefiLib Print API to print string to UEFI console
      //
      Print ((CHAR16 *)PcdGetPtr (PcdHelloWorldPrintString));
    }
  }

  return EFI_SUCCESS;
}
root@boot-Standard-PC-Q35-ICH9-2009:~/src/edk2/MdeModulePkg/Application/HelloWorld# 

### Command

```
nano HelloWorld.c
```
**nano:**

This is the name of the text editor. Nano is a simple, command-line-based text editor that is easy to use for basic text editing tasks.

**HelloWorld.c:**

This is the file you want to edit. Paste the below code in the HelloWorld.c file to get desire output.

### Output

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
      Print(L"My name is Nitesh.This is my first bootloader.");

      // Stall for a while (15 seconds) to see the output on the console
      SystemTable->BootServices->Stall(15 * 1000000);  // 15 seconds in microseconds
    }
  }

  return EFI_SUCCESS;

### Command

```   
cd ~/src/edk2/
```
**cd ~/src/edk2/:**

Change directory to ~/src/edk2/

```   
build
```
The build command is used to initiate the build process for the UEFI project. The *.dsc file specifies the project configuration, dependencies, and build settings.

### Output

- Done -
Build end time: 15:32:45, Feb.21 2024
Build total time: 00:03:11

root@boot-Standard-PC-Q35-ICH9-2009:~/src/edk2#

### Command 

```
ls Build/MdeModule/DEBUG_GCC5/X64/HelloWorld.*
```
List all the files and diectories in the Build/MdeModule/DEBUG_GCC5/X64/HelloWorld.*path whose name is HelloWorld.

### Output

root@boot-Standard-PC-Q35-ICH9-2009:~/src/edk2# ls Build/MdeModule/DEBUG_GCC5/X64/HelloWorld.*
Build/MdeModule/DEBUG_GCC5/X64/HelloWorld.debug  Build/MdeModule/DEBUG_GCC5/X64/HelloWorld.efi
root@boot-Standard-PC-Q35-ICH9-2009:~/src/edk2# 

### Command

```
mkdir /boot/efi/EFI/nitesh_booting
```
Create a directory named nitesh_booting in /boot/efi/EFI/

### Output

root@boot-Standard-PC-Q35-ICH9-2009:~/src/edk2# mkdir /boot/efi/EFI/nitesh_booting
root@boot-Standard-PC-Q35-ICH9-2009:~/src/edk2# 

```
cp Build/MdeModule/DEBUG_GCC5/X64/HelloWorld.efi /boot/efi/EFI/nitesh_booting
```
Copy the HelloWorld.efi file from  Build/MdeModule/DEBUG_GCC5/X64/HelloWorld.efi into /boot/efi/EFI/nitesh_booting.

### Output

root@boot-Standard-PC-Q35-ICH9-2009:~/src/edk2# cp Build/MdeModule/DEBUG_GCC5/X64/HelloWorld.efi /boot/efi/EFI/nitesh_booting
root@boot-Standard-PC-Q35-ICH9-2009:~/src/edk2# 

### Command

```
tree /boot/efi/
```
Showing directory and files it contains in /boot/efi/ path.

### Output

root@boot-Standard-PC-Q35-ICH9-2009:~/src/edk2# tree /boot/efi/
/boot/efi/
└── EFI
    ├── BOOT
    │   ├── BOOTX64.EFI
    │   ├── fbx64.efi
    │   └── mmx64.efi
    ├── nitesh_booting
    │   └── HelloWorld.efi
    └── ubuntu
        ├── BOOTX64.CSV
        ├── grub.cfg
        ├── grubx64.efi
        ├── mmx64.efi
        └── shimx64.efi

4 directories, 9 files

### Command

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

### Output

root@boot-Standard-PC-Q35-ICH9-2009:~/src/edk2 efibootmgr -c -d /dev/vda1 -p 1 -L HelloWorldLoader -l \\EFI\\nitesh_booting\\HelloWorld.efi
BootCurrent: 0004
Timeout: 3 seconds
BootOrder: 0001,0004,0003,0000,0002
Boot0000* UiApp
Boot0002* EFI Internal Shell
Boot0003* UEFI Misc Device
Boot0004* ubuntu
Boot0001* HelloWorldLoader
root@boot-Standard-PC-Q35-ICH9-2009:~/src/edk2# 

#### Reboot system and go to boot manager

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/3e343678-b3c2-4175-89b7-b514d167ec5a)


Select HelloLodaer

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/4a5d2a55-fe38-4cea-8a02-544009325b9d)

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/e4e22882-a19c-417f-a586-543a717a4f62)
