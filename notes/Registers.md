### Registers
Registers are small (- ) memory locations stored physically on the CPU. They have by far the fastest access times out of all possible memory addresses, as the distance current needs to travel to the main processing components is mininal. Registers can be grouped into two categories: special purpose, and general purpose.
***
#### Special purpose registers
The CPU has a small amount of registers which fufill specific purposes for performing [computational operators](<Fetch, Decode, Execute cycle>). These are:
- Program counter (PC)<span style="color:gray">, which stores the memory address of the instruction to be processed on the next cycle.</span>
- Memory Address register (MAR)<span style="color:gray">, which stores the address of the data / instruction currently being retrived from memory.</span>
- Memory Data register (MDR)<span style="color:gray">, which stores the data / instruction retrived from .</span>
- CIR
See the [[Fetch, Decode, Execute cycle]] page for a descriptive overview of how information is moved between these to allow for the processing of instructions on data.
***
#### General purpose registers
There is a small number of general purpose registers of varying sizes. When a program is compiled to machine code, a well-designed compiler will inteligently substitute as many as possible of the rewrite/recall-to-RAM data transfers with general purpose register stores.

On the x86-64 architecture, the general purpose registers are:
- RAX, ( bytes)

#Component1-Section1