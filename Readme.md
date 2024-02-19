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


apt install build-essential uuid-dev iasl git  nasm  python-is-python3
    
cd /home/boot/Downloads/
    
wget -c http://security.ubuntu.com/ubuntu/pool/universe/n/nasm/nasm_2.15.05-1_amd64.deb
    
apt install /home/vbg/Downloads/nasm_2.15.05-1_amd64.deb
    
apt install /home/boot/Downloads/nasm_2.15.05-1_amd64.deb
    
nasm --version
    
mkdir ~/src
   
cd ~/
   
cd ~/src/
   
git clone https://github.com/tianocore/edk2
   
cd edk2/
   
git checkout tags/edk2-stable202208
   
git switch -c niteshboot
   
git branch
   
git submodule update --init
   
make -C BaseTools
   
. edksetup.sh
   
make -C BaseTools
   
export EDK_TOOLS_PATH=$HOME/src/edk2/BaseTools
   
echo $EDK_TOOLS_PATH
   
. edksetup.sh BaseTools
   
cp Conf/target.txt Conf/target.org
   
nano Conf/target.txt
   
diff Conf/target.txt Conf/target.org
   
ls MdeModulePkg/Application/HelloWorld/
   
 cd MdeModulePkg/Application/HelloWorld/
   
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
