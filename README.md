# Vsdquadron Mini

## Task-1
+ Install Oracle Virtual Machine
+ install Ubuntu 20.04 on VM
+ ### Install Riscv GNU Toolchain

```
  git clone https://github.com/riscv/riscv-gnu-toolchain
  sudo apt-get install autoconf automake autotools-dev curl python3 python3-pip libmpc-dev libmpfr-dev libgmp-dev gawk build-essential bison flex texinfo gperf libtool   
  patchutils bc zlib1g-dev libexpat-dev ninja-build git cmake libglib2.0-dev
  ./configure --prefix=/opt/riscv
  make
  ```
![image](https://github.com/Amrutha3515/RISC-V/assets/150571663/9a6bbd49-9c43-4ec2-8590-fdd2ba1445b6)



+ ### Install Yosys
```
git clone git@github.com:YosysHQ/yosys.git
sudo apt-get install build-essential clang bison flex \
	libreadline-dev gawk tcl-dev libffi-dev git \
	graphviz xdot pkg-config python3 libboost-system-dev \
	libboost-python-dev libboost-filesystem-dev zlib1g-dev
cd yosys
mkdir build
cd build
make -f ../Makefile -j
```
![image](https://github.com/Amrutha3515/RISC-V/assets/150571663/c4bb02b9-5454-4a3d-8dc1-da1420c8f27e)

+ ### Install Iverilog
  ```
  sudo apt-get install iverilog
  ```
  ![image](https://github.com/Amrutha3515/RISC-V/assets/150571663/1e635984-51f3-4533-b73b-646754abd8bd)

+ ### Install gtkwave
```
sudo apt-get install gtkwave
```
![image](https://github.com/Amrutha3515/RISC-V/assets/150571663/9122d695-2e38-40f3-8949-601ebab8d46b)








