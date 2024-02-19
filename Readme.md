![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/e537e972-911a-4737-86c8-b3b9e6e13a82)
```
sudo apt install tree
```
**sudo :**

It stands for "superuser do" and permits user to execute a command as the superuser

**apt:**

This is the package management tool used on Debian-based Linux distributions, including Ubuntu. It is used to handle the installation, removal, and management of software packages.

**install:**

This is the APT command used to install software packages.

**tree:**

This is the name of the package that you want to install. In this case, it refers to a command-line utility called "tree" that displays the contents of a directory in a tree-like structure.

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/aade4cc9-f6c1-4e0e-b86a-597cea7f5815)

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

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/7e9b4ab5-e8d7-44c2-af8a-c4daf7ba2604)

```  
tree /boot/efi/
```
**tree:**

This is the command-line utility used to display the directory structure in a tree-like format. It recursively lists the contents of directories and subdirectories, showing the hierarchical relationship of files and directories.

**/boot/efi/:**

This is the path to the directory for which you want to display the tree structure. In this case, it refers to the EFI (Extensible Firmware Interface) partition's "/boot/efi/" directory. On many Linux systems, this directory is used for storing boot-related files, especially on systems that use UEFI (Unified Extensible Firmware Interface) for booting.

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/3c883ecc-f97a-4169-8567-d0b0930c4b05)

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

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/cca64869-cbed-4d90-bec4-8b2135952252)

```
cd /home/boot/Downloads/
```
**cd:** 

This stands for "change directory." It is a command used to change the current working directory in the command line.

**/home/boot/Downloads/:**

This is the path to the directory you want to change into. In this case, it specifies the absolute path to the "Downloads" directory located within the "boot" user's home directory.

 ```
wget -c http://security.ubuntu.com/ubuntu/pool/universe/n/nasm/nasm_2.15.05-1_amd64.deb
```
**wget:**

This is a command-line utility for downloading files from the web. It is often used to retrieve files and content from web servers.

**-c:**

This option stands for "continue." If the download is interrupted or if the file already exists locally, this option allows wget to resume the download from where it left off.

**http://security.ubuntu.com/ubuntu/pool/universe/n/nasm/nasm_2.15.05-1_amd64.deb:**

This is the URL of the Debian package file you want to download. In this case, it is the NASM (Netwide Assembler) package with version 2.15.05-1 for the AMD64 architecture.
    
```
apt install /home/boot/Downloads/nasm_2.15.05-1_amd64.deb
```
**apt:**

This is the package management tool used on Debian-based Linux distributions, including Ubuntu. It is used to handle the installation, removal, and management of software packages.

**install:**

This is the APT command used to install software packages.

**/home/boot/Downloads/nasm_2.15.05-1_amd64.deb:**

This is the path to the Debian package file you want to install. In this case, it specifies the absolute path to the NASM (Netwide Assembler) package with version 2.15.05-1 for the AMD64 architecture.
```
nasm --version
```
**nasm:**

This is the command for the NASM assembler. NASM is a popular assembler used for x86 and x86-64 architectures.

**--version:**

It is used to display version information. 
```
mkdir ~/src
```
**mkdir:**

This stands for "make directory." It is a command in Unix-like operating systems used to create a new directory or folder.

**~/src:**

This specifies the path where the new directory should be created. The tilde (~) is a shorthand notation for the user's home directory. So, ~/src refers to a directory named "src" within the user's home directory.   
```   
cd ~/src/
```
**cd:** 

This stands for "change directory." It is a command used to change the current working directory in the command line.

**~/src:**

This specifies the path where the new directory should be created. The tilde (~) is a shorthand notation for the user's home directory. So, ~/src refers to a directory named "src" within the user's home directory. 
```   
git clone https://github.com/tianocore/edk2
```
**git:** 

This is the command-line interface for the Git version control system. Git is used for tracking changes in source code during software development.

**clone:**

This is a Git command used to create a copy or clone of a remote Git repository.

**https://github.com/tianocore/edk2:** 

This is the URL of the Git repository you want to clone. In this case, it's the EDK II (Extensible Firmware Interface Development Kit) repository hosted on GitHub. EDK II is an open-source project that provides a set of development tools and firmware libraries for UEFI (Unified Extensible Firmware Interface) development.


 ``` 
cd edk2/
 ```
```
git checkout tags/edk2-stable202208
```
```
git switch -c niteshboot
```
```   
git branch
```
```   
git submodule update --init
```
```   
make -C BaseTools
```
```  
. edksetup.sh
```
```
make -C BaseTools
```
```   
export EDK_TOOLS_PATH=$HOME/src/edk2/BaseTools
```
```   
echo $EDK_TOOLS_PATH
```
```   
. edksetup.sh BaseTools
```
```   
cp Conf/target.txt Conf/target.org
```
```   
nano Conf/target.txt
```
```   
diff Conf/target.txt Conf/target.org
```
```   
ls MdeModulePkg/Application/HelloWorld/
```
```   
 cd MdeModulePkg/Application/HelloWorld/
  ``` 
ls
   
cat HelloWorld.c
   
nano HelloWorld.c
   
cd ..
   
cd ~/src/edk2/
   
build
   
ls Build/MdeModule/DEBUG_GCC5/X64/HelloWorld.*
   
mkdir /boot/efi/EFI/nitesh_booting
   
cp Build/MdeModule/DEBUG_GCC5/X64/HelloWorld.efi /boot/efi/EFI/nitesh_booting
   
tree /boot/efi/
   
sudo efibootmgr -c -d /dev/vda1 -p 1 -L HelloWorldLoader -l \\EFI\\helloloader\\HelloWorld.efi
   
efibootmgr -c -d /dev/vda1 -p 1 -L HelloWorldLoader -l \\EFI\\nitesh_booting\\HelloWorld.efi

`exit`
