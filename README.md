# <center> RISC-V Arch Test </center>

## *<center> Implementation of Task 6 </center>*

#### Question Statement:

###### *Write a test to change behaviour of a locked pmp region using smepmp extension in spike (Smepmp task)*

1. Pre-requisites:
	- Read RISCV privileged architecture spec for PMP.
	- Read about Smepmp extension.

2. Write an assembly test:
	- Start your test in M mode. Configure a locked pmp region for read, write and execute permissions.
	- What two things happen when you configure a locked pmp region?
	-  Now, try to change permissions of that region to only read from read,write and execute. How it can be achieved using smepmp extension.

#### Build & Run:

###### *Compile Assembly File to Elf:*

```shell
riscv64-unknown-elf-gcc -march=rv32imac_smepmp -mabi=ilp32 -nostdlib -T link.ld task6.S -o test.elf
```
###### *Create a Disassembly:*

```shell
riscv64-unknown-elf-objdump -D test.elf > test.disass
```

###### *Simulate on Spike & Generate Logfile:*

```shell
spike --isa=rv32imac_smepmp -l --log-commits test.elf 1> spike.out 2> spike.log
```

###### *Simulate on Sail & Generate Logfile:*

```shell
Sail DOES NOT Support SMEPMP...
```

#### Documentation:

###### *Source Code Available at:*
-	<span style = 
			"color: rgb(255, 64, 92);
			background: rgb(228, 228, 228);
			padding: 4px 12px;
			border-radius: 10px"
		> /Code/task6.S
	</span>

###### *Log Files Available at:*
-	<span style = 
			"color: rgb(255, 64, 92);
			background: rgb(228, 228, 228);
			padding: 4px 12px;
			border-radius: 10px"
		> /Code/spike.log
	</span>

###### *Report Available at:*
-	<span style = 
			"color: rgb(255, 64, 92);
			background: rgb(228, 228, 228);
			padding: 4px 12px;
			border-radius: 10px"
		> /Report/RISC-V_Arch_Test_Task_6_Report.docx
	</span>

###### *Output Screenshots Available at:*
-	<span style = 
			"color: rgb(255, 64, 92);
			background: rgb(228, 228, 228);
			padding: 4px 12px;
			border-radius: 10px"
		> /Screenshots
	</span>