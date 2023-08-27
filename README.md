#PES_ASIC_CLASS

DAY 1 - INTRODUCTION TO RISC-V ISA AND GNU COMPILER TOOLCHAIN

LAB1 - c program to compute sum 1 to N
![image](https://github.com/kushal2710/pes_asic_class/assets/115935208/5773fe42-28bb-4e42-9b0f-832bc90e8abc)
![image](https://github.com/kushal2710/pes_asic_class/assets/115935208/21260005-cdf4-4acd-84bc-00ee17a52a17)

LAB2 - RISC-V GCC COMPILE AND DISASSEMBLE

#riscv64-unknown-elf-gcc -O1  -mabi=lp64  march=rv64i  -o sum1ton.o  sum1ton.c 

the above command is used in Ubuntu to compile a C source code file (sum1ton.c) into an object file (sum1ton.o) using the RISC-V 64-bit architecture toolchain (riscv64-unknown-elf-gcc)

O1 - optimisation flag GCC will try to optimize the code for size and execution speed.

-mabi=lp64: This flag specifies the ABI (Application Binary Interface) to use. ABI defines how functions, data, and system calls are represented and accessed in machine code. lp64 stands for "Long, Pointer, 64-bit," which means that integers and longs are 64 bits, and pointers are also 64 bits.

-march=rv64i: This flag specifies the target RISC-V architecture. 

So, when you run this command in Ubuntu, it will take the sum1ton.c source code, compile it with the specified options and toolchain, and produce an object file named sum1ton.o that can later be linked to create an executable program for the RISC-V 64-bit architecture.

When you run ls -ltr in a terminal in Ubuntu, you'll see a list of files and directories in the current directory

![image](https://github.com/kushal2710/pes_asic_class/assets/115935208/a34f4af7-5378-4cfe-a9eb-936eca0a661e)

![image](https://github.com/kushal2710/pes_asic_class/assets/115935208/6e2f4e6d-5334-48f1-ab25-8a4b153d4dd7)

Using Ofast - optimisation flag 

![image](https://github.com/kushal2710/pes_asic_class/assets/115935208/c2730444-1907-4b2a-914c-e7a278cd71cc)

You can use riscv64-unknown-elf-objdump to disassemble machine code into human-readable assembly language

![image](https://github.com/kushal2710/pes_asic_class/assets/115935208/50cd1940-0c7e-445f-a673-095294e7f036)

LAB3 - spike simulation and debug

![image](https://github.com/kushal2710/pes_asic_class/assets/115935208/95881567-bef9-4e00-a1df-ca9942e0251d)

LAB4 - signed and unsigned integers

![image](https://github.com/kushal2710/pes_asic_class/assets/115935208/ea752c52-caef-4b37-a03c-2759f910fc0f)

DAY2 - INTRODUCTION TO ABI AND BASIC VERIFICATION FLOW

LAB1 - simulating new c program with function call

![image](https://github.com/kushal2710/pes_asic_class/assets/115935208/d7410f44-5ecd-4f5b-93d8-68f9740c8e15)

![image](https://github.com/kushal2710/pes_asic_class/assets/115935208/34badac8-eaba-4d25-b870-5526175dc31e)

![Screenshot from 2023-08-22 09-06-19](https://github.com/kushal2710/pes_asic_class/assets/115935208/a217b637-e54d-4470-a6d7-d0002ba9e8e6)


![Screenshot from 2023-08-19 18-09-41](https://github.com/kushal2710/pes_asic_class/assets/115935208/b57724d5-8d0f-43ab-a1b4-22e5680cca24)

TO RUN C PROGRAM ON RISC-V CPU

![image](https://github.com/kushal2710/pes_asic_class/assets/115935208/3897a88c-52a2-4247-8a53-6d76b8360714)

![image](https://github.com/kushal2710/pes_asic_class/assets/115935208/578cd5ed-7ffe-48b4-a320-4e7d82f89970)

![image](https://github.com/kushal2710/pes_asic_class/assets/115935208/fa303720-2a16-438a-991b-2e5a0e42c0c1)

INTRODUCTION TO VERILOG RTL DESIGN AND SYNTHESIS

DAY1 - Introduction to open-source simulator iverilog

 RTL design is checked for adherence to the spec by simulating the design

• Simulator is the tool used for simulating the design, iverilog is the tool used 

  Design is the actual Verilog code or set of Verilog codes which has the intended functionality to meet with the required specifications

  TestBench is the setup to apply stimulus (test_vectors) to the design to check its functionality

  ![Screenshot from 2023-08-27 23-27-04](https://github.com/kushal2710/pes_asic_class/assets/115935208/691762b3-69e4-44e3-9ae3-78b6d759ec17)

  ![Screenshot from 2023-08-27 23-28-20](https://github.com/kushal2710/pes_asic_class/assets/115935208/f4d958c6-71ce-49de-9744-e1091210bf5f)

 LABS using iverilog and gtkwave 

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




