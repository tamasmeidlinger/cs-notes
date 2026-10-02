# Data Storage

## Bits and their storage

### Bits and Bit Patterns

Inside today’s computers all information is encoded as patterns of 0s and 1s called **bits** (short for binary digits).
Bit Patterns are used to represent information.

### Gates and Flip-flops

A device that produces the output of a Boolean operation when given the
operation’s input values is called a **gate**, or sometimes a **logic gate**.
- **A logic gate is a hardware abstraction that is modeled by a Boolean function.**

![Logical Gates](images/logical-gates.png)

#### Flip-Flop Circuit

A flip-flop is a fundamental
unit of computer memory. It is a circuit that produces an output value
of 0 or 1, which remains constant until a pulse (a temporary change to
a 1 that returns to 0) from another circuit causes it to shift to the other
value.

- **In other words, the output can be set to “remember” a zero or a one
under control of external stimuli.**

![Flip-flop circuit](images/flip-flop-1.png)

![Demonstration of flip-flop circuit](images/flip-flop-2.png)

![Different version of a flip-flop circuit](images/flip-flop-3.png)

    Essential knowledge
    - Binary data is processed by physical layers of computing hardware, including gates, chips, and components.
    - Hardware is built using multiple levels of abstractions, such as transistors, logic gates, chips, memory, motherboards, special purposes cards, and storage devices.

### Hexadecimal notation

A long string of bits is often called a **stream**

To simplify the representation of long bit patterns we use a
shorthand notation called **hexadecimal notation**

- bit patterns within a machine tend to have lengths in multiples of four
- hexadecimal notation uses a single symbol to represent a pattern of four bits
- math subscripts to indicate the base of a non-decimal number
    - the hexadecimal value for $15_{10}$ is $F_{16}$
- the common prefix “0x” in front of our
hexadecimal numbers

![Hexadecimal Encoding System](images/hexadecimal-encoding-system.png)

## Main Memory

For the purpose of storing data, a computer contains a large collection of circuits (such as flip-flops), each capable of storing a single bit. This bit reservoir is known as the machine’s main memory.

- A computer’s main memory is organized in manageable units called **cells**
- a typical cell size being eight bits
- A string of eight bits is called a byte

Although there is no left or right within a computer, we normally envision the bits within a memory cell as being arranged in a row. The left end of this row is called the **high-order end**, and the right end is called the **low-order end**. The leftmost bit is called either the high-order bit or the **most significant bit** in reference to the fact that if the contents of the cell were interpreted as representing a numeric value, this bit would be the most significant digit in the number. Similarly, the rightmost bit is referred to as the **low-order bit** or the **least significant bit**.

![Memory cell organization](/images/memory-cell.png)

- To identify individual cells in a computer’s main memory, each cell is assigned a unique “name,” called its **address**.
- Such an addressing system not only gives us a way of uniquely identifying each cell but also associates an order to the cells such as "the next cell" or "the previous cell."
- Assigning an order to both the cells in main memory and the bits within each cell makes the entire collection of bits within a computer’s main memory is essentially ordered in one long row
- Pieces of
this long row can therefore be used to store bit patterns that may be longer
than the length of a single cell
    - store a string of 16
bits merely by using two consecutive memory cells

![Memory cells and addresses](/images/memory-cells-addresses.png)

Because a computer’s main memory is organized as individual, addressable cells, the cells can be accessed independently as required. To reflect the ability to access cells in any order, a computer’s main memory is often called **random access memory (RAM)**

### Measuring Memory Capacity

It is convenient to design main memory systems in which the total number of cells is a power of two.

| Unit | Symbol | Equivalent |
|---|---:|---:|
| Bit | bit (b) | 0 or 1 |
| Byte | B | 8 bits |
| Kibibyte | KiB | 1,024 B = 2¹⁰ B |
| Mebibyte | MiB | 1,024 KiB = 2²⁰ B |
| Gibibyte | GiB | 1,024 MiB = 2³⁰ B |
| Tebibyte | TiB | 1,024 GiB = 2⁴⁰ B |

**Important:** KB, MB, GB technically refer to decimal units (1,000), while KiB, MiB, GiB are binary units (1,024). For computer memory, the binary units are often what you want.

## Mass Storage

Due to the volatility and limited size of a computer’s main memory, most
computers have additional memory devices called mass storage (or secondary storage) systems.

- magnetic disks
- CDs, DVDs
- magnetic tapes
- flash drives and solid-state drives

### Magnetic Systems

The most common example in use today is the magnetic disk or hard disk drive (HDD), in which a thin, spinning disk with magnetic coating is used to hold data.

![Disk Storage System](images/disk-storage-system.png)

    Essential knowledge
    - The bandwidth of a system is a measure of bit rate—the amount of data (measured in bits) that can be sent in a fixed amount of time.
    - The latency of a system is the time elapsed between the transmission and the receipt of a request.

### Optical Systems

Another class of mass storage systems applies optical technology.

- **Compact Disk (CD)**
    - These disks are 12 centimeters (approximately 5 inches) in diameter and consist of reflective material covered with a clear protective coating.
    - Information is recorded on them by creating variations in their reflective surfaces.
    - This information can then be retrieved by means of a laser that detects irregularities on the reflective surface of the CD as it spins.
    - Traditional CDs have capacities in the range of 600 to 700MB

![CD storage format](images/cd-storage.png)

- **DVDs (Digital Versatile Disks)**
    - are constructed from multiple, semi-transparent layers that serve as distinct surfaces when viewed by a precisely focused laser
    - provide storage capacities of several GB

- **BDs (Blu-ray Disks)**
    - Uses Blu-ray technology, which uses a laser in the blue-violet spectrum of light (instead of red), is able to focus its laser beam with very fine precision.
    - provide over five times the capacity of a DVD

### Flash Drives

Mass storage systems based on magnetic or optic technology uses physical motion such as spinning disks, moving read/write heads, and aiming laser beams to store and retrieve data.
Data storage and retrieval is slow compared to the speed of electronic circuitry

#### Flash Memory Technology

In a flash memory system, bits are stored by sending electronic signals directly to the storage medium where they cause electrons to be trapped in tiny chambers of silicon dioxide, thus altering the characteristics of small electronic circuits.

Although data stored in flash memory systems can be accessed in small, byte-size units as in RAM applications, current technology dictates that stored data be erased in large blocks.

- repeated erasing slowly damages the silicon dioxide chambers
- current flash memory technology is not suitable for general main memory applications where its contents might be altered many times a second.

**Devices:**

Flash memory devices called ***flash drives***, with capacities of hundreds of GBs, are available for general mass storage applications

Larger flash memory devices called **SSDs (solid-state drives)** are explicitly designed to take the place of magnetic hard disks.

- SSD sectors suffer from the more limited lifetime of all flash memory technologies, but the use of wear-leveling techniques can reduce the impact of this by relocating frequently altered data blocks to fresh locations on the drive.

Another application of flash technology is found in **SD (Secure Digital)memory cards** (or just SD cards).

- These provide up to two GBs of storage and are packaged in a plastic-rigged wafer about the size of a postage stamp. (SD cards are also available in smaller mini and micro sizes.)

**SDHC (High Capacity) memory cards** can provide up to 32 GBs and the next generation **SDXC (Extended Capacity) memory cards** can exceed a TB
