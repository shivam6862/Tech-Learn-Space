# Operating Systems

Operating systems manage hardware and provide services for computer programs. Functions include process management, memory management, file systems, and user interfaces.

### Introduction to Operating System and its Functions:

An operating system (OS) is a software that acts as an intermediary between computer hardware and the computer user. Its primary functions include:

1. **Process Management:** Allocating resources to different tasks and managing their execution.

2. **Memory Management:** Controlling and coordinating the use of the computer's memory.

3. **File System Management:** Organizing and managing files on storage devices.

4. **Device Management:** Managing peripheral devices connected to the computer.

5. **Security and Protection:** Ensuring the security of data and resources and protecting against unauthorized access.

### Types of Operating Systems:

1. **Batch Operating System:** Processes in batches without user interaction.

2. **Multiprogramming Operating System:** Runs multiple programs simultaneously.

3. **Multitasking Operating System:** Allows multiple tasks to run concurrently.

4. **Real-Time Operating System:** Responds to input instantly, commonly used in embedded systems.

5. **Distributed Operating System:** Runs on multiple machines and allows them to work together.

6. **Clustered Operating System:** Multiple systems working together for improved performance and availability.

7. **Embedded Operating System:** Designed for specific embedded devices.

### Process States and Schedulers:

- **Process States:**

  - **Running:** The process is being executed.
  - **Ready:** The process is waiting for CPU time.
  - **Blocked:** The process is waiting for some event (e.g., I/O).

- **Schedulers:**
  - **Long-term Scheduler:** Selects processes from the job pool to bring them into the ready queue.
  - **Short-term Scheduler:** Selects processes from the ready queue to run on the CPU.
  - **Medium-term Scheduler:** Swaps processes in and out of the main memory.

### Important Linux Commands:

- **ls:** List directory contents.
- **cd:** Change directory.
- **pwd:** Print working directory.
- **cp:** Copy files or directories.
- **mv:** Move or rename files/directories.
- **rm:** Remove/delete files or directories.
- **mkdir:** Create a new directory.
- **chmod:** Change file permissions.
- **ps:** Display information about processes.
- **kill:** Terminate a process.

### System Calls in Operating System and Types:

System calls are functions provided by the operating system for program execution. Types include:

1. **Process Control:** Create, terminate processes.
2. **File Manipulation:** Open, close, read, write files.
3. **Device Manipulation:** Request I/O services.
4. **Information Maintenance:** Get or set system information.
5. **Communication:** Create, manage communication between processes.

### Fork System Call:

Creates a new process (child) by duplicating the existing process (parent).

### User Mode and Kernel Mode:

- **User Mode:** Restricted mode where user applications run.
- **Kernel Mode:** Privileged mode where the OS kernel executes.

### Process vs. Threads:

- **Process:** An independent program with its own memory space.
- **Thread:** A lightweight, smaller unit of a process, sharing its memory space.

### User Level vs. Kernel Level Thread:

- **User Level Thread:** Managed by user-level libraries, without kernel involvement.
- **Kernel Level Thread:** Managed by the operating system kernel.

### CPU Scheduling Algorithms:

1. **FCFS (First Come First Serve):** Processes are executed in the order they arrive.

2. **SJF (Shortest Job First):** Executes the shortest job first.

3. **SJF with Preemption:** Allows preemption of a running process if a shorter job arrives.

4. **Round Robin (RR):** Each process gets a fixed time on the CPU, then moves to the back of the queue.

5. **Pre-emptive Priority Scheduling:** Priority-based scheduling with preemption.

6. **Mix Burst Time:** Handles both CPU and I/O burst times.

7. **Multi-Level Queue Scheduling:** Processes are divided into multiple queues with different priority levels.

8. **Multilevel Feedback Queue Scheduling:** Allows processes to move between queues based on their behavior to reduce starvation.

### CPU Scheduling Terms:

