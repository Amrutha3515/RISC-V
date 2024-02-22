# Vsdquadron Mini
<details>
<summary>Task-1</summary>

+ Install Oracle Virtual Machine
+ install Ubuntu 20.04 on VM

<details>
    <summary> Install Riscv GNU Toolchain</summary>

  ```bash 
    git clone https://github.com/riscv/riscv-gnu-toolchain
    sudo apt-get install autoconf automake autotools-dev curl python3 python3-pip libmpc-dev libmpfr-dev libgmp-dev gawk build-essential bison flex texinfo gperf libtool   
    patchutils bc zlib1g-dev libexpat-dev ninja-build git cmake libglib2.0-dev
    ./configure --prefix=/opt/riscv
    make
  ```
![image](https://github.com/Amrutha3515/RISC-V/assets/150571663/9a6bbd49-9c43-4ec2-8590-fdd2ba1445b6)
</details>

<details>
 <summary>Install Yosys</summary>
	
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
</details>
<details>
<summary>Install Iverilog</summary>
  ```
  sudo apt-get install iverilog
  ```
  ![image](https://github.com/Amrutha3515/RISC-V/assets/150571663/1e635984-51f3-4533-b73b-646754abd8bd)
</details>
<details>
<summary> Install gtkwave</summary>
```
sudo apt-get install gtkwave
```
![image](https://github.com/Amrutha3515/RISC-V/assets/150571663/9122d695-2e38-40f3-8949-601ebab8d46b)
</details>
</details>
<details>
<summary>Task-2</summary> 
	
+ Identify instruction type and exact 32-bit instruction code in the instruction type format.
  
  RV32I can be divided into six basic instruction formats. R-type instructions for register-register operations, an I-type instructions for immediate and load operations, and S-type instructions for store operations. B-type instructions for conditional branch operations. U-type instructions for long immediate and J-type instructions for unconditional jumps.

  ![WhatsApp Image 2024-02-22 at 17 29 06_b1e00065](https://github.com/Amrutha3515/RISC-V/assets/150571663/e06834ef-90e6-4b81-8ce4-9c720aff2562)
  
 +  add r6, r2, r1 	= R type instruction
+ sub r7, r1, r2	= R type instruction
+ and r8, r1, r3	= R type instruction
 + or r9, r2, r5	= R type instruction
+ xor r10, r1, r4	= R type instruction
+ slt r11, r2, r4	= R type instruction
+ addi r12, r4, 5	= I type instruction
+ sw r3, r1, 2		= S type instruction
+ lw r13, r1, 2		= I type instruction
+ beq r0, r0, 15	= B type instruction
+ bne r0, r1, 20	= B type instruction
 ``` 
add r6, r2, r1
0000000	00001	00010	000	00110	0110011

sub r7, r1, r2

0100000	0010	00001	000	00111	0110011

and r8, r1, r3
0000000	0011	00001	111	01000	0110011

or r9, r2, r5
0000000	0101	00010	110	01001	0110011

xor r10, r1, r4

0000000	0100	00001	100	01010	0110011

slt r11, r2, r4

0000000	0100	00010	010	01011	0110011

addi r12, r4, 5

00000000101	00100	000	01100	0010011

sw r3, r1, 2 

0000000	0001	00011	010	01110	1100011
```
</details>










