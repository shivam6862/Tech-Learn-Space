# Computer Architecture

Computer architecture covers the design and organization of computer systems. Topics include CPU design, instruction set architecture, memory hierarchy, and input/output systems.

### Von Neumann's Architecture | Stored Memory Concept:

- **Von Neumann's Architecture:**

  - Named after John von Neumann, it is a computer architecture that uses the same memory space for data and instructions. The CPU fetches instructions from memory and processes them sequentially.

- **Stored Memory Concept:**
  - The idea that both data and instructions are stored in the same memory, and the CPU fetches instructions from memory for execution.

### Various General Purpose Registers:

- **General Purpose Registers:**
  - Registers within the CPU that can be used for various purposes, such as storing data temporarily during computation.

### Types of Buses (Address, Data, and Control):

- **Address Bus:**

  - Carries memory addresses from the CPU to memory or I/O devices.

- **Data Bus:**

  - Transfers data between the CPU, memory, and I/O devices.

- **Control Bus:**
  - Carries control signals that coordinate and manage the activities of various components in the system.

### Common Bus System using Multiplexer:

- **Common Bus System:**

  - A system where multiple components share a common bus for communication.

- **Multiplexer:**
  - A device that selects one of many input signals and directs it to a single output.

### Common Bus System | How Basic Computer Works:

- **Common Bus System (Recap):**

  - Components communicate using a shared bus for transferring data and control signals.

- **How Basic Computer Works:**
  - Fetches instructions from memory, decodes them, performs operations, and stores results—all facilitated by the common bus.

### Types of Instructions in General Purpose Computer:

1. **Data Transfer Instruction:**

   - Moves data between registers or between memory and registers.

2. **Arithmetic Instructions (Data Manipulation):**

   - Perform basic arithmetic operations like addition, subtraction, multiplication, and division.

3. **Logical Instructions (Data Manipulation):**

   - Perform logical operations like AND, OR, NOT.

4. **Shift Instructions (Data Manipulation):**
   - Shift bits in a register left or right.

### Program Control Instructions (Types of Control Instructions):

- **Program Control Instructions:**
  - Direct the sequence of execution of instructions in a program.

### What is Instruction Format:

- **Instruction Format:**
  - Describes the structure of a machine instruction, including the opcode (operation code) and operand fields.

### Single Accumulator CPU Organization | Single Address Instructions:

- **Single Accumulator CPU Organization:**

  - Uses a single register (accumulator) for most arithmetic operations.

- **Single Address Instructions:**
  - Instructions that specify a single operand, often the accumulator.

### General Register CPU Organization | Two and Three Address Instructions:

- **General Register CPU Organization:**

  - Employs multiple general-purpose registers for operations.

- **Two Address Instructions:**

  - Operations involving two operands.

- **Three Address Instructions:**
  - Operations involving three operands.

### Register Stack Organization | Zero Address Instructions:

- **Register Stack Organization:**

  - Uses a stack of registers for operations.

- **Zero Address Instructions:**
  - Operations that do not explicitly specify operands.

### Memory Stack Organization | Memory Stack vs. Register Stack:

- **Memory Stack Organization:**

  - Uses a stack in memory for operations.

- **Memory Stack vs. Register Stack:**
  - Memory stack operations involve reading from and writing to memory, whereas register stack operations use registers directly.

### What is Addressing Mode | Various Types of Addressing Modes:

- **Addressing Mode:**
  - Specifies how an operand is designated, determining how the operand's address is calculated.

1. **Implied Addressing Mode:**

   - The operand is implicit in the operation, requiring no additional specification.

2. **Immediate Addressing Mode:**

   - The operand is directly specified within the instruction.

3. **Register Mode | Addressing Mode:**

   - The operand is a register.

4. **Register Indirect Mode | Addressing Modes:**

   - The content of a register is used as an address to access data.

5. **Auto Increment and Decrement Addressing Modes:**

   - The address in a register is automatically incremented or decremented after accessing data.

6. **Direct Addressing Mode:**

   - The operand's address is explicitly given in the instruction.

7. **Indirect Addressing Mode:**

   - The operand's address is located in a register or memory location.

8. **Relative Addressing Mode:**

   - The operand's address is specified as a displacement from the current program counter or instruction.

9. **Base Register Addressing Mode:**

   - Uses a base register value to calculate the operand's address.

10. **Indexed Addressing Mode:**

- Uses an index value added to a base address to calculate the operand's address.

### Memory Hierarchy in Computer Architecture | Access Time, Speed, Size, Cost:

- **Memory Hierarchy:**

  - A hierarchical arrangement of different types of memory, organized based on speed, size, and cost.

- **Access Time:**

  - The time it takes for the CPU to retrieve data from or store data into a memory location.

- **Speed:**

  - The rate at which data can be accessed or transferred.

- **Size:**

  - The capacity of the memory.

- **Cost:**
  - The expense associated with manufacturing the memory.

### Independent vs. Hierarchical Memory Organization | 2-Level Memory Organization:

- **Independent Memory Organization:**

  - Each level of memory operates independently.

- **Hierarchical Memory Organization:**

  - Memory levels are organized in a hierarchy, with each level acting as a cache for the level below it.

- **2-Level Memory Organization:**
  - A memory system with two levels, typically involving a faster, smaller, and more expensive level (e.g., cache) and a slower, larger, and less expensive level (e.g., main memory).

