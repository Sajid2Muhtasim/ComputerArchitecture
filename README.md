# ComputerArchitecture
Sajid Muhtasim 
100743250

What I learned from classes, class activities and assignments. 


May 5, 2025
Computer Organization – All physical aspects; How does a computer work?
Computer Architecture – Logical aspects of system implementation; How to design a computer?
Principle of Equivalence of Hardware and Software – Assuming speed isn’t a concern. any task that can be done by a software can also be done using a hardware, and any operation performed directly by the hardware can be done using a software.
Computer system at basic has 3 pieces – Processor, memory, mechanism
Different parts of a pc setup – RAM, Storage, Monitor display (LCD), PCIe, Cache, etc.
 
Studying computer architecture will help to better design programs and software as well as drivers and better optimize them. It will also help us to benchmark computer performances and understand the value/cost and trade offs of computers.


May 7, 2025

Error: A mistake; information not the way it is supposed to be.
 
Error detection methods + algorithm:
Parity bit – Check to see if the data set has even or odd numbers and assign the parity bit based on that. Example: If the signal has an even number of 1s, use 0 for parity bit, if signal has odd number of 1s, use 1 for parity bit.
From video – 16 bit data
4 bits + 1 reserved for parity.
The 1 extra bit for extended, to know if the dataset has more than one error (position 0).
4 sets of questions to assign the parity bits in locations 2,3 (for column checks) and 4,8 (for row checks)
 
Venn diagram tests, three circles; for even parity, the number of 1s should be even. Check each circle, the two circles with error shows where the error is.
 
Encoding – two types
Fixed length – Example ASCII, could take more space
Variable length – Assign higher frequency letters with smaller bits and less frequency letters with higher bits. Example, assign 0 to a which has a frequency of 60 and 0110 to b which has a frequency of 2.
 
Using huffman's algorithm to encode variable length. Organize letters in increasing frequency order, add the two lowest and arrange new order, repeat till left with 1 value. Draw the tree and assign 0 and 1 to branches (branches that end are 0 and branches that keep going are 1)
 
 
Different kinds of gates: AND, NOT, NOR, NAND, NOR, XOR
Input number can vary
Number of possibilities = 2inputs
Example, for a system with 3 inputs, the number of possibilities is 23 = 8
 
Truth table shows all the possible inputs and the corresponding outputs
 
A function with 4 inputs has 16 possibilities.
 
To get a function out of a truth table, the lines with the output being 1 are taken. Example:
X = 0. Y=0, Z=1          Output =1
X=1, Y=1, Z=1             Output = 1
Function would be F(x,y,z) = (xy)z + xyz
Note: xy is bar (NOT) but I don’t know how to do that on word doc








12 May, 2025

Addition of binary numbers.
Problem: Carry over at the end (overflow)
Use half adder; Two outputs, Sum and carry over. If there is a carry over, the signal is 1.
Simplified, half adder is a combination of sum of two gates (XOR) and carry (AND)
Half adder circuit in notation will have two inputs A,B and two outputs S,C
 
Full adder is a combination of two half adders
 
Signed numbers:
0 is used to show a positive number, 1 is used to show a negative number (left most bit)
Adding a positive and negative number using basic binary addition causes errors, so 2 complements are necessary. 1st complement is flipping all the bits (turn 0 to 1 and 1 to 0), 2nd complement is adding 1.
When subtracting, treat A-B as A+(-B) and add.
 
Shifts:
Logical shift – Left: Shift all bits to the left by 1 and place a 0 at the end (right side)
                      Right: Shift all bits to the right by 1 and place a 0 at the start (left side)
 
Arithmetic shift – Left: Same as logical shift left
                           Right: Shift all bits right by 1 and duplicate the leftmost bit
Arithmetic shift left is used for multiplying in powers of 2
Example, shifting left by n is multiplying by 2n
 
Arithmetic shift right is used for dividing in powers of 2
Example, shifting right by n is dividing by 2n
 
 
------------------------------------x------------------------------------x---------------------------------x------
 
 
Sisck risk architecture (?)
Patent: A legal right granted by the government to an inventor, giving them the exclusive right to make, use, sell, and license their invention for a certain period of time. It prevents others from using the same invention without permission
Two scientists working simultaneously in different parts of the world
Konrad Zuse from Germany and John Atanasoff from United States
Ultimately, John Atanasoff was awarded the patent for the electronic computer (U.S. Patent 3,558,068) in 1973.
First computer architecture
 
