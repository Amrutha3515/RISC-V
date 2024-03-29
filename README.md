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

```  sudo apt-get install iverilog ```
  
	
![image](https://github.com/Amrutha3515/RISC-V/assets/150571663/2615477c-d6c3-4992-8daf-d5798a595100)
</details>
<details>
<summary> Install gtkwave</summary>

``` sudo apt-get install gtkwave ```

![image](https://github.com/Amrutha3515/RISC-V/assets/150571663/2615477c-d6c3-4992-8daf-d5798a595100)
	

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

<details>
	<summary>Task-3</summary>
	
 + compiled the c code of sumof 1 to 5 numbers in gcc 

 ![image](https://github.com/Amrutha3515/RISC-V/assets/150571663/f60d4a74-826c-41b4-8ed7-0574124c64ba)

+ After compiling, we can see disassembply code generated using RISC-V Objdmp
```
 riscv64-unknown-elf-objdump -d sum1ton.o | less
 ```
 ![image](https://github.com/Amrutha3515/RISC-V/assets/150571663/8b42a705-7b4a-47af-8d79-424bec8cf5e1)


</details>
<details>
<summary>Task-4</summary>
	
+ The conventional GCC X86 compiler and the riscv compiler should be simulated for the C code (SPIKE Simulation).
GCC (F1) SHOULD HAVE AN EQUAL OUTPUT TO THE RISCV GCC (F2) AS REQUIRED.



+ To compile the code: ``` riscv64-unknown-elf-gcc -o sum1ton sum1ton.c ``` To Get the output use ``` ./a.out ``` : Here the output finds to be -Sum of numbers from 1 to 500 is 125250



  </details>

<details>
	<summary>Task-5</summary>




### The output waveform showing the instructions performed in a 5-stage pipelined architecture.
<details>
<summary>add r6,r2,r1</summary>

![image](https://github.com/Amrutha3515/RISC-V/assets/150571663/d991a6ba-b4ee-4193-a8d5-8d4a3aac514f)


</details>

<details>
<summary>sub r7,r1,r2</summary>
	
![image](https://github.com/Amrutha3515/RISC-V/assets/150571663/34e4bf38-022c-48f7-8e96-4b43fc5d3749)

</details>
<details>
<summary>and r8,r1,r3</summary>
	
![image](https://github.com/Amrutha3515/RISC-V/assets/150571663/5a030fa4-f166-494d-a2a3-00ff455d5a88)

</details>

<details>
	<summary>or r9,r2,r5</summary>

 ![image](https://github.com/Amrutha3515/RISC-V/assets/150571663/d45c6b14-b979-4253-ae38-74d69d8aa0cf)


</details>

<details>
	<summary>xor r10,r1,r4</summary>

 ![image](https://github.com/Amrutha3515/RISC-V/assets/150571663/ead5a7b5-6ea8-42b7-a87e-5c41fb13943b)


</details>
<details>
	<summary>slt r11,r2,r4</summary>

 ![image](https://github.com/Amrutha3515/RISC-V/assets/150571663/7f7493a0-b6c3-4352-ba24-0134badf026e)


</details>
<details>
	<summary>addi r12,r4,5</summary>

 ![image](https://github.com/Amrutha3515/RISC-V/assets/150571663/0ade44dd-103c-481c-aecd-2b940d990c80)


</details>
<details>
	<summary>sw r3,r1,2</summary>

 ![image](https://github.com/Amrutha3515/RISC-V/assets/150571663/ffd2bad8-0407-4084-bba7-e2c6ca5c6a3b)


</details>
<details>
	<summary>lw r13,r1,2</summary>

 ![image](https://github.com/Amrutha3515/RISC-V/assets/150571663/badcc136-aade-4333-bbbb-ce5203adf65e)


</details>
<details>
	<summary>beq r0,r0,15</summary>
	
![image](https://github.com/Amrutha3515/RISC-V/assets/150571663/5879dacb-c38c-4b40-bca9-a70fd02859ea)


</details>
<details>
	<summary>add r14,r2,r2</summary>

 ![image](https://github.com/Amrutha3515/RISC-V/assets/150571663/998e24a9-8240-4f1e-a699-db63224c8480)


</details>

</details>