- **Arrival Time:** Time when a process arrives in the ready queue.
- **Burst Time:** Time required by a process to complete its execution.
- **Completion Time:** Time at which a process completes its execution.
- **Turnaround Time:** Total time taken by a process to complete from arrival to completion.
- **Waiting Time:** Total time a process spends waiting in the ready queue.
- **Response Time:** Time taken to respond to the first input.

### Process Synchronization | Process Types | Race Condition:

- **Process Synchronization:**
  - It is the coordination of concurrent processes to avoid conflicts that may arise when multiple processes access shared resources simultaneously.
- **Process Types:**

  - **Independent Process:** Executes independently without affecting other processes.
  - **Cooperating Process:** Interacts with other processes by sharing data.

- **Race Condition:**
  - A race condition occurs when the behavior of a system depends on the relative timing of events, such as the order of execution of processes.

### Producer-Consumer Problem | Process Synchronization Problem:

- **Producer-Consumer Problem:**

  - A classical synchronization problem where there are two types of processes - producers that produce items and put them into a buffer, and consumers that take items from the buffer.

- **Printer-Spooler Problem:**
  - Another synchronization problem where multiple processes want to print documents. A spooler manages the print queue to avoid conflicts.

### Critical Section Problem | Mutual Exclusion, Progress, and Bounded Waiting:

- **Critical Section:**

  - A section of code where shared resources are accessed, and only one process can execute it at a time.

- **Mutual Exclusion:**

  - Ensuring that only one process accesses the critical section at a time.

- **Progress:**

  - If no process is in the critical section and some processes wish to enter it, then only those processes not in the remainder section can participate in deciding which will enter.

- **Bounded Waiting:**
  - There exists a bound, or limit, on the number of times other processes are allowed to enter their critical sections after a process has made a request to enter its critical section.

### LOCK Variable in OS | Process Synchronization:

- **Lock Variable:**
  - A variable used to implement mutual exclusion. When a process enters the critical section, it sets the lock, and other processes must wait until the lock is released.

### Test and Set Instruction in OS | Process Synchronization:

- **Test and Set Instruction:**
  - An atomic instruction that tests a variable and sets it to a new value in a single, uninterruptible operation. It is often used to implement locks.

### Turn Variable | Strict Alteration Method | Process Synchronization:

- **Turn Variable:**

  - A variable used to determine which process has the right to enter its critical section next.

- **Strict Alteration Method:**
  - A synchronization method where processes take turns entering their critical sections.

### Semaphores | Wait, Signal Operation | Counting Semaphore:

- **Semaphore:**

  - A synchronization tool used to control access to a shared resource. It can be a binary semaphore or a counting semaphore.

- **Wait Operation:**

  - Decrements the value of the semaphore. If the value becomes negative, the process is blocked.

- **Signal Operation:**

  - Increments the value of the semaphore. If the previous value was negative, it unblocks a waiting process.

- **Counting Semaphore:**
  - A semaphore that can have an integer value greater than or equal to zero.

### Binary Semaphore:

- A semaphore with only two possible values: 0 and 1. It is often used to represent mutex locks.

### Solution of Readers-Writers Problem using Binary Semaphore:

- A classical synchronization problem where multiple readers and writers access shared data. Binary semaphores are often used to implement a solution that ensures mutual exclusion.

### Dining Philosophers Problem and Solution using Semaphore:

- A synchronization problem where philosophers sit around a dining table, and to eat, they need two forks. Semaphores can be used to avoid deadlock and ensure that philosophers can eat without conflicts.

### DEADLOCK concept:

- **Deadlock:**
  - A situation where two or more processes are unable to proceed because each is waiting for the other to release a resource.

### Resource Allocation Graph in Deadlock | Single Instance:

- **Resource Allocation Graph:**

  - A graph that depicts the allocation of resources to processes and the relationships between them. It helps in identifying and preventing deadlocks.

- **Single Instance:**
  - Each resource type has only one instance.

### Multi-Instance Resource Allocation Graph:

- Resources can have multiple instances in this type of resource allocation graph.