Physics behind computer
Vacuum tubes -> Transistors + Semiconductors -> Integrated circuits -> Binary logic + Boolean algebra
 
--------------------------------------x---------------------------------------x--------------------x--------------

 
Null rule:
 A + 1 = 1
A * 0 = 0
 
Complement
A + A’ = 1
A . A’ = 0


21 May, 2025


Digital logic can be described in three ways:

Truth tables (showing all input/output possibilities)
Boolean algebraic expressions (using math-like formulas with True/False)
Digital circuit diagrams (pictures of connected logic gates)

A truth table clearly lists every possible input combination and what the output will be for each. I can create one for any function where the output is always the same for a given input.

I learned Boolean algebra is like normal algebra but for logic (True/False, or 1/0). It has variables, operators (like AND, OR, NOT), and rules called axioms.


I learned I can write Boolean algebraic expressions to define logic functions. I also learned about properties of these expressions:

Satisfiable means it can be true for at least one input
Unsatisfiable means it's never true
Universally valid means it's always true
Two expressions are logically equivalent if they always produce the same output for the same inputs (have the same truth table)



I learned about the Sum of Products (SOP) form. This is a standard way to write a Boolean expression directly from a truth table by looking at the rows where the output is true. It's useful because it's easy to turn into a circuit diagram. SOP forms might not be the most efficient (using the fewest gates), so optimization is important.

I also learned how to translate Boolean expressions (especially SOP) into digital circuit diagrams using logic gates like AND, OR, and NOT. This shows how abstract logic becomes a physical circuit.

Boolean algebraic simplification is a key way to optimize circuits. This means using Boolean algebra rules (axioms) to make the expression smaller, which usually leads to a simpler circuit with fewer gates and transistors. The simplified circuit must still be logically equivalent to the original

Simplifying with Boolean algebra isn't always straightforward because it's not always obvious which rule to apply next. Finding the absolute simplest form can be a very hard problem (NP-complete).


I learned about Karnaugh Maps (K-Maps) as a systematic, visual method for simplifying Boolean expressions, especially for 2, 3, or 4 variables.


K-Maps involve arranging truth table values in a special grid.
The goal is to find the largest possible rectangular groups of 1s (where group sizes are powers of 2). The table order is: 00 01 11 10 for two inputs on one axis
Each group represents a simplified term in the final expression.
K-Maps for 3 and 4 variables use a specific ordering (Gray code) so adjacent cells differ by only one bit, allowing for wrap-around grouping (edges are considered adjacent).
Don't care conditions in a truth table can be used as either 0 or 1 in a K-Map to help make larger groups.






28 May, 2025

CPU visual Simulator


This website simulates how a very basic CPU would work at a fundamental level. It visualizes the execution of simple machine code instructions showing how the data would flow in the CPU.

From the simulation, I understood that at a fundamental level, there are three different buses that take the flow of data from and to the RAM and between the components of the CPU. The PC (program counter) is first taken to the address bus, and the data from this location is fetched on the control bus. This instruction is then loaded into the IR (instruction register) through the data bus. The upcode is then decoded by the Control Unit/Decoder. And then according to the instructions, the values are changed, operations are done, values are loaded, etc. in the other components of the CPU. Once the instructions are complete, the Program counter is incremented by 2, and the cycle repeats. 

The Program Counter does not connect directly to the address bus. Instead, its value is first copied into the MAR. The MAR's only job is to hold the address of the memory location that the CPU wants to read from or write to. It decouples the CPU's internal operations from the memory bus, acting as a stable buffer for the memory address while the rest of the CPU prepares for the next step.
These registers are essential for managing the timing and flow of a real CPU. They solve the problem of different components being ready at different times.


Similarly, data does not flow directly from RAM to the Instruction Register. First it lands in the MDR. The MDR is a two way buffer. When reading from memory, data comes from RAM into the MDR. When writing to memory, data is put into the MDR before being sent to RAM.

From experimenting on the website further, it seems the Control Unit is essentially a state machine that sends out these tiny control signals (_out, _in, _inc) in a precise sequence for every instruction.

The ALU is where the if and while loops work at the hardware level. 

