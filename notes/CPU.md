### The CPU (Central Processing Unit)
The CPU is the main processor of the computer system. It is the component which is generally responsible for [executing instructions on data](<Fetch, Decode, Execute cycle>) - a process who's exact order and structure is determined by the code of the program which is being ran. As a CPU is a *digital* electronic device, both the instructions and data are internally represented as [binary](Binary) numbers. When formatted in [binary](Binary), the program is said to be [machine code](<Machine code>), and the instructions and data are [opcodes and operands](<Opcodes and Operands>) respectively.

#### Components of a CPU
**The Arithmetic and Logic Unit (ALU)** processes arithmetical and logical computations, such as *ADD, SUB, AND, OR, XOR*. It uses the [accumulator register](Registers#^f2645b) to store intermediate results when calculating operations which take multiple clock cycles, leaving the final result within to be written into RAM for a active program to access.
**The Control Unit (CU)** directs the operations of the rest of the CPU. It is responsible for the following tasks:
- Dictating the transfer of data to addresses between the CPU and other devices, along  

The CPU is connect to 

Bus Name | Contents | Direction
--|--|--
Address Bus | Transmits addresses from the processor to memory and the input-output device controller|Unidirectional: Processor -> Memory and IO
Data Bus | Transmits data between the processor, memory, and input-output devices | Bidirectional: Processor <-> Memory and IO
Control Bus | Transmits 'control' signals, sent between the processor, peripheral devices, motherboard's system clock and (occasionally from, often to) memory.| Bidirectional: Processor <-> Peripherals <(rarely)-> Memory <- Motherboard hardware clock 

***
#### CPU Structure, Types and Architecture
The 'structure' (also referred to as <u>'architecture'</u>) of the CPU describes the properties and design of the components which make up the CPU, and how they interact with each other & the other parts of the computer system. The CPU has many general purpose [registers](Registers.md) and a set number of [special purpose registers](Registers.md#Sec2), which are primarily used to fulfil specific roles during the [fetch, decode, execute cycle](<Fetch, Decode, Execute cycle>). 
The 'architecture' of the CPU can **also** be used to describes the categorical specialisation of how memory is shared between programs and data. The most common architectures are: 
- The vonn Neumann architecture 
- The Harvard architecture
- The Contemporary processor architecture <span style="color:gray">(a combination of both the von Neumann and Harvard architectures; most commonly used in practice)</span>

##### Vonn Neumann architecture
The vonn Neumann architecture is characterised by **one** [address space](<RAM#Address space>) being used to store both active programs and their allocated data in primary memory. Additionally, this address space is also physically connected by **one** data bus (i.e a single hardware connection between the CPU and RAM). Vonn Neumann architectures are often associated with [CISC](<RISC and CISC>) processors, as the disadvantage of non-parallel instruction and data access can be minimised by allowing for more complex and expressive instructions.

##### Harvard architecture
The Harvard architecture is characterised by a separation of the primary memory [address space](<RAM#Address space>) into two sections: one containing active programs, and one containing the data they use. Additionally, this separation is physical: there is one data bus *per section*, each used to transmit requested data to the CPU (potentially simultaneously). The Harvard architecture is often associated with [RISC](<RISC and CISC>) processors, as the lack of a delay in data-access when accessing instructions makes using more, but simpler, instructions viable. 

##### Comparison

Category|vonn Neumann|Harvard
--|--|--
Speed|The vonn Neumann architecture is generally less performant, as the singular data bus forces instructions and data to be accessed sequentially, whereas they'll actually be required together ([[SISD]]).|0
Flexibility|The combination of these two categories of memory allows for a greater degree of flexability in what techniques a program can use - data can be carefully and cleverly processed as instructions (and vice versa), allowing for very dynamic computation. |0


#Component1-Section1