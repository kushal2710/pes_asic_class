# PES_ASIC_CLASS

## DAY 1 - INTRODUCTION TO RISC-V ISA AND GNU COMPILER TOOLCHAIN

### LAB1 - c program to compute sum 1 to N
![image](https://github.com/kushal2710/pes_asic_class/assets/115935208/5773fe42-28bb-4e42-9b0f-832bc90e8abc)
![image](https://github.com/kushal2710/pes_asic_class/assets/115935208/21260005-cdf4-4acd-84bc-00ee17a52a17)

### LAB2 - RISC-V GCC COMPILE AND DISASSEMBLE

#riscv64-unknown-elf-gcc -O1  -mabi=lp64  march=rv64i  -o sum1ton.o  sum1ton.c 

the above command is used in Ubuntu to compile a C source code file (sum1ton.c) into an object file (sum1ton.o) using the RISC-V 64-bit architecture toolchain (riscv64-unknown-elf-gcc)

O1 - optimisation flag GCC will try to optimize the code for size and execution speed.

-mabi=lp64: This flag specifies the ABI (Application Binary Interface) to use. ABI defines how functions, data, and system calls are represented and accessed in machine code. lp64 stands for "Long, Pointer, 64-bit," which means that integers and longs are 64 bits, and pointers are also 64 bits.

-march=rv64i: This flag specifies the target RISC-V architecture. 

So, when you run this command in Ubuntu, it will take the sum1ton.c source code, compile it with the specified options and toolchain, and produce an object file named sum1ton.o that can later be linked to create an executable program for the RISC-V 64-bit architecture.

When you run ls -ltr in a terminal in Ubuntu, you'll see a list of files and directories in the current directory

![image](https://github.com/kushal2710/pes_asic_class/assets/115935208/a34f4af7-5378-4cfe-a9eb-936eca0a661e)

![image](https://github.com/kushal2710/pes_asic_class/assets/115935208/6e2f4e6d-5334-48f1-ab25-8a4b153d4dd7)

#### Using Ofast - optimisation flag 

![image](https://github.com/kushal2710/pes_asic_class/assets/115935208/c2730444-1907-4b2a-914c-e7a278cd71cc)

You can use riscv64-unknown-elf-objdump to disassemble machine code into human-readable assembly language

![image](https://github.com/kushal2710/pes_asic_class/assets/115935208/50cd1940-0c7e-445f-a673-095294e7f036)

## LAB3 - spike simulation and debug

![image](https://github.com/kushal2710/pes_asic_class/assets/115935208/95881567-bef9-4e00-a1df-ca9942e0251d)

## LAB4 - signed and unsigned integers

![image](https://github.com/kushal2710/pes_asic_class/assets/115935208/ea752c52-caef-4b37-a03c-2759f910fc0f)

# DAY2 - INTRODUCTION TO ABI AND BASIC VERIFICATION FLOW

## LAB1 - simulating new c program with function call

![image](https://github.com/kushal2710/pes_asic_class/assets/115935208/d7410f44-5ecd-4f5b-93d8-68f9740c8e15)

![image](https://github.com/kushal2710/pes_asic_class/assets/115935208/34badac8-eaba-4d25-b870-5526175dc31e)

![Screenshot from 2023-08-22 09-06-19](https://github.com/kushal2710/pes_asic_class/assets/115935208/a217b637-e54d-4470-a6d7-d0002ba9e8e6)


![Screenshot from 2023-08-19 18-09-41](https://github.com/kushal2710/pes_asic_class/assets/115935208/b57724d5-8d0f-43ab-a1b4-22e5680cca24)

TO RUN C PROGRAM ON RISC-V CPU

![image](https://github.com/kushal2710/pes_asic_class/assets/115935208/3897a88c-52a2-4247-8a53-6d76b8360714)

![image](https://github.com/kushal2710/pes_asic_class/assets/115935208/578cd5ed-7ffe-48b4-a320-4e7d82f89970)

![image](https://github.com/kushal2710/pes_asic_class/assets/115935208/fa303720-2a16-438a-991b-2e5a0e42c0c1)

# INTRODUCTION TO VERILOG RTL DESIGN AND SYNTHESIS

## DAY1 - Introduction to open-source simulator iverilog

 RTL design is checked for adherence to the spec by simulating the design

• Simulator is the tool used for simulating the design, iverilog is the tool used 

  Design is the actual Verilog code or set of Verilog codes which has the intended functionality to meet with the required specifications

  TestBench is the setup to apply stimulus (test_vectors) to the design to check its functionality

  ![Screenshot from 2023-08-27 23-27-04](https://github.com/kushal2710/pes_asic_class/assets/115935208/691762b3-69e4-44e3-9ae3-78b6d759ec17)

  ![Screenshot from 2023-08-27 23-28-20](https://github.com/kushal2710/pes_asic_class/assets/115935208/f4d958c6-71ce-49de-9744-e1091210bf5f)

 ## LABS using iverilog and gtkwave 

 After gitcloning to https://github.com/kunalg123/sky130RTLDesignAndSynthesisworkshop.git

 ![Screenshot from 2023-08-27 18-14-03](https://github.com/kushal2710/pes_asic_class/assets/115935208/82ad467a-c40d-4643-819e-e55a68f5cc0c)

 ![Screenshot from 2023-08-27 23-42-26](https://github.com/kushal2710/pes_asic_class/assets/115935208/9785d898-103d-4801-a970-7a29df3ac2ef)

 After simulating the multiplexer using iverilog 

 ![Screenshot from 2023-08-27 18-17-08](https://github.com/kushal2710/pes_asic_class/assets/115935208/af25ea3b-f138-46d6-9985-0ac92bfe8cfd)

 ![Screenshot from 2023-08-27 18-23-56](https://github.com/kushal2710/pes_asic_class/assets/115935208/440527bc-7b46-4905-8200-8cff5e599246)

 we can see that multiplexer is selecting the output based on the select signal 

 ![Screenshot from 2023-08-27 18-17-08](https://github.com/kushal2710/pes_asic_class/assets/115935208/4fe340ca-6783-402e-b57e-bdc028e60eb2)

 ![Screenshot from 2023-08-27 18-41-54](https://github.com/kushal2710/pes_asic_class/assets/115935208/1f212761-117a-425d-8ed8-34270b8edfd3)

 ![Screenshot from 2023-08-27 23-50-12](https://github.com/kushal2710/pes_asic_class/assets/115935208/21856417-c99e-4ac5-9500-d657f936b785)

 ![Screenshot from 2023-08-27 23-51-20](https://github.com/kushal2710/pes_asic_class/assets/115935208/25799ab3-3571-4ecc-8ae7-82c2117e0490)

 ![Screenshot from 2023-08-27 23-52-47](https://github.com/kushal2710/pes_asic_class/assets/115935208/98dd8dd3-0c1d-4ad9-b63a-09d4f8d46fe5)

 Invoking the yosys

 ![Screenshot from 2023-08-27 23-58-23](https://github.com/kushal2710/pes_asic_class/assets/115935208/2088e3ec-d445-49d1-9e0f-a5a61f07a14d)

 ![Screenshot from 2023-08-28 12-11-46](https://github.com/kushal2710/pes_asic_class/assets/115935208/fdf6c8f7-2660-487d-909c-f926c05b4790)

 ![Screenshot from 2023-08-28 12-12-12](https://github.com/kushal2710/pes_asic_class/assets/115935208/32f03763-ab85-4538-b101-fdafc3728f52)

 ![Screenshot from 2023-08-28 22-48-08](https://github.com/kushal2710/pes_asic_class/assets/115935208/764c4055-5319-46ad-a160-c91a48bf19ec)

 ![Screenshot from 2023-08-28 22-45-03](https://github.com/kushal2710/pes_asic_class/assets/115935208/55ba2c03-fd21-4c09-928c-0441e066dd07)
 
 ![Screenshot from 2023-08-28 22-28-56](https://github.com/kushal2710/pes_asic_class/assets/115935208/a82f1432-cacf-487b-aafa-ab008652f075)

 ![Screenshot from 2023-08-28 23-13-18](https://github.com/kushal2710/pes_asic_class/assets/115935208/93886b7e-6e08-4bd1-a144-313d934d3606)

 # DAY2 - TIMING LIBS,HIERARCHIAL V/S FLAT SYNTHESIS,EFFICIENT FLOP CODING STYLES

 ## Introduction to timing.libs
 
 ![Screenshot from 2023-08-28 23-45-49](https://github.com/kushal2710/pes_asic_class/assets/115935208/e4adcf16-06bd-4bd4-b9bd-6f060151bbb1)

 ![Screenshot from 2023-08-28 23-31-32](https://github.com/kushal2710/pes_asic_class/assets/115935208/13b7545f-a296-4f8d-b229-632b09d6e29c)

 ![Screenshot from 2023-08-28 23-44-03](https://github.com/kushal2710/pes_asic_class/assets/115935208/8c253dbc-ea7e-4613-8b0d-2c777c20bcb0)

 ## Hierarchial v/s flat synthesis

 ![Screenshot from 2023-08-29 00-00-19](https://github.com/kushal2710/pes_asic_class/assets/115935208/9d969171-c754-488b-a964-1e05df741e5e)

 ![Screenshot from 2023-08-29 00-01-28](https://github.com/kushal2710/pes_asic_class/assets/115935208/2c3e729c-770c-4279-9b4d-0f88bf0f9e0f)

 ![Screenshot from 2023-08-29 00-04-00](https://github.com/kushal2710/pes_asic_class/assets/115935208/2d40c6f7-8ac3-4c19-a740-de8e1d67ef69)

 ![Screenshot from 2023-08-29 00-04-47](https://github.com/kushal2710/pes_asic_class/assets/115935208/a32f3aa9-9a06-4fd8-a10f-ddb66863d4ad)

 ![Screenshot from 2023-08-29 00-09-44](https://github.com/kushal2710/pes_asic_class/assets/115935208/4c78af00-0afc-4690-8b06-9e965012cdf2)

 ![Screenshot from 2023-08-29 00-10-48](https://github.com/kushal2710/pes_asic_class/assets/115935208/7cf7a180-a7ee-4d28-9167-b3f9644bcd5d)

 ![Screenshot from 2023-08-29 00-16-13](https://github.com/kushal2710/pes_asic_class/assets/115935208/f256674c-a41e-4407-971d-83b7750cf223)

 ![Screenshot from 2023-08-29 00-17-14](https://github.com/kushal2710/pes_asic_class/assets/115935208/bca052c0-9b91-4038-80b7-2c9240ae25ed)

 ![Screenshot from 2023-08-29 00-22-59](https://github.com/kushal2710/pes_asic_class/assets/115935208/ca90ac8b-b00d-4623-b8ce-0bd661d37f3b)

 ![Screenshot from 2023-08-29 00-23-26](https://github.com/kushal2710/pes_asic_class/assets/115935208/cbbd41e2-a439-458e-b3e3-baec121cd299)

 ![Screenshot from 2023-08-29 00-26-37](https://github.com/kushal2710/pes_asic_class/assets/115935208/329db042-bc9d-44dd-bee9-4ab15ca132c1)

 ![Screenshot from 2023-08-29 00-26-59](https://github.com/kushal2710/pes_asic_class/assets/115935208/d6083a0a-3f49-4039-af16-1ba5876cccfa)

 ![Screenshot from 2023-08-29 00-28-16](https://github.com/kushal2710/pes_asic_class/assets/115935208/d3304955-c020-4af7-af3a-c9be8b4e7127)

 ![Screenshot from 2023-08-29 00-28-42](https://github.com/kushal2710/pes_asic_class/assets/115935208/46aed982-26ec-45b2-9730-81c82881301c)

 ## Various flop coding styles and optimization

 ![Screenshot from 2023-08-29 15-33-56](https://github.com/kushal2710/pes_asic_class/assets/115935208/3e2c4c5a-7199-4493-9a6c-94a38bbc530e)

 ![Screenshot from 2023-08-29 15-38-18](https://github.com/kushal2710/pes_asic_class/assets/115935208/7f5e7b78-f68e-4a45-8ba6-9484a428d42c)

 ![Screenshot from 2023-08-29 15-28-59](https://github.com/kushal2710/pes_asic_class/assets/115935208/176939bb-4df2-46ff-bc40-7d08f1b8427e)

 ![Screenshot from 2023-08-29 15-32-32](https://github.com/kushal2710/pes_asic_class/assets/115935208/b14a61e0-75c9-418f-99c7-e7af8f9b7228)

 ![Screenshot from 2023-08-29 15-49-36](https://github.com/kushal2710/pes_asic_class/assets/115935208/3b948a4c-4f94-4bd8-aaf6-b183bf6d6854)

 ![Screenshot from 2023-08-29 15-54-41](https://github.com/kushal2710/pes_asic_class/assets/115935208/96815590-3893-4c5e-8241-5505fcbab4b7)

 ![Screenshot from 2023-08-29 15-54-51](https://github.com/kushal2710/pes_asic_class/assets/115935208/807b4bc6-c3bb-413f-a1b6-ee300b39161a)

 ![Screenshot from 2023-08-29 17-04-04](https://github.com/kushal2710/pes_asic_class/assets/115935208/ecf723e7-d242-4c58-9cdc-50e8c1fbdb16)

 ![Screenshot from 2023-08-29 17-04-10](https://github.com/kushal2710/pes_asic_class/assets/115935208/6acbf113-1bab-473c-a41d-dbbad7ee2986)

 ![Screenshot from 2023-08-29 17-11-47](https://github.com/kushal2710/pes_asic_class/assets/115935208/710d049d-f5c0-4a5d-b021-d622e7b6d993)

 ![Screenshot from 2023-08-29 17-12-12](https://github.com/kushal2710/pes_asic_class/assets/115935208/8fc63076-82d4-4245-8c1e-15d37b7c8faf)

 ![Screenshot from 2023-08-29 17-19-05](https://github.com/kushal2710/pes_asic_class/assets/115935208/25909262-cc65-46ab-aabc-b3b504baf771)

 ![Screenshot from 2023-08-29 17-22-29](https://github.com/kushal2710/pes_asic_class/assets/115935208/248d1e34-6a0b-4b62-bb75-cbe1a7760abc)

 ## Interesting optimisations

 ![Screenshot from 2023-08-29 17-38-46](https://github.com/kushal2710/pes_asic_class/assets/115935208/f7a07484-7355-4875-9222-8f57f2340f93)

 ![Screenshot from 2023-08-29 17-33-58](https://github.com/kushal2710/pes_asic_class/assets/115935208/8f1e7e4f-2269-4d5f-a63f-e141550ad987)

 ![Screenshot from 2023-08-29 17-39-10](https://github.com/kushal2710/pes_asic_class/assets/115935208/9e51bf67-a5ac-4808-82f9-8191a148aef3)

 ![Screenshot from 2023-08-29 17-41-14](https://github.com/kushal2710/pes_asic_class/assets/115935208/c5f69dc3-4722-46a1-999b-9b412f8f28f0)

 ![Screenshot from 2023-08-29 17-44-06](https://github.com/kushal2710/pes_asic_class/assets/115935208/a4e894b3-4971-40a8-b91a-f01793b15f4a)

 ![Screenshot from 2023-08-29 17-53-38](https://github.com/kushal2710/pes_asic_class/assets/115935208/5f45861f-5c64-48ff-aa74-fad749148571)

 ![Screenshot from 2023-08-29 17-58-36](https://github.com/kushal2710/pes_asic_class/assets/115935208/c90b985d-1bf5-4833-8350-3aa17a8ad7c5)

 # DAY3 - combinational and sequential optimisations

 ## Combinational optimisations

 ![Screenshot from 2023-08-29 17-58-36](https://github.com/kushal2710/pes_asic_class/assets/115935208/7ad20ddb-ee42-435f-8463-ebd0b7c57b17)

 ![Screenshot from 2023-08-29 18-18-27](https://github.com/kushal2710/pes_asic_class/assets/115935208/0d0fe3f0-d299-479a-a871-25bddb7786a0)

 ![Screenshot from 2023-08-29 18-19-23](https://github.com/kushal2710/pes_asic_class/assets/115935208/402d2175-cb11-471c-acf1-9dc279268902)

 ![Screenshot from 2023-08-29 18-20-20](https://github.com/kushal2710/pes_asic_class/assets/115935208/0a69e7cb-23b1-414d-bdfd-0656a0a8aa2a)

 ![Screenshot from 2023-08-29 18-23-11](https://github.com/kushal2710/pes_asic_class/assets/115935208/1ac35ae7-2256-4db2-93f5-71c006336e3c)

 ![Screenshot from 2023-08-29 18-26-29](https://github.com/kushal2710/pes_asic_class/assets/115935208/7316dc1e-f2ec-46f4-a738-5ac9247e7fac)

 ## sequential logic optimisations

 ![Screenshot from 2023-08-29 18-36-19](https://github.com/kushal2710/pes_asic_class/assets/115935208/9a2286bc-8ed4-417f-8c39-5cafcf475735)

 ![Screenshot from 2023-08-29 18-38-45](https://github.com/kushal2710/pes_asic_class/assets/115935208/0de76eb1-04bf-4b42-92e8-bda4ec265ba9)

 ![Screenshot from 2023-08-29 18-42-14](https://github.com/kushal2710/pes_asic_class/assets/115935208/36ba5cf5-60d8-4532-8b1d-6eb02ed83164)

 ![Screenshot from 2023-08-29 18-43-47](https://github.com/kushal2710/pes_asic_class/assets/115935208/f4ab39da-5330-4a21-91c1-e017a86ae0dd)

 ![Screenshot from 2023-08-29 18-48-38](https://github.com/kushal2710/pes_asic_class/assets/115935208/e2b53155-37c7-4930-88be-886091dd56af)

 ![Screenshot from 2023-08-29 18-53-57](https://github.com/kushal2710/pes_asic_class/assets/115935208/e0ebaf32-86a3-401d-af22-5909818208a7)

 ![Screenshot from 2023-08-29 18-57-29](https://github.com/kushal2710/pes_asic_class/assets/115935208/6d7b607c-699b-4ea4-b001-0fe09e4295a2)

 ## sequential optimisation for unused outputs

 ![Screenshot from 2023-08-29 19-10-02](https://github.com/kushal2710/pes_asic_class/assets/115935208/321f7781-341a-45ce-9d3d-e6c72b2b0c6b)

 ![Screenshot from 2023-08-29 19-13-46](https://github.com/kushal2710/pes_asic_class/assets/115935208/53fe5a09-0494-47ff-8c6e-eb6f6a739e88)

 ![Screenshot from 2023-08-29 19-25-31](https://github.com/kushal2710/pes_asic_class/assets/115935208/630182b5-2475-45b8-8653-d1d382ee9501)