The parts of the CPU include: 

ALU (Arithmetic Logic Unit): This is where arithmetic and logic operations are done

Memory: This is where data and instructions are stored

Control Unit: This is the part of the CPU that fetches instructions from memory, decodes them and then directs the operation of other components of the CPU

Busses: These are what is used to transfer data and information between different components of the CPU




Intel Museum 

This website shows a virtual tour of Intel throughout the years, and through this tour, I learned the history and evolution of computing over the past few decades.
Intel was founded in July 1968 by Robert Noyce, Gordon Moore, and Arthur Rock. The founding occurred during a time of significant growth and innovation in the semiconductor industry, particularly in what would become known as Silicon Valley.

On April 1, 1969, Intel launched their first product, the 3101 RAM chip. 

Later on November 15, 1971, Intel introduced the 4004, the world’s first single chip microprocessor. The initial design was intended for a calculator, but it became a general purpose processing unit very soon. 

Following the 4004, Intel released the 8008 on April 1, 1972. It is an 8 bit microprocessor that was used in some early computing devices and was built on the foundation laid by 4004. 

On April 1, 1974, Intel introduced the 8080, which was a more powerful and popular 8 bit microprocessor. It became the CPU for many early computers and it was a key component in development of the CP/M operating system, playing a significant role in the early micro computer revolution. 

On June 8, 1978, Intel introduced the 8086 microprocessor, which established the 16-bit x86 architecture that would dominate personal computing for decades. The 8086 delivered significantly greater processing capability compared to its 8-bit predecessors.

Later on June 1, 1979, Intel introduced the 8088, a variation of the 8086 featuring an 8-bit external data bus. This design made it more cost effective to integrate with existing 8 bit components, and the 8088’s use in the groundbreaking IBM PC (introduced in 1981) made it a pivotal product for both Intel and the burgeoning personal computer industry.

On February 1, 1982, Intel released the 286 (80286), a 16 bit processor that brought protected mode capabilities to personal computers. This advancement enabled multitasking and expanded memory access beyond the limitations of the 8086/8088, powering the IBM PC/AT and subsequent compatible machines.

On October 17, 1985, Intel introduced the Intel386 processor, marking a major leap as the first full 32 bit x86 chip. The 386 provided essential capabilities for modern operating systems like Windows, including crucial features such as virtual memory and true multitasking.

On April 10, 1989, Intel introduced the Intel486 processor. This generation significantly boosted performance by integrating the math coprocessor and a cache directly onto the CPU die, resulting in substantial speed improvements over previous designs.

On March 22, 1993, Intel launched the Intel Pentium processor, alongside a new branding strategy. The Pentium featured a superscalar architecture, enabling it to execute multiple instructions simultaneously and leading to significant performance gains that supported the rapid growth of multimedia and the internet on PCs.
Throughout the Late 1990s and 2000s, Intel continued to introduce new processor generations, including the Pentium Pro, Pentium II, Pentium III, Pentium 4, and the Core Series. These releases showcased continuous architectural advancements, increased clock speeds, and higher transistor densities, solidifying Intel’s leadership and expanding the capabilities of the x86 architecture in personal computers.

From the mid 2000s onwards, Intel’s focus expanded beyond desktop PCs. The timeline shows the company’s efforts in mobile processors (with varying degrees of success), the development of powerful server processors for data centers, and investments in emerging technologies such as flash memory, FPGAs, and hardware designed for artificial intelligence.


Microprocessor design



Microchips and microprocessors are explained using the "goods truck analogy." It describes the microchip as a "city" where data ("goodies") are transported by "trucks"  along "highways" (connections/buses) between and through different parts of the city 

I learned how different parts of the design relates to the city. For example, clocking speed is described using the speed of delivery trucks, how CPU fabrication can mean having wider turns, construct guardrails, make the asphalt smoother to make the trucks faster, how pipelining refers to having trucks be ready to go when ones gone, how multi processor can refer to having a four laned road, how 32 and 64 bits refers to a truck being able to carry 1 ton vs 2 tons, how cache refers to having the warehouse being fit with the loading bay where the most popular goods are loaded first while waiting for truck to came back from deliveries.

I then learned that ISA defines the Processor's Language: The Instruction Set Architecture is the fundamental set of commands a CPU can execute.

