Enable Boot Menu

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/e537e972-911a-4737-86c8-b3b9e6e13a82)

Disable Secure Boot from Boot Manager

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/fcb470d5-2609-47e8-b76c-e12da7fb8208)


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

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/9334c207-a48e-4b2a-93a8-1357eaf69a13)

 ``` 
cd edk2/
 ```
**cd:** 

This stands for "change directory." It is a command used to change the current working directory in the command line.

**edk2/:** 

This specifies the directory you want to change into. In this case, it's the "edk2" directory.

```
git checkout tags/edk2-stable202208
```
**git:** 

This is the command-line interface for the Git version control system. Git is used for tracking changes in source code during software development.

**checkout:** This is a Git command used for switching branches or tags. In this case, it is used to switch to a specific tag.

tags/edk2-stable202208: This specifies the tag you want to check out. Tags in Git are used to label specific points in the commit history, often denoting releases or important milestones.

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/de2e6d3f-501e-412f-ba76-2c607478e6ff)

```
git switch -c niteshboot
```
![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/9e878014-bbe3-4457-b200-143f1ea58082)

```   
git branch
```
![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/8c8c7fde-b98f-4bbb-a1d6-112edc98bda3)


```   
git submodule update --init
```
![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/8c68c54c-5abb-4898-beca-16acc115896d)

```   
make -C BaseTools
```
![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/1ef1a0b4-afb8-443e-9c6e-c66417a40659)

```  
. edksetup.sh
```
![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/48e8fc4d-920c-4cda-abb5-27a9ef391901)

```
make -C BaseTools
```
```   
export EDK_TOOLS_PATH=$HOME/src/edk2/BaseTools
```
![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/7432f6ea-0933-44c2-abbd-c83892938f17)

```   
echo $EDK_TOOLS_PATH
```
![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/ccff8c29-9a5b-4eca-9774-43ec0eb679bd)

```   
. edksetup.sh BaseTools
```
![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/aa819c39-06f0-46fd-8955-7f948a34f116)

```   
cp Conf/target.txt Conf/target.org
```
![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/d8566788-6f60-49d3-834d-288887ade855)

```   
nano Conf/target.txt
```
```   
diff Conf/target.txt Conf/target.org
```
![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/dca618b7-2463-4785-9445-a69bebe0527a)

```   
ls MdeModulePkg/Application/HelloWorld/
```
![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/a2168eb2-ea1d-4103-83e9-b498690fb89e)

```   
 cd MdeModulePkg/Application/HelloWorld/
```
![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/ba3706a7-1e9b-4369-bff2-21757df11c47)
```
ls
```
![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/d72a0cdd-4d0e-4e19-af7b-c0d29e41cb1c)

   
cat HelloWorld.c
```   
nano HelloWorld.c
```
```
/** @file
  This sample application bases on HelloWorld PCD setting
  to print "UEFI Hello World!" to the UEFI Console.

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

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/a6902140-4369-4b5f-94ec-817cc5940948)

```   
build
```
![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/d63af7f7-e6d8-40aa-9c1d-ca5ed4e81c99)

```
ls Build/MdeModule/DEBUG_GCC5/X64/HelloWorld.*
```
![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/f3441473-a8ea-4555-9bca-977bcacc34f9)
```
mkdir /boot/efi/EFI/nitesh_booting
```

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/5b2ebccf-589e-4e4c-8f22-0fbfa9e4fc3b)
```
cp Build/MdeModule/DEBUG_GCC5/X64/HelloWorld.efi /boot/efi/EFI/nitesh_booting
```
![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/a3e7cd58-2137-420e-a46a-72883bbc55ea)
```
tree /boot/efi/
```
![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/b57f99f8-9721-4bc6-9c3f-04c2146e05b9)
   
sudo efibootmgr -c -d /dev/vda1 -p 1 -L HelloWorldLoader -l \\EFI\\helloloader\\HelloWorld.efi
```
efibootmgr -c -d /dev/vda1 -p 1 -L HelloWorldLoader -l \\EFI\\nitesh_booting\\HelloWorld.efi
```
![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/6288ddd7-e150-4a9b-ae2d-9c203a37fc58)

`exit`

![image](https://github.com/gitnitesh1995/UEFI-Bootloader/assets/61899084/84b88ed9-516e-4826-a265-b713d7858b86)