### Deadlock Handling Methods and Deadlock Prevention:

- **Deadlock Handling Methods:**
  - **Deadlock Detection and Recovery:** Identify deadlocks and take corrective actions.
  - **Deadlock Avoidance:** Ensure that deadlocks never occur.
  - **Deadlock Prevention:** Avoid conditions that could lead to deadlock.

### Deadlock Avoidance Banker's Algorithm:

- **Banker's Algorithm:**
  - A deadlock avoidance algorithm that ensures the system remains in a safe state by checking if resource allocation requests will leave the system in a safe or unsafe state.

### Memory Management and Degree of Multiprogramming:

- **Memory Management:**

  - The process of managing computer memory, including RAM and other storage devices.

- **Degree of Multiprogramming:**
  - The number of processes that can be in memory simultaneously.

### Memory Management Techniques | Contiguous and Non-Contiguous:

- **Contiguous Memory Management:**

  - Allocate a single contiguous block of memory to a process.

- **Non-Contiguous Memory Management:**
  - Allocate memory in non-contiguous blocks, often through paging or segmentation.

### Internal Fragmentation | Fixed Size Partitioning | Memory Management:

- **Internal Fragmentation:**

  - Wasted memory within a partition due to the allocation of more space than needed.

- **Fixed Size Partitioning:**
  - Divides memory into fixed-size partitions.

### Variable Size Partitioning | Memory Management:

- Allows processes to occupy varying amounts of memory.

### First Fit, Next Fit, Best Fit, Worst Fit Memory Allocation | Memory Management:

- **First Fit:** Allocates the first available block that is large enough.
- **Next Fit:** Like First Fit, but starts searching from the last allocation point.
- **Best Fit:** Allocates the smallest available block that fits.
- **Worst Fit:** Allocates the largest available block.

### Need of Paging | Memory Management:

- **Paging:**
  - A memory management scheme that eliminates the need for contiguous allocation of physical memory.

### What is Paging | Memory Management:

- A technique where processes are divided into fixed-size pages, and these pages are loaded into non-contiguous frames in memory.

### Page Table Entries | Format of Page Table:

- **Page Table Entries:**
  - Contains information about each page in a process, including the frame number where the page is stored.

### 2-Level Paging in Operating System | Multilevel Paging:

- A hierarchical page table structure where the page table itself is divided into multiple levels.

### Inverted Paging | Memory Management:

- **Inverted Paging:**
  - In traditional paging, each process has its own page table, mapping virtual pages to physical frames. In inverted paging, a single page table is used for the entire system, and each entry in the table corresponds to a frame. This method is more memory-efficient but requires searching the entire table for a mapping.

### Thrashing:

- **Thrashing:**
  - Occurs when a computer's performance degrades due to excessive paging (constant swapping of pages in and out of main memory). It leads to a high page-fault rate, causing the system to spend more time swapping pages than executing actual instructions.

### Segmentation vs. Paging | Segmentation Working:

- **Segmentation:**

  - Divides a program into segments (logical units) like code, data, and stack.

- **Paging:**

  - Divides a program into fixed-size pages, allowing for non-contiguous allocation.

- **Segmentation Working:**
  - Segments are assigned varying sizes dynamically, providing flexibility. Paging divides memory into fixed-size blocks.

### Overlay | Memory Management:

- **Overlay:**
  - Technique to overcome memory limitations by dividing a program into modules. Only the necessary modules are loaded into memory at a time, replacing them as needed.

### Virtual Memory | Page Fault | Significance of Virtual Memory:

- **Virtual Memory:**

  - An abstraction that provides an illusion to users that each process has its own dedicated memory. It allows for more processes to run than there is physical memory.

- **Page Fault:**

  - A page fault occurs when the desired page is not in main memory, leading to a swap from secondary storage to main memory.

- **Significance of Virtual Memory:**
  - Allows processes to be larger than physical memory, facilitating efficient multitasking and the execution of more complex programs.

