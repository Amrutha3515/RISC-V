# Vsdquadron Mini
## Task-1
+ ### Install Riscv GNU Toolchain

```
  git clone https://github.com/riscv/riscv-gnu-toolchain
  sudo apt-get install autoconf automake autotools-dev curl python3 python3-pip libmpc-dev libmpfr-dev libgmp-dev gawk build-essential bison flex texinfo gperf libtool   
  patchutils bc zlib1g-dev libexpat-dev ninja-build git cmake libglib2.0-dev
  ./configure --prefix=/opt/riscv
  make
  ```

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






