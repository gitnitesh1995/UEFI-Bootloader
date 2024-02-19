root@boot-Standard-PC-Q35-ICH9-2009:/home/boot# history

    1  mount | grep efi
    2  sudo apt install tree
    3  tree /boot/efi/
    4  apt install build-essential uuid-dev iasl git  nasm  python-is-python3
    5  cd /home/boot/Downloads/
    6  wget -c http://security.ubuntu.com/ubuntu/pool/universe/n/nasm/nasm_2.15.05-1_amd64.deb
    7  apt install /home/vbg/Downloads/nasm_2.15.05-1_amd64.deb
    8  apt install /home/boot/Downloads/nasm_2.15.05-1_amd64.deb
    9  nasm --version
   10  mkdir ~/src
   11  cd ~/
   12  cd ~/src/
   13  git clone https://github.com/tianocore/edk2
   14  cd edk2/
   15  git checkout tags/edk2-stable202208
   16  git switch -c niteshboot
   17  git branch
   18  git submodule update --init
   19  make -C BaseTools
   20  . edksetup.sh
   21  make -C BaseTools
   22  export EDK_TOOLS_PATH=$HOME/src/edk2/BaseTools
   23  echo $EDK_TOOLS_PATH
   24  . edksetup.sh BaseTools
   25  cp Conf/target.txt Conf/target.org
   26  nano Conf/target.txt
   27  diff Conf/target.txt Conf/target.org
   28  ls MdeModulePkg/Application/HelloWorld/
   29  cd MdeModulePkg/Application/HelloWorld/
   30  ls
   31  cat HelloWorld.c
   32  nano HelloWorld.c
   33  cd ..
   34  cd ~/src/edk2/
   35  build
   36  ls Build/MdeModule/DEBUG_GCC5/X64/HelloWorld.*
   37  mkdir /boot/efi/EFI/nitesh_booting
   38  cp Build/MdeModule/DEBUG_GCC5/X64/HelloWorld.efi /boot/efi/EFI/nitesh_booting
   39  tree /boot/efi/
   40  sudo efibootmgr -c -d /dev/vda1 -p 1 -L HelloWorldLoader -l \\EFI\\helloloader\\HelloWorld.efi
   41  efibootmgr -c -d /dev/vda1 -p 1 -L HelloWorldLoader -l \\EFI\\nitesh_booting\\HelloWorld.efi
   42  exit
   43  history
root@boot-Standard-PC-Q35-ICH9-2009:/home/boot# 