### 3-Level Memory Organization:

- A memory system with three levels, typically involving cache, main memory, and secondary storage.

### Cache Mapping || Cache Mapping Techniques:

- **Cache Mapping:**

  - The process of determining where to place blocks in the cache.

- **Cache Mapping Techniques:**

  1. **Direct Mapping:**
     - Each block of main memory maps to exactly one block in the cache.
  2. **Fully Associative Mapping:**
     - Any block of main memory can map to any block in the cache.
  3. **Set Associative Mapping:**
     - A compromise between direct and fully associative, where each set has multiple blocks, and a block from main memory can map to any block within the set.

- **Advantages and Disadvantages of Direct Mapping:**
  - **Advantages:** Simple and fast.
  - **Disadvantages:** Limited flexibility, potential for conflicts.

### Locality of Reference in Cache Memory | Spatial Vs. Temporal Locality:

- **Locality of Reference:**

  - The tendency of a program to access a relatively small portion of the address space for a certain period.

- **Spatial Locality:**

  - Refers to accessing nearby addresses in memory.

- **Temporal Locality:**
  - Refers to accessing the same memory locations repeatedly over a short period.

### Cache Replacement Algorithms:

1. **LRU (Least Recently Used) Cache Replacement Algorithm:**

   - Evicts the least recently used block.

2. **FIFO Cache Replacement Policy:**

   - Evicts the oldest block.

3. **LRU (Least Recently Used) Cache Replacement Policy (repeated):**
   - Ensures that the least recently used block is evicted.

### Pipelining Introduction and Structure:

- **Pipelining:**

  - A technique that enables the CPU to overlap the execution of multiple instructions, improving throughput.

- **Pipelining Structure:**
  - Comprises multiple stages (fetch, decode, execute, etc.), with each stage handling a specific task in instruction execution.

### Pipelining Vs. Non-Pipelining | Instruction Execution | Speedup, Efficiency, Utilization:

- **Pipelining:**

  - Overlapping execution of multiple instructions.

- **Non-Pipelining:**

  - Instructions are executed one at a time.

- **Speedup:**

  - The ratio of the time taken without pipelining to the time taken with pipelining.

- **Efficiency:**

  - The ratio of speedup to the number of pipeline stages.

- **Utilization:**
  - The percentage of time a pipeline stage is actively processing an instruction.

### Stage Delay in Pipeline:

- **Stage Delay:**
  - The time taken for an instruction to pass through a specific stage of the pipeline.

### Hazard in Pipelining | Various Types of Hazards:

- **Hazard in Pipelining:**

  - Situations that prevent the next instruction from executing during its designated pipeline stage.

- **Various Types of Hazards:**
  - **Structural Hazards:**
    - Conflicts in resource usage.
  - **Control Hazards:**
    - Depend on the control flow of instructions.
  - **Data Hazards:**
    - Depend on data dependencies between instructions.

### Structural Hazards in Pipelining | Types of Hazards:

- **Structural Hazards:**
  - Conflicts in resource usage.

### Control Hazards in Pipelining | Types of Hazards:

1. **Read After Write (RAW) Hazards | Data Hazard in Pipelining:**

   - A dependence where a later instruction reads a value before a prior instruction writes it.

2. **Write After Read Hazard | Data Hazards:**

   - A dependence where a later instruction writes a value before a prior instruction reads it.

3. **Write After Write Hazard | Data Hazards in Pipelining:**
   - A dependence where two instructions both attempt to write to the same location.

### Register Renaming in Computer Organization | Data Hazard:

- **Register Renaming:**
  - A technique used to eliminate data hazards by mapping logical registers to physical registers dynamically.

### I/O Interface in Computer Organization:

- **I/O Interface:**
  - The mechanism that allows the CPU and memory to communicate with external devices.

### Interrupts in 8085 Microprocessor | Types of Interrupts in Computer Organization:

- **Interrupts in 8085 Microprocessor:**

  - Signals that temporarily halt the normal execution of a program.

- **Types of Interrupts:**
  - **Maskable Interrupts:**
    - Can be disabled or enabled by the programmer.
  - **Non-Maskable Interrupts:**
    - Cannot be disabled by the programmer.

### Daisy Chaining in Priority Interrupt | Priority-Based Interrupt in I/O Organization:

- **Daisy Chaining in Priority Interrupt:**

  - A priority resolution technique where devices are connected in a chain, and each device signals the next in the chain if it has an interrupt.

- **Priority-Based Interrupt in I/O Organization:**
  - Devices are assigned priority levels, and the CPU services the highest priority interrupt first.

### Parallel Priority Interrupt | I/O Organization:

- **Parallel Priority Interrupt:**
  - Multiple interrupt request lines are used, each corresponding to a different priority level.

### RISC vs. CISC | Computer Organization & Architecture:

- **RISC (Reduced Instruction Set Computing):**

  - Emphasizes a small and highly optimized set of instructions, with each instruction taking one clock cycle.

- **CISC (Complex Instruction Set Computing):**
  - Supports a larger and more complex instruction set, with instructions taking multiple clock cycles.

### Operand Forwarding in Computer Organization & Architecture | Data Hazard:

- **Operand Forwarding:**
  - A technique where the result of an instruction is forwarded directly to another instruction, eliminating the need to store the result in a register.
