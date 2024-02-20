# System Requiremtnts :

**OS:-** Ubuntu 23.10

**RAM:-** 2GB or more.

**CPU:-** 2 or more.

**Storage**:- 20GB or more.

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