I learned about CISC vs. RISC, and that historically, processor design followed two main paths: CISC (more complex, varied instructions) and RISC (simpler, fixed length instructions), each with design trade offs and performance implications.

I also learned that processors rely on essential instructions for:

Data Movement: Moving data between registers, memory, and I/O (Move, Load, Store). These are the most frequent.
Control Flow: Changing the sequence of instruction execution (Branch, Jump, Call, Return, Interrupt). Calls (and returns) are the second most frequent.
Computation: Performing arithmetic and logic operations (Arithmetic instructions handled by the ALU).
External Interaction: Communicating with input and output devices (Input/Output instructions).


From further reading, I understood that the instruction length and format matter. The way instructions are structured and their length significantly impact the complexity of the CPU design and its ability to select operations and operands efficiently. There are trade offs between code density, instruction complexity, and the number of available registers.

I also learned about how program execution involves fetching and data access. The CPU uses the Program Counter to track the next instruction in memory and can load/store data to/from memory as needed.

I learned about compatibility considerations as well. Designing new ISAs involves balancing new features with the need for compatibility (either binary or source code) with older architectures.


I learned what essential hardware components make up a typical microprocessor. It includes the Control Unit, I/O Units, Arithmetic Logic Unit (ALU), Registers, and Cache as key components. I then learned what the components do: The Control Unit interprets instructions and directs the operation of other components. I/O Units handle communication between the processor and the rest of the computer system, including memory and peripherals. The ALU is responsible for performing arithmetic and logical operations on data. Registers are the fastest memory locations within the CPU, used for temporary storage of data and instructions. Cache is an on chip memory that is faster than external RAM and used to store frequently accessed data to reduce the need for slower memory access.


I learned about HDD and SSD, how HDD is slower and uses moving parts and how SSD is faster. I learned about different types of RAM (SRAM and DRAM). SRAM is faster but takes up more space, and DRAM is slower but takes up less space. 

I learned about the fundamental language a processor understands, the ISA, or Instruction Set Architecture. I also learned about the two main historical approaches to ISA design, CISC and RISC, each with its own trade-offs and effects on performance.

I learned that key instruction types are essential for how processors work. These include instructions for moving data (Move, Load, Store), controlling program flow (Branch, Jump, Call, Return, Interrupt), performing calculations and logic (Arithmetic instructions via the ALU), and interacting with external devices (Input/Output).

I learned that instruction length and format are important design considerations. The way instructions are structured affects the complexity of the CPU and its ability to efficiently handle operations and data.

I learned about how program execution involves fetching instructions and accessing data. The CPU uses a Program Counter to keep track of where it is in a program and can retrieve or store data from memory as needed.

I also learned about compatibility considerations as well. Designing new ISAs involves balancing new features with the need for compatibility (either binary or source code) with older architectures.

I learned that the clock is the engine's pulse, providing the timing for the microprocessor's operations, with clock frequency indicating how many cycles occur per second.

I learned that CPI (Cycles Per Instruction) matters for true performance. Clock frequency alone isn't enough; the number of clock cycles needed for each instruction is crucial for understanding a processor's real speed.

I learned that IPS (Instructions Per Second) is a better performance metric. Calculated as Clock Frequency divided by CPI, it offers a more accurate measure of how many instructions a processor can execute in a given time.

I also learned that CPU time depends on multiple factors. The total time a program takes to run is influenced by the number of instructions, the cycles per instruction, and the clock cycle time. Improving performance often involves balancing these factors, sometimes with trade offs.

I also learned about Amdahl's Law, which shows that optimizing just one part of a computer system has limited overall performance gains. This is especially true if that part doesn't make up a large portion of the total execution time.

I learned that to achieve significant overall performance improvements, it's important to identify and focus on optimizing the parts of the system that are the biggest bottlenecks and take the most time to execute.



Microprocessor vs Microcontrollers

Microprocessor: A microprocessor is the device in a computer which makes things happen. It is capable of performing basic arithmetic operations, moving data from place to place, and making basic decisions based on the quantity of certain values. Microprocessors are typically referred to as general purpose processing units that are designed to be integrated into a larger system with peripherals and external RAM.
Uses: Desktop computers, laptops, servers, workstations

