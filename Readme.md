mount | grep efi

sudo apt install tree
    
tree /boot/efi/
    
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
