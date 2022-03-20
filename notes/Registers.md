### Registers
Registers are small memory locations (typically less than 64 bits of storage), stored physically on the CPU. They have by far the fastest access times out of all possible memory addresses, as the distance current needs to travel to the main processing components is mininal. Registers can be grouped into two categories: special purpose, and general purpose.
***
#### Special purpose registers
The CPU has a small amount of registers which fufill specific purposes for performing [computational operators](Fetch,%20Decode,%20Execute%20cycle.md Decode, Execute cycle>). These are:
- Program counter (PC)<span style="color:gray">, which stores the memory address of the instruction to be processed on the next cycle.</span>
- Memory Address register (MAR)<span style="color:gray">, which stores the address from which data / a instruction will be retrived from or written to RAM.</span>
- Memory Data register (MDR)<span style="color:gray">, which stores the data / instruction retrived from or being written to RAM.</span>
- Current Instruction register (CIR)<span style="color:gray">, which stores the current instruction being executed.</span>
- Accumilators<span style="color:gray">, which hold the data being worked on and the result of arithmatic and logic operations, to be copied to RAM after the operations are finalised.</span>
- Status register<span style="color:gray">, which hold information on the last operation, e.g. if a summation's result was zero, or negative, or if a over/under-flow occoured.</span>
- Interupt register<span style="color:gray">, which hold information about whether an interupt has occoured, and details regarding it.</span>
See the [[Fetch, Decode, Execute cycle]] page for a descriptive overview of how information is moved between these to allow for the processing of instructions on data.
***
#### General purpose registers
There is a small number of general purpose registers of varying sizes. When a program is compiled to machine code, a well-designed compiler will inteligently substitute as many as possible of the rewrite/recall-to-RAM data transfers with general purpose register stores.

On the x86-64 architecture, the general purpose registers are:
- EAX, EBX, ECX, EDX (32 bits)
- AX, BX, CX, DX (16 bits)
- AH, AL, BH, BL, CH, CL, DH, DL (8 bits)

#Component1-Section1