Microcontroller: It is also known as an embedded controller. It is a microprocessor with additional hardware integrated into a single chip. Many microcontrollers have RAM, ROM, A/D and D/A converters, interrupt controllers, timers, and even oscillators built into the chip itself. They are designed to be used in situations where a specific task needs to be performed without the need of a whole computer, and only a small amount of simple processing needs to be performed.
Uses: Calculator, toys, microwaves, remote controller 





Computer Revolution

Hardware and memory


Hardware:

I learned that computer hardware isn't just one thing, but a collection of physical parts that must work together. 

I learned the CPU (Central Processing Unit) is the main chip that actually runs programs. It fetches instructions from memory, performs calculations like adding numbers (arithmetic), and makes decisions (logic). It is the core that controls everything else and dictates how fast tasks are done.

I learned about input devices, like keyboard or mouse. These are how someone can give commands or data (input) to the computer. From an architecture perspective, this means there are pathways for this external information to get into the system and be processed by the CPU.

I learned about output devices, like my screen or a printer. These show me the results of what the computer has processed. This means there are pathways for data to go out of the system after the CPU has done its work.

I learned that storage devices, like a hard drive or SSD, are where the computer keeps information permanently, even when the computer is turned off (non volatile). This is different from RAM because it doesn't lose its data. It helped me to understand how the CPU accesses this slower, non volatile storage for programs and data files.

I learned that the motherboard is the main circuit board that everything plugs into. It has pathways (buses) that let the CPU, memory, storage, and other parts communicate with each other. The design of these pathways is a big part of computer architecture, affecting speed and capability.

Memory:


I learned that computer memory is a crucial workspace where the computer temporarily stores the data and instructions it is actively working at that moment. The CPU needs to access this information very quickly for the computer to be fast.

I learned about RAM. This is the main fast memory the CPU uses for running programs and processing data currently. It is volatile because it loses all its information when the computer is turned off. Its speed and size are critical architectural considerations.

I learned about ROM. This holds essential instructions that the computer needs to start up, like the BIOS of a computer. This information is permanent and does not get erased even when the power is off, and it usually cannot be changed or affected by me. It's a fundamental part of the boot process of a system.

I learned there's a key difference between primary storage, which is RAM (fast, temporary, for active work), and secondary storage, like hard drives or SSDs (slower, permanent, for long term storage of files and programs). 

I learned that memory is organized like a series of numbered mailboxes, where each small unit of memory has a unique address. The CPU uses these addresses to find and access specific pieces of data or instructions it needs. This addressing scheme is a core concept in architecture.

I learned that the amount of RAM a computer has is important because it determines how much information for active programs can be held at once. More RAM usually means the computer can handle more programs running at the same time without slowing down, as the CPU has more immediate workspace.








Jun 2, 2025


Compiler Explorer

This website has different programming languages with compilers that shows what happens to the high level language code in assembly code. This helps me learn about computer architecture in a direct way. 

When I look at the assembly code, I see terms like eax, rbx, rsp, etc. These are registers, which I know are tiny, super fast storage spots inside the CPU. I can see the compiler using them all the time to hold temporary values, pointers, or function arguments. It helps me understand why they're so important for speed and how they are used constantly.

If I define a variable or work with an array, the assembly code will show instructions like mov  or push/pop that involve memory addresses. 

By switching between different compilers or target architectures (like x86-64 and ARM64), I can see how the same C++ code can be translated into completely different sets of assembly code. I learned from this that different CPUs have different Instruction Set Architectures (ISAs), which are basically their own unique languages. 





References

Wikibooks contributors. (2023, May 18). The computer revolution. In Wikibooks.
https://en.wikibooks.org/wiki/The_Computer_Revolution 

Wikibooks contributors. (2024, January 24). Microprocessor design. In Wikibooks
https://en.wikibooks.org/wiki/Microprocessor_Design 

Intel Corporation. (n.d.). Intel Museum. Retrieved June 7, 2025
https://virtualmuseum.intel.com/ 

Břečka, J. (n.d.). CPU Visual Simulator. GitHub.
https://cpuvisualsimulator.github.io/ 

Godbolt, M. (n.d.). Compiler Explorer. 
https://godbolt.org/ 





I could not upload images, for a better more organized version with images: https://docs.google.com/document/d/1gxZ62IrJVL-VgxkRkEjwwkXTUKgvwhAeducKiUfDUSc/edit?tab=t.0 