### Translation Lookaside Buffer (TLB):

- **TLB:**
  - A small, fast cache that stores recent translations from virtual memory to physical memory, reducing the need to access the page table.

### Page Replacement Introduction | FIFO Page Replacement Algorithm:

- **Page Replacement:**

  - When a page needs to be brought into memory, and there's no space, an existing page must be evicted. Page replacement algorithms decide which page to replace.

- **FIFO (First-In-First-Out) Page Replacement Algorithm:**
  - The oldest page in memory is the first to be replaced.

### Belady's Anomaly in FIFO Page Replacement:

- **Belady's Anomaly:**
  - Occurs when increasing the number of frames leads to an increase in page faults, defying the principle that more memory should result in fewer page faults. FIFO exhibits Belady's Anomaly.

### Optimal Page Replacement Algorithm:

- **Optimal Page Replacement Algorithm:**
  - Replaces the page that will not be used for the longest period, providing the minimum possible page faults. It is not practical for implementation due to its predictive nature.

### Least Recently Used Page Replacement Algorithm:

- **Least Recently Used (LRU) Page Replacement Algorithm:**
  - Replaces the page that has not been used for the longest time.

### Most Recently Used Page Replacement Algorithm:

- **Most Recently Used (MRU) Page Replacement Algorithm:**
  - Replaces the page that has been used most recently.

### Hard Disk Architecture:

- **Hard Disk Architecture:**
  - Consists of one or more platters, each with its own read/write head. Data is stored in tracks and sectors on the platters.

### Disk Access Time | Seek Time, Rotational Time, and Transfer Time:

- **Disk Access Time:**

  - The time it takes to locate and transfer data from a storage device.

- **Seek Time:**

  - Time taken for the read/write head to move to the desired track.

- **Rotational Time:**

  - Time taken for the desired sector to rotate under the read/write head.

- **Transfer Time:**
  - Time taken to actually transfer the data.

### Disk Scheduling Algorithm:

1. **FCFS in Disk Scheduling:**

   - Requests are served in the order they arrive.

2. **SSTF in Disk Scheduling:**

   - Serves the request with the shortest seek time.

3. **SCAN Algorithm in Disk Scheduling:**

   - The read/write head moves in one direction, serving requests until the end, then reverses.

4. **LOOK Algorithm in Disk Scheduling:**

   - Similar to SCAN, but the head reverses direction when there are no more requests in one direction.

5. **C-SCAN Algorithm in Disk Scheduling:**

   - Similar to SCAN but moves only in one direction, servicing requests until the end, then jumping to the beginning.

6. **C-LOOK Algorithm in Disk Scheduling:**
   - Similar to LOOK but jumps to the beginning after reaching the end of requests.

### File System in Operating System:

- **File System:**
  - Manages files on a storage device, providing a structure for organizing and accessing data.

### File Attributes & Operations:

- **File Attributes:**

  - Characteristics associated with a file, such as size, type, creation time, etc.

- **File Operations:**
  - Actions that can be performed on files, including read, write, create, delete, etc.

### Allocation Methods in Operating System | Contiguous vs. Non-Contiguous:

- **Allocation Methods:**

  - Strategies for allocating space to files in a file system.

- **Contiguous Allocation:**
  - Allocates a continuous block of space to a file.

### Contiguous Allocation | Advantages & Disadvantages:

- **Advantages:**

  - Simple and efficient for sequential access.

- **Disadvantages:**
  - Fragmentation issues; inefficient for dynamic storage needs.

### Linked List Allocation in File Allocation:

- Allocates space to a file using a linked list data structure.

### Indexed File Allocation:

- Allocates space using an index block that contains pointers to data blocks.

### Unix Inode Structure:

- **Inode (Index Node):**
  - A data structure on Unix-like file systems that stores information about a file or directory.

### Protection & Security in Operating System:

- **Protection:**

  - Ensures that unauthorized users do not access or modify data.

- **Security:**
  - Protects the system from intentional or accidental harm.
