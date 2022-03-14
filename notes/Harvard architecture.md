### Harvard architecture
The Harvard architecture is characteristed by a seperation of the primary memory [address space](<RAM#Address space>) into two sections: one containing active programs, and one containg the data they use. Additionally, this seperation is physical: there is one data bus *per section*, each used to transmit requested data to the CPU (potentially simultaneously). The Harvard architecture is often associated with [RISC](<RISC and CISC>) processors, as the lack of a delay in data-access when accessing instructions makes using more, but simpler, instructions viable.   ^145246
***
For a detailed evaluation of the consequences of the Harvard architecture, and a comparison to alternatives, see the [[CPU architecture]] page.

#Component1-Section1