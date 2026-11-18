Source: see manifest row of the PDF
PDF sha256: d3a9c449e301cfddd0d14f20733875900207357633a68a832a731039cbf00e7d
License: CC-BY-4.0
Language: eng
Fidelity: machine-gated

# Transcription of gazziro_2024_design_evaluation_open_source_soft_core_processors.pdf

Transcription of `gazziro_2024_design_evaluation_open_source_soft_core_processors.pdf` in this directory, 20 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-20 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

electronics
Article

Design and Evaluation of Open-Source Soft-Core Processors
Mario Gazziro 1,2 , Jecel Mattos de Assumpção Junior 2 , Oswaldo Hideo Ando Junior 3 ,
Marco Roberto Cavallari 4 and João Paulo Carmo 2, *
1

2

3

4

*

Information Engineering Group, Department of Engineering and Social Sciences (CECS), Federal University
of ABC (UFABC), Santo André 09210-580, Brazil; mario.gazziro@ufabc.edu.br
Group of Metamaterials Microwaves and Optics (GMeta), Department of Electrical Engineering (SEL),
University of São Paulo (USP), Avenida Trabalhador São-Carlense, Nr. 400, Parque Industrial
Arnold Schimidt, São Carlos 13566-590, Brazil; jecel@merlintec.com
Academic Unit of Cabo de Santo Agostinho (UACSA), Federal Rural University of Pernambuco (UFRPE),
Cabo de Santo Agostinho 54518-430, Brazil; oswaldo.ando@ufrpe.br
Department of Electronics and Biomedical Engineering (DEEB), School of Electrical and Computer
Engineering (FEEC), State University of Campinas (UNICAMP), Campinas 13083-852, Brazil;
mrcavall@unicamp.br
Correspondence: jcarmo@sc.usp.br

Abstract: The advantage of FPGAs lies in their ability to implement a fully hardware solution
for interfacing with various input/output (I/O) devices. Each block can work in parallel with all
the others, simplifying the satisfaction of timing constraints. However, this hardware utilization
consumes FPGA resources that could otherwise be allocated to the primary project. An alternative
involves employing a small “soft-core” processor to implement I/O in software. With the goal of
designing and evaluating a new tiny soft-core processor optimized for FPGA resources in I/O, a
novel processor named Baby8 is developed. It is an 8-bit CISC soft-core processor optimized for
reduced FPGA resources, including program size for 8-bit applications. The number of instructions is
not large, but any instruction can access arbitrary memory locations. The performance and resource
utilization of the newly designed processor are evaluated and compared with a variety of other
soft-core processors. The results demonstrate its competitive performance, achieving an average
maximum clock frequency of approximately 57 MHz and a power consumption of around 2 mW.
Furthermore, it conserves nearly half of the FPGA resources in implementation.
Citation: Gazziro, M.; Junior, J.M.d.A.;
Junior, O.H.A.; Cavallari, M.R.;

Keywords: optimization; soft core; processor; FPGA; ASIC; RISC-V; CISC

Carmo, J.P. Design and Evaluation of
Open-Source Soft-Core Processors.
Electronics 2024, 13, 781. https://
doi.org/10.3390/electronics13040781
Academic Editor: Paris Kitsos
Received: 30 December 2023
Revised: 7 February 2024
Accepted: 12 February 2024
Published: 16 February 2024

Copyright: © 2024 by the authors.
Licensee MDPI, Basel, Switzerland.
This article is an open access article
distributed under the terms and
conditions of the Creative Commons
Attribution (CC BY) license (https://
creativecommons.org/licenses/by/
4.0/).

1. Introduction
FPGAs offer the flexibility to implement a fully operational hardware solution for
interfacing with diverse I/O devices, allowing the blocks to operate in parallel, simplifying
their timing constraint fulfillment. However, the drawback is the consumption of FPGA
resources that could be directed towards the main project. A viable alternative is employing
a small “soft-core” processor for software-based I/O implementation. This approach saves
resources in two ways: block RAM bits are smaller compared to separate flip-flops in
configurable blocks, and a processor can time multiplex operations like adders, unlike
the hardware solution with multiple unused copies. The performance only needs to be
sufficient for protocol implementation, making the trade-off between fewer resources and
speed. To achieve this goal, a new processor called Baby8, designed for FPGA I/O, is being
developed using Yosys Synthesis software version 0.38 [1,2].
Baby8 is a von Neumann 8-bit CISC soft-core processor (already available in the authors’ GitHub repository in [3]) optimized for reduced FPGA resources, including program
size for 8-bit applications. Although the instruction set is not extensive, each instruction can
access an arbitrary memory location. Features like post-increment addressing, while not
faster than RISC (instructions use simple register-level [4]), enhance program compactness

Electronics 2024, 13, 781. https://doi.org/10.3390/electronics13040781

https://www.mdpi.com/journal/electronics

## PDF page 2

Electronics 2024, 13, 781

2 of 20

and may reduce the need for block RAMs. This paper presents a comparison of Baby8
with almost a dozen other soft-core processors, demonstrating competitive performance in
terms of implementation results, and comparisons with ASIC, NAND gates, and various
FPGA models.
1.1. ASICs
Application-specific integrated circuits are those designed to be used in one particular
product, as opposed to standard integrated circuits that are sold to many companies to
be used in many products. While the cost of each ASIC is normally a fraction of the cost
of an FPGA capable of handling the same design, the production of the ASIC has some
high NRE (non-recurring engineering) costs, so a reasonably high volume is needed for
the ASIC to be more viable economically than a FPGA. Additionally, ASICs may operate
at higher frequencies and lower power than FPGAs, impacting product considerations.
Comparing processor cores involves assessing area, operating frequency, and power usage
for a given fabrication technology.
1.2. NAND Gates
It is possible to build any digital circuit entirely with NAND logic gates or with just
NOR gates (the case for the AGC, the Apollo Guidance Computer, which landed on the
Moon). Before field-programmable gate arrays (FPGAs), many projects used gate arrays.
These were chips that had a large number of NAND gates, the same for all clients, and
the metal layer was specific to each client. Translating designs to NAND gates provides
insights into design complexity using the OnlyNANDYosysSynth complement script to
Yosys Synthesis software version 0.38.
1.3. FPGAs
Field-programmable gate arrays can implement any digital circuit up to a size that
depends on the particular FPGA device. Using hardware description languages like Verilog,
VHDL, Chisel, SpinalHDL, and others, a high-level processor description can be translated
into a netlist of basic blocks. The placement tool assigns blocks to specific locations, and
routing utilizes the FPGA’s configurable connection network. Routing uses the configurable
connection network in the FPGA (a little like early telephone exchange systems) to actually
connect the placed blocks. This is encoded into a “bit file” that is loaded by the FPGA each
time it is turned on to actually implement the circuit.
This comparison considers the usage of basic blocks (LUT, registers, DSP, distributed
memory, and block memory) in soft cores when translated with the open-source tool
Yosys002E. The basic blocks are:

•

•

•

•

LUT: LookUp tables implement all logic in FPGAs and can be categorized by the
number of address lines they require. A LUT4 has 16 words of a single bit each and
needs 4-bit addresses. A LUT6 has 64 bits and needs six address lines. A larger LUT
can always perform the job of a smaller one by either tying unused address lines to
zero or one or else duplicating the bits such that the output does not depend on that
address line. Combining smaller LUTs into a larger one is facilitated by special “mux”
blocks in some FPGAs (XC4000), enhancing their efficiency.
Registers: The LUTs are purely combinational, and an optional flip–flop circuit at
the output enables the implementation of sequential circuits. Normally, one register
is associated with one LUT, but there tend to be some extra registers as part of the
I/O pads.
DSP: Digital signal processing blocks are hardware implementations of multiplication
circuits. Otherwise, a very large number of LUTs would be required to implement this
operation, which has many more uses beyond digital signal processing.
Distributed memory: Each LUT is actually a very small random access memory (RAM),
generally unaltered after the initial FPGA configuration. An additional circuit allows
the use of all LUTs or a fraction as read/write memories.

## PDF page 3

Electronics 2024, 13, 781

3 of 20

•

Block memory: The area needed to store a bit in a register or even in a LUT is very
large compared to a dedicated RAM circuit. Since the 1990s, FPGAs have included
a number of memory blocks that can efficiently handle a medium to large number
of bits.

Other FPGA blocks include input and output buffers, clock buffers, and carry circuits
converting LUTs into adder circuits, along with multiplexers for combining small LUTs
and FPGA-specific circuits unique to each type.
FPGA Families
Xilinx 7: The 28 nm generation of Xilinx FPGAs remains popular, even after AMD’s
acquisition and the introduction of two subsequent generations. It is common for soft-core
processor implementation projects to make use of the FPGAs manufactured by Xilinx [5].
Cyclone V: The Cyclone family was the low end of Altera FPGAs, with the V generation
being the last before Intel’s acquisition of Altera. ICE40: The startup Silicon Blue took
advantage of the expiration of key FPGA patents to introduce their own very basic offering.
Their focus was on smaller FPGAs with low costs and low energy requirements. They were
bought by Lattice Semiconductor, and a second generation was designed, moving from the
original 65nm process to a more modern 40nm process, further reducing the energy use.
GoWin: This Chinese company achieved success with various FPGA variations globally,
introducing unique features like using spare LUTs to aid routing. How much this is used
varies from one project to the next, and this is why the numbers are not always relatively
the same compared to other types of FPGAs. ECP5: An evolution of the earlier ECP, ECP2,
and ECP3 FPGAs, the ECP5 family is a cost-effective mid-range option with high-speed
serial interfaces.
1.4. RISC-V Soft Cores
The rising popularity of RISC-V [6] in the industrial and academic space resulted in
a plethora of open-source RISC-V implementations [7,8]. The openness of the standard
does not guarantee the openness of specific cores, but those considered in this paper are
open. In addition, only cores implemented in Verilog or the subset of System Verilog
handled by Yosys were considered. RISC-V cores have a tremendous range in performance
and complexity [9], from tiny 32-bit microcontrollers to out-of-order 64-bit application
cores for data centers. Only the low end was studied here. darkRISC-V: The original
darkRISC-V was created by Samsoniuk in a single night of development to evaluate the
advantages and disadvantages of the RISC-V instruction set compared to others. It can be
optionally made smaller by reducing the number of registers as per RV32E. vexRISC-V: The
vexRISC-V in SpinalHDL is meant to show off the advantages of using that language, with
many configuration options where it is even easy to change the number of pipeline stages.
Many projects use the translated Verilog version of the processor, like the management
system in the repository for the GlobalFoundries 180 nm version of the Caravel “harness”
for open-source ASIC design. Glacial: Glacial trades off performance for size by being
an 8-bit processor that emulates a 32-bit RISC-V. One inspiration was the low end of the
original IBM S/360 family, which used microcode and an 8-bit datapath to implement the
architecture. PicoRV32: An early compact RISC-V core, the goal of the PicoRV32 was to fit
in the tiny ICE40 FPGAs first targeted by the ICE Storm open-source FPGA tool, of which
Yosys was a key component. SERV: SErial Risc V also trades off performance for size, in this
case by having a completely serial implementation. This means that any operation requires
32 clock cycles, as the operation handles only a single bit in each cycle. Serial computers
were a little more common in the days of vacuum tubes, when every single component
had a significant cost and added to the construction cost as well. They became far rarer in
the integrated circuit days, but they are one way to save FPGA resources best left for other
parts of a project.

## PDF page 4

Electronics 2024, 13, 781

4 of 20

1.5. Other Soft Cores
Even with all the variation possible with the RISC-V instruction set, there are applications where other designs are a better option. That is particularly true when executing
programs. Baby8: Designed to help interfaces adapt FPGA projects to specific boards, the
goal of Baby8 is to use as few FPGA resources as possible to leave more for the user’s actual
project (available in the authors’ GitHub repository in [3]). An 8-bit architecture is a good
match for the applications of interfacing to PS/2 or USB keyboards, mice, and game controllers, as well as providing an abstract interface to files on a FAT32-formatted SD memory
card. In a FPGA, distributed memory built from LUTs is denser than individual flip-flops.
Baby8 capitalizes on this density, albeit at the cost of reduced performance, by incorporating
the program counter into the register bank. In an ASIC, there is no advantage in doing this,
as the flip-flops would be the same either way. The nomenclature of the processor was
chosen in honor of the Manchester Baby, a 32-bit small-scale experimental machine and
the first electronic stored-program computer in 1948 [10]. A complete description of the
features and particularities of the Baby8 processor will be presented in the Materials and
Methods Section of this paper. 6502 and UKP: A NES (Famicom) emulator for the Sipeed
Tang Nano 20K FPGA board includes two processors. The 6502 is needed to run the actual
games, while the limited UKP handles USB mice, keyboards, or game controllers. Femto16:
In the 8-Bit Workshop online video game development system, there is an option to design
games at the hardware level using Verilog. The examples grow in complexity, introducing
two simple processors, the 8-bit Femto8 and the 16-bit Femto16. Games are then converted
from pure hardware to assembly programs for these processors. J0: Describing the J1 soft
core optimized for small programs in the Forth language was the inspiration for projects
like SwapForth by the same author and the Forth CPU computer system. The Gameduino
project adds FPGA-based video output for Arduino boards, incorporating the J0 processor
as a slight modification of the J1. MCPU: With only four instructions and addressing
only 64 bytes of memory (similar to Xilinx PicoBlaze), the MCPU is remarkably small yet
Turing complete. ZPU: The ‘ZPU Avalanche’ was designed to use the least FPGA possible
while being fully compatible with all the GNU programming tools, including GCC. The
concept revolves around treating C as more of a scripting language on an FPGA, with heavy
processing handled by hardware blocks. The Avalanche project translated the original
VHDL implementation to System Verilog. The System Verilog files were copied from the
original repository in the top directory.
2. Objectives
The main goal of our study is to design and evaluate a brand new soft-core processor
optimized for reduced FPGA resources, including program size for 8-bit applications.
3. Materials and Methods
3.1. Processor Specifications
3.1.1. State Registers
The processor features 16 internal 8-bit state registers, as shown in Figure 1. While not
accessible to programmers, exceptions include the registers W, X, and Y and the external
memory, which can be directly read and written by the user program. Flags Z (zero),
N (negative), C (carry), and V (overflow) do not persist between instructions but can be
saved with TEST instructions.
The complete list of 8-bit state registers is provided in the following, where H denotes
a high byte and L denotes a low byte in the case of 16-bit addressing:

•
•
•
•
•

PH/PL: 16-bit (8H/8L) program counter in normal execution mode;
MH/ML: 16-bit (8H/8L) pointer for indirect “zero page” operands;
IH/IL: 16-bit (8H/8L) program counter in interrupt mode;
LH/LL: 16-bit (8H/8L) address saved in the last call instruction;
ZH/ZL: 16-bit (8H/8L) address of the “zero page” operand;

## PDF page 5

Electronics 2024, 13, 781

5 of 20

•

TH/TL: 16-bit (8H/8L) timer to define the number of cycles to pause before the
next instruction;
Electronics 2024, 13, x FOR PEER REVIEW
5 of 23
•
K: 8-bit single register for ’cascades’—values between pairs of instructions;
•
W, X, and Y: 8-bit single registers accessible to the programmers for reading and writing.

Figure
The
Baby8
processor’s
8‐bit
state
registers.
High‐
and
low‐forming
16‐bit
addresses.
Figure
1. 1.
The
Baby8
processor’s
8-bit
state
registers.
Highand
low-forming
16-bit
addresses.

3.1.2. Basic
The Syntax
complete list of 8‐bit state registers is provided in the following, where H de‐
notes
a
high
byte and
denotes awith
low byte
in the case architecture,
of 16‐bit addressing:
The processor
wasLdesigned
a two-address
where one address
indicates
both the
destination
one counter
operand,inand
the second
address
specifies the other

PH/PL:
16‐bit
(8H/8L) and
program
normal
execution
mode;
operand.
The
assembly
language
syntax
is
C-like,
with
an
addition
represented
as:

MH/ML: 16‐bit (8H/8L) pointer for indirect “zero page” operands;

IH/IL: 16‐bit (8H/8L) program counter in interrupt mode;
rD +=
rS last call instruction;

LH/LL: 16‐bit (8H/8L) address saved
in the

ZH/ZL: 16‐bit (8H/8L) address of the “zero page” operand;
3.1.3. K-Cascades

TH/TL: 16‐bit (8H/8L) timer to define the number of cycles to pause before the next
The
“cascade” feature changes the destination to be the first operand of the followinstruction;
ing
instruction.
A sequence
is incremented by between
‘the value
pointed
to by location 20’

K: 8‐bit single
register that
for ’cascades’—values
pairs
of instructions;
looks like:

W, X, and Y: 8‐bit single registers accessible to the programmers for reading and
X += *20
writing.

3.1.2. Basic Syntax
The processor was designed with a two‐address architecture, where one address
indicates both the destination and one operand, and the second address specifies the
other operand. The assembly language syntax is C‐like, with an addition represented as:

## PDF page 6

Electronics 2024, 13, 781

6 of 20

W&=X
It can be implemented with the cascade as:
K = X + *20
Y=W&K
Unlike the original code fragment, these two instructions do not erase the value in X.
While the architecture is generally two-address, it can function as three addresses (actually
four) when needed. The use of “K” in the instruction distinguishes it from a move with
some complicated expression to be calculated at assembly time.
3.1.4. Source and Destination
Table 1 shows the source and destination directives in the processor architecture. In
theory, the zero page allows access to bytes 0 to 127 of the 256-byte page selected by register
ZH. In practice, addresses 12 to 15 access the four input and four output ports. More I/O
ports can be memory-mapped to other addresses if needed.
Table 1. Source and destination directives in Baby8 architecture.
Source and Destination
Syntax

Cycle 1,2

Range

zpa
zpa
zpa
*zpa
*zpa++

ZL = *(PH,PL)++

0 ≥ ZL ≥ 11
12 ≥ ZL ≥ 15
16 ≥ ZL ≥ 127
128 ≥ ZL ≥ 254
129 ≥ ZL ≥ 255

Cycle 3,4,5

M = *(ZH,ZL)
M = *(ZH,ZL)

Cycle 6. . .

Access

*(Z) = M + 1

register
I/O port
*(ZH,ZL)
*(MH,ML)
*(MH,ML)

Zero page addresses 0 to 11 access the internal registers W to IH, allowing LL and LH
to be saved and restored if more than one level of subroutines is needed. Since ZH can
also be changed, the “zero page” can be relocated to any memory location, similar to the
6809 and 65,816 processors. When TL is changed, the timer is started if TL and TH are not
both zero, and it is stopped if they are zero.
The two-bit ss and dd fields (see Table 2) in the instruction use values 0, 1, and 2 to
encode the registers W, X, and Y, respectively. A value of 3 indicates that a byte follows,
encoding the actual address.
Table 2. Regular and K-cascade basic instructions in Baby8.
Basic Instructions
Opcode

Binary

Syntax

K-Binary

K-Syntax

add

0000 ssdd

D += S

0001 ssdd

K=D+S

subtract

0010 ssdd

D −= S

0011 ssdd

K=D−S

move

0100 ssdd

D=S

0101 ssdd

K=D=S

test

0110 cccc

cond ?

0111 cccc

K = cond

and

1000 ssdd

D &= S

1001 ssdd

K=D&S

or

1010 ssdd

D |= S

1011 ssdd

K=D|S

exclusive or

1100 ssdd

D ˆ= S

1101 ssdd

K=DˆS

See next table

1111 ffdd

When both ss and dd are 3, the first extra byte is for the source, and the second is for
the other source/destination. In the case of immediate instructions, the immediate value is
the first extra byte, followed by the destination.

## PDF page 7

Electronics 2024, 13, 781

7 of 20

Next, Tables 2–5 will be presented, describing, respectively:

•
•
•
•

The basic operations opcodes;
The immediate instructions opcodes;
The control flow instructions opcodes;
The conditional tests.

Table 3. Immediate instructions in Baby8.
Immediate Instructions
Opcode

Binary

Syntax

add

1110 00dd

D += #

subtract

1110 01dd

D −= #

move

1110 10dd

D=#

See next table

1110 11ff

and

1111 00dd

D &= #

or

1111 01dd

D |= #

exclusive or

1111 10dd

D ˆ= #

See next table

1111 11ff
Table 4. Control flow instructions in Baby8.

Control Flow Instructions
Opcode

Binary

Syntax

Internal Operation

jump

1110 1100

>>>> expr

PH,PL := ##

call

1110 1101

>>>>$ expr

LH,LL := PH,PL;PH,PL := ##

nop

1110 1110

~

return

1110 1111

<<<<

PH,PL := LH,LL

jump

1111 1100

>>>> *zpa

PH,PL := *zpa

call

1111 1101

>>>>$ *zpa

LH,LL := PH,PL;PH,PL := *zpa

branch

1111 1110

>>>> #expr

PH,PL += #

table

1111 1111

<<<< zpa

PH,PL := [LH,LL + zpa]

Table 5. Conditional tests in Baby8.
Conditional
Tests
Conditional

Name

Code

Syntax

Alternative
Syntax

Code

Syntax

Alternative
Syntax

Z

Equal

011k 0000

==

Z

011k 0001

!=

!Z

C

Greater equal

011k 0010

>=

C

011k 0011

<

!C

N

Negative

011k 0100

<0

N

011k 0101

>=0

!N

V

Overflow

011k 0110

V

011k 0111

C & !Z

Greater

011k 1000

>

011k 1001

<=

N==V

Signed greater equal

011k 1010

$>=

011k 1011

$<

!Z & N==V

Signed greater

011k 1100

$>

011k 1101

$<=

1

TRUE

011k 1110

true

011k 1111

false

!V

## PDF page 8

greater
greater equal
equal
Signed
Signed
!Z
!Z &
& N==V
N==V
greater
greater
1
Electronics 2024, 13, 781 TRUE
1
TRUE

011k
011k 1100
1100

$>
$>

011k
011k 1101
1101

$<=
$<=

011k
011k 1110
1110

true
true

011k
011k 1111
1111

false
false

8 of 20

3.1.5. Shifts and Rotations
3.1.5.
3.1.5. Shifts
Shifts and
and Rotations
Rotations
The missing multiplication and division instructions are to be expected for a very
The
missing
multiplication
and division
are
to
be
for a
very
missing
multiplication
divisionasinstructions
instructions
are if
to needed),
be expected
expected
veryof
small The
processor
(though
they canand
be added
an I/O device
but for
thealack
small
processor
(though
they
can
be
added
as
an
I/O
device
if
needed),
but
the
lack
of
small
processor
(though
they
can
be
added
as
an
I/O
device
if
needed),
but
the
lack
shift and rotate instructions might seem limiting. Adding a value to itself is equivalentofto
shift
and
rotate
instructions
might
seem
limiting.
Adding
a
value
to
itself
is
equivalent
to
andshift
rotate
might
seem indicating
limiting. Adding
a value bit.
to itself
is equivalent
to
a shift
one-bit
toinstructions
the left, with
the carry
the removed
Shifting
to the right
a
one‐bit
shift
to
the
left,
with
the
carry
indicating
the
removed
bit.
Shifting
to
the
right
a
one‐bit
shift
to
the
left,
with
the
carry
indicating
the
removed
bit.
Shifting
to
the
right
(logical or arithmetic) an 8-bit value by N bits can be achieved by extending (zero or sign)
(logical or
arithmetic)
an
8‐bit
value by
bits
can
be
by extending
(zero
or
arithmetic)
anthe
8‐bit
by N
N
bits
canusing
be achieved
achieved
extending
(zero(Listing
or sign)
sign)1).
to(logical
16-bits,orshifting
that to
leftvalue
by 8-N
bits,
and
the top by
byte
as the result
to
16‐bits,
shifting
that
to
the
left
by
8‐N
bits,
and
using
the
top
byte
as
the
result
(Listing
to
16‐bits,
shifting
that
to
the
left
by
8‐N
bits,
and
using
the
top
byte
as
the
result
(Listing
Sending a byte with the least significant bit first might seem to require 7 such steps per bit,
1).
Sending
a byte
the
least
bit
might
to require
7 such
steps
per
1). the
Sending
byte with
with
theachieved
least significant
significant
bit first
first
might seem
seem
suchper
steps
perto
but
samearesult
can be
by shifting
a one-bit
maskto
torequire
the left7once
step
bit,
but
the
same
result
can
be
achieved
by
shifting
a
one‐bit
mask
to
the
left
once
per
step
bit,
but
the
same
result
can
be
achieved
by
shifting
a
one‐bit
mask
to
the
left
once
per
step
check each bit from least to most significant (Listing 2).
to
to check
check each
each bit
bit from
from least
least to
to most
most significant
significant (Listing
(Listing 2).
2).
Listing 1. Shifts and rotations syntax example in Baby8.
Listing
Listing 1.
1. Shifts
Shifts and
and rotations
rotations syntax
syntax example
example in
in Baby8.
Baby8.
11 ;code
;code to
to shift
shift X
X right
right by
by 5
5 bits
bits arithmetically
arithmetically
22 W
W == #0
#0 ;; default
default sign
sign
33 K
K == X
X&
& #128
#128
44 C
C ??
55
W
W == #255
#255 ;; extended
extended sign
sign for
for V
V
66 W
+=
W
;
shift
left
top
half
W += W ; shift left top half
77 X
X +=
+= X
X ;; shift
shift left
left bottom
bottom half
half
88 C
?
C?
99
W
W +=
+= #1
#1 ;; move
move carry
carry to
to bottom
bottom bit
bit
10
W
+=
W
10 W += W
11
11 X
X +=
+= X
X
12
C
12 C ?
?
13
W
13
W +=
+= #1
#1 ;; second
second bit
bit
14
W
+=
W
14 W += W
15
15 X
X +=
+= X
X
16
16 C
C ??
17
W
17
W +=
+= #1
#1 ;; third
third bit.
bit. Now
Now W
W is
is X
X $>>
$>> 5
5
Listing
Shifts
and
rotations
syntax
example
Listing
Listing2.2.
2.Shifts
Shiftsand
androtations
rotationssyntax
syntax example
example in Baby8.
W
W == #1
#1 ;; bit
bit mask,
mask, start
start at
at least
least significant
significant
SendBit:
SendBit:
20
K
20
K == X
X&
&W
W
21
C
21
C ??
22
>>>>
22
>>>> sendOne
sendOne
23
23 SendZero:
SendZero:
24
.. .. ..
24
25
W
25
W +=
+= W
W
26
C
26
C ??
27
>>>>
27
>>>> sendBit
sendBit
18
18
19
19

3.1.6. Interrupt
3.1.6.
Interrupt
3.1.6.
Interrupt
The
interrupt mode uses IH/IL for instruction fetches instead of PH,PL (bit 2 of
The
mode
uses
IH/IL
instruction
fetches
instead
of
PH,PL
(bit
of
The interrupt
interrupt
mode
uses
IH/IL
for
instruction
fetches
instead
of 255
PH,PL
(bit 2
2of
of the
the
the register
addresses
is 1),
and
zerofor
page
addresses
go from
144 to
instead
from
register
addresses
1),
from
to
instead
of
16
register
addresses
is
1), and
andiszero
zero
page
addresses
go
from
144
to 255
255on the
instead
of from
from
16 to
to
16 to
127 (bit 7
of is
addresses
set).page
The addresses
interrupt go
mode
is 144
entered
next
instruction
127
(bit
7
of
addresses
is
set).
The
interrupt
mode
is
entered
on
the
next
instruction
fetch
127
(bit
7
of
addresses
is
set).
The
interrupt
mode
is
entered
on
the
next
instruction
fetch
fetch after the interrupt line goes high, unless the previous instruction was a cascade or the
after
interrupt
goes
the
previous
instruction
was
aa the
cascade
the
after
he
interruptisline
line
goes high,
high,
unless
theThe
previous
instruction
wason
cascade
or
the
currentthe
instruction
supposed
to
beunless
skipped.
interrupt
mode ends
next or
instruction fetch after the interrupt line goes low, with the same restrictions as described before.
Most processors have interrupt handlers that start at fixed addresses or, more often, as
indicated in some tables. In Baby8, the address in IH/IL is simply the instruction following
the one that caused the interrupt line to go low at the end of the previous interrupt. This is
more like a coroutine scheme where an explicit “yield” instruction is executed. With careful
programming, it is possible to speed up response time by having the processor ready to
execute in different places for different situations. Any registers used by the interrupt

## PDF page 9

Electronics 2024, 13, 781

9 of 20

Electronics 2024, 13, x FOR PEER REVIEW
Electronics 2024, 13, x FOR PEER REVIEW

10 of 23
10 of 23

handler should be saved and then restored right before the yield. Having the use of the
second half of the zero page makes this easier. Note that the first half can still be accessed
with
3.1.7.indirect
Timer addressing.
3.1.7. Timer
3.1.7. Every
Timer instruction is executed in a known number of clock cycles, but to make precise
Every instruction is executed in a known number of clock cycles, but to make precise
delays even easier, TH/TL implements a 16‐bit timer. The timer mode is entered on the
Every
instruction
is executed
in a known
number
clock
cycles,
butistoentered
make precise
delays
even
easier, TH/TL
implements
a 16‐bit
timer.ofThe
timer
mode
on the
next instruction fetch after a write to TL, which results in TH or TL having a non‐zero
delays even
easier,
TH/TL
implements
a 16-bit
timer.
The
timerormode
is
entered
on
the
next
instruction
fetch
after
a
write
to
TL,
which
results
in
TH
TL
having
a
non‐zero
value.
The restrictions
are the
same
as entering
or leaving
mode.
next
instruction
fetch after
write
to as
TL,
which
results
in
THinterrupt
or
TL having
a non-zero value.
value. The
restrictions
areathe
same
entering or
leaving
interrupt
mode.
Instead ofare
fetching
instructions,
the
processor
simply decrements TL by one on
The restrictions
the same
as enteringthe
or leaving
interrupt
Instead
of fetching
instructions,
processor
simplymode.
decrements
TL
by one
every
clock
cycle.
When
TH/TL
reaches
zero,
the
instruction
fetch
resumes.
If TH
isevery
noton0
Instead
of fetching
the processor
simply decrements
TL by one
onis
every
clock cycle.
Wheninstructions,
TH/TL reaches
zero, the instruction
fetch resumes.
If TH
not 0
but TL
is, then
TL
is decremented
by twoinstruction
(going to 254), resumes.
and on the
next
cycle,
TH is
clock
cycle.
WhenTL
TH/TL
reaches zero,
If TH
is not
0 but
but TL
is, then
is decremented
by the
two (going to fetch
254), and on the
next
cycle,
THTL
is
decremented.
If
an
interrupt
arrives
while
in
timer
mode,
the
interrupt
is
handled,
and
is,
then TL is decremented
by two
(going
to 254),
and on
the next
cycle, TH is
is decremented.
decremented.
If
an
interrupt
arrives
while
in
timer
mode,
the
interrupt
handled,
and
execution
is normal
until
the interrupt
ends. Theinterrupt
interrupt handler
may
reset
TH/TL or
Ifexecution
an
interrupt
arrives
while
timer mode,
handled,
and
execution
is normal
until
thein
interrupt
ends. the
The interruptishandler
may
reset
TH/TL is
or
decrease
their
values
if
encountering
a
longer
delay
than
expected
in
the
user
code
is an
normal
until
thevalues
interrupt
ends. The interrupt
mayexpected
reset TH/TL
oruser
decrease
decrease
their
if encountering
a longerhandler
delay than
in the
code their
is an
issue.
values
issue. if encountering a longer delay than expected in the user code is an issue.

3.2.Custom
CustomProcessor
ProcessorDesign
Design
3.2.
3.2. Custom Processor Design
An advanced
advanced digital
digital design
design and
and simulation
simulation tool
tool named
named DIGITAL,
DIGITAL, developed
developed by
by
An
An advanced
digital
and process.
simulation
named
DIGITAL,
developed
by
Neemann,
employed
fordesign
thedesign
design
Thetool
Baby8
processor
andits
its
peripherals
Neemann,
isis employed
for
the
process. The
Baby8
processor
and
peripherals
Neemann,
is employed
for the design
process.
Baby8
processor
and
its peripherals
(RAM
shown in
in Figure
FigureThe
whileitsits
internalblocks
blocks
aregiven
given
(RAM block
block and
and terminal) are shown
2,2,while
internal
are
in
(RAM
block
and
terminal)
are
shown
in
Figure
2,
while
its
internal
blocks
are
given
in
in
Figure
Figure
3. 3.
Figure 3.

Figure 2. The Baby8 CPU and its peripheral RAM block and terminal.
Figure
Figure2.2. The
TheBaby8
Baby8CPU
CPUand
andits
itsperipheral
peripheralRAM
RAMblock
blockand
andterminal.
terminal.

Figure 3. The combination of the DATAPATH with the CONTROL UNIT forms the CPU.
Figure3.3. The
Thecombination
combinationof
ofthe
theDATAPATH
DATAPATHwith
withthe
theCONTROL
CONTROLUNIT
UNITforms
formsthe
theCPU.
CPU.
Figure

3.2.1. DATAPATH
3.2.1. DATAPATH

## PDF page 10

Electronics 2024, 13, 781

10 of 20
11 of 23

Electronics 2024, 13, x FOR PEER REVIEW

3.2.1. DATAPATH
The
Theheart
heartofofthe
theDATAPATH
DATAPATHisisthe
theALU
ALU(arithmetic
(arithmeticlogic
logicunit).
unit).ItItcan
canperform
performaa
logical
OR,
XOR,
or or
NOT)
between
8-bit
inputs
A A
andand
B, or
modify
input
logicaloperation
operation(AND,
(AND,
OR,
XOR,
NOT)
between
8‐bit
inputs
B, or
modify
in‐
A.
Figure 4
provides
an an
in-depth
view
of of
thethe
DATAPATH
architecture
and
put A.
Figure 4
provides
in‐depth
view
DATAPATH
architecture
anditsitsinternal
internal
components,
components,including
includingthe
theALU,
ALU,register
registerbank,
bank,multiplexers,
multiplexers,address
addressmodifier
modifier(address
(address
modification),
modification),and
anddata
dataoutput
outputregister.
register.

Figure4.4.The
TheDATAPATH
DATAPATHdefines
definesthe
thelogic
logictotoexecute
executethe
theinstructions.
instructions.
Figure

Duringthe
thenative
nativedata
dataflow,
flow,operand
operandBBofofthe
theALU
ALUtypically
typicallyoriginates
originatesfrom
fromthe
the
During
outputDb
Dbofofthe
theregister
registerbank.
bank.However,
However,ititmay
mayeventually
eventuallycome
comefrom
frommemory
memoryororfrom
from
output
oneofofthe
theprocessor’s
processor’stwo
twoinput
inputports.
ports.InInturn,
turn,the
theDa
Daand
andDb
Dboutputs
outputsofofthe
theregister
registerbank
bank
one
togetherform
formaa16-bit
16‐bitaddress.
address.Within
Withinthe
theregion
regionofofcombinational
combinationallogic
logiccircuits
circuitscalled
called
together
addressmodification,
modification,the
thebinary
binaryvalues
valuesofofthe
theaddresses
addressesare
areprocessed.
processed.Bit
Bit77indicates
indicates
address
whetherthe
theaddress
addressisisdirect
directororindirect,
indirect,while
whilebit
bit0 0signifies
signifieswhether
whetherititshould
shouldbe
beused
usedoror
whether
notincremented.
incremented.
not
The
Theaddress
addressfrom
frommemory
memoryisisnot
notalways
alwaysdesired,
desired,and
andititcan
canbe
becreated
createdfrom
frominternal
internal
operands
Logical
address
modification
circuits
also also
serve this
operandsand/or
and/orALU
ALUoperations.
operations.
Logical
address
modification
circuits
servepurthis
pose.
The first
memory
addresses
are are
allocated
for normal
programs,
and theand
range
purpose.
The 127
first 127
memory
addresses
allocated
for normal
programs,
the
between 128
and 128
255 is
utilized
routines
interrupts.
Additionally, a data
outputa regrange
between
and
255 isby
utilized
bycalled
routines
called interrupts.
Additionally,
data
ister
is necessary
to external
memory,
requiring
24 bitsrequiring
for this operation—16
address
output
register to
is write
necessary
to write
to external
memory,
24 bits for this
opera‐
bits
and
another
8
data
bits,
concatenated
at
the
clock
edge,
using
2
clock
cycles
this2
tion—16 address bits and another 8 data bits, concatenated at the clock edge, for
using
operation.
Although
operationAlthough
slightly this
reduces
performance,
it enables
utilization ofit
clock
cycles
for thisthis
operation.
operation
slightly
reducesthe
performance,
fewer
FPGA
resources,
the primary
objective.
enables
thehardware
utilization of
feweraligning
FPGA with
hardware
resources,
aligning with the primary
objective.
3.2.2. CONTROL UNIT
The
core of the
Baby8 processor control unit is the state machine defined by the
3.2.2.
CONTROL
UNIT
ROMfsm
block
in
Figure
5. Internally,
it implements
internal
generating
The core of the Baby8
processor
control unit the
is the
stateROM
machine
definedcontrol
by the
signals for decoding (microcode), as specified in Figure 6 and Table 6. This connected finite
ROMfsm block in Figure 5. Internally, it implements the internal ROM generating control
state machine generates signals needed to use the data path to execute instructions.
signals for decoding (microcode), as specified in Figure 6 and Table 6. This connected fi‐
nite state
machine
signalssignals
needed
use theOPCODES.
data path to execute instructions.
Table
6. Internal
ROMgenerates
generates control
byto
decoding
Address (8-Bits)

Control (32-Bits)

Address (8-Bits)

Control (32-Bits)

0x00
0x01
0x02
0x03
0x04
0x05
0x06
0x07

0xE3308801
0xF3308801
0x43308801
0x53308800
0x0
0x0
0x0
0x0

0x40
0x41
0x42
0x43
0x44
0x45
0x46
0x47

0x30380803
#N/DISP
0x303A6812
0xFF30180A
0xFF30180A
0x303A6811
#N/DISP
0x3CD00200

## PDF page 11

Electronics 2024, 13, 781

11 of 20

Table 6. Cont.
Address (8-Bits)

Control (32-Bits)

Address (8-Bits)

Control (32-Bits)

0x08
0x09
0x0A
0x0B
0x0C
0x0D
0x0E
0x0F
0x10
0x11
0x12
0x13
0x14
0x15
0x16
0x17
0x18
0x19
0x1A
0x1B
0x1C
0x1D
0x1E
0x1F
0x20
0x21
0x22
0x23
0x24
0x25
0x26
0x27
0x28
0x29
0x2A
0x2B
0x2C
0x2D
0x2E
0x2F
0x30
0x31
0x32
0x33
0x34
0x35
0x36
0x37
0x38
0x39
0x3A
0x3B
0x3C
0x3D
0x3E
0x3F

0x44311800
0x55311801
0x44310800
0x0
0xEEF01C05
0xFF30190F
0x3330010F
0x0
0xEEF01C05
0xFF30180E
0x3330000E
0xEE301805
0xFF301801
0xEE301800
0xFF301800
0x0
0x3330B800
0x0
0x21026810
0x0
0x8E300801
0x9F300801
0xEEF01C05
0xC3340802
0xC3340802
0xFF301801
0x3EF00401
0xF3340801
0xEC300800
0x0
0xE8300801
0xF9300800
0x0
0xEEF01C05
0x13166812
0x13166810
0xFF301800
0x0
0x0
0x0
0x0
0x0
0x0
0x0
0x0
0x0
0x0
0x0
0x0
0x0
0x0
0x0
0x0
0x0
#N/DISP
#N/DISP

0x48
0x49
0x4A
0x4B
0x4C
0x4D
0x4E
0x4F
0x50
0x51
0x52
0x53
0x54
0x55
0x56
0x57
0x58
0x59
0x5A
0x5B
0x5C
0x5D
0x5E
0x5F
0x60
0x61
0x62
0x63
0x64
0x65
0x66
0x67
0x68
0x69
0x6A
0x6B
0x6C
0x6D
0x6E
0x6F
0x70
0x71
0x72
0x73
0x74
0x75
0x76
0x77
0x78
0x79
0x7A
0x7B
0x7C
0x7D
0x7E
0x7F

0x3300800
0x3300000
0
0x8E300801
0x9F300809
0xEC300801
0xFD300800
0x0
0xC0880805
0xD9301802
0xD9300801
0xCCD01C05
0xE3340802
0xE3340802
0x3CD00402
0xDD301802
0xF3340800
0x3CD00401
0xF3340800
0x0
0x201A6810
0x0
#N/DISP
0x3CD00200
0x3300800
0x3300000
#N/DISP
0x0
0x30380809
#N/DISP
0x3CD00200
0x3300800
0x3300000
0x0
0x0
0x0
0x0
0x0
0x0
0x0
0xEEF01C05
0x63340802
#N/DISP
#N/DISP
0x36700408
0x367004C1
0xC3340801
0x367004E1
#N/DISP
0x3C301005
0x367002C2
0x367002C3
0x3D301001
0x367002E1
0x3CD00408
0x0

## PDF page 12

Electronics
Electronics2024,
2024,13,
13,781
x FOR PEER REVIEW
Electronics 2024, 13, x FOR PEER REVIEW

of2023
12 of
12 of 23

Figure5.5.AAdecodification
decodification combinatorialcircuit
circuit insideaaCONTROL
CONTROL unit.
Figure
Figure 5. A decodificationcombinatorial
combinatorial circuitinside
inside a CONTROLunit.
unit.

Figure 6. Internal details of the ROMfsm block, containing the uPC microprogram counter register
Figure
Figure6.6.Internal
Internaldetails
detailsofofthe
theROMfsm
ROMfsmblock,
block,containing
containingthe
theuPC
uPCmicroprogram
microprogramcounter
counterregister
register
and the microcode ROM, whose contents are described in Table 6.
andthe
themicrocode
microcodeROM,
ROM,whose
whosecontents
contentsare
aredescribed
describedininTable
Table6.6.
and
TableALU
6. Internal ROM generates control signals by decoding OPCODES.
3.2.3.
Table 6. Internal ROM generates control signals by decoding OPCODES.

In the design of the ALU, several factors were meticulously considered to achieve a
Address (8‐bits)
Control (32‐bits)
Address (8‐bits)
Control (32‐bits)
Address
(8‐bits)performance
Control and
(32‐bits)
(8‐bits)
Control
(32‐bits)
balance
between
resourceAddress
efficiency.
The initial step
involved
defining
the logical
and arithmetic0xE3308801
operations necessary for0x40
the application. Another
critical aspect
0x00
0x30380803
0x40
0x30380803
focused0x00
on the format of 0xE3308801
the operands to be manipulated.
Ultimately,
priority was
given to minimizing the
area and optimizing
the layout, with
0x01
0xF3308801
0x41
#N/DISP
0x01 of the FPGA
0xF3308801
0x41
#N/DISP
the reduction
circuit area established
as a primary project
objective. This
approach,
tailored for FPGA
implementation rather
decisions
0x02
0x43308801
0x42than TTL, led to specific
0x303A6812
0x02
0x43308801
0x42
0x303A6812
contributing to circuit reduction in this particular context. Choosing multiplexers at the
0x53308800
input of0x03
the adders instead of
at the output was0x43
one such decision. 0xFF30180A
Motivated by the
0x03
0x53308800
0x43
0xFF30180A
presence of a 6-input lookup table on the FPGA, this choice makes the circuit more compact
0x0
0x44
0xFF30180A
for this 0x04
specific case.
0x04
0x0
0x44
0xFF30180A
The ALU, showcased in Figure 7, was designed around an 8-bit adder, receiving two
0x05
0x303A6811
8-bit data
and a Cin (carry in)0x0
bit. This setup results0x45
in a 9-bit output, where
8 bits represent
0x05
0x0
0x45
0x303A6811
the operation result and 1 bit is the C (carry out).
0x06
0x0
0x46
#N/DISP
The0x06
operations performed
determined by two multiplexers.
0x0by the adder are 0x46
#N/DISP The first
multiplexer, in short, defines the arithmetic operations. Using the aSel selector, it is possible
0x07
0x0
0x47
0x3CD00200
0x07
0x3CD00200
to choose
the operand A, the 0x0
inverse of A, 0, or -2. 0x47
The0x08
second multiplexer
is mainly responsible0x48
for logical operations.
Using the logSel
0x44311800
0x3300800
0x44311800
0x48
selector,0x08
it is possible to choose
between A and B, A
or B, A or B, or just 0x3300800
B.

0x09
0x09

0x55311801
0x55311801

0x49
0x49

0x3300000
0x3300000

## PDF page 13

the input of the adders instead of at the output was one such decision. Motivated by the
presence of a 6‐input lookup table on the FPGA, this choice makes the circuit more
compact for this specific case.
The ALU, showcased in Figure 7, was designed around an 8‐bit adder, receiving two
of 20
8‐bit data and a Cin (carry in) bit. This setup results in a 9‐bit output, where 8 bits13repre‐
sent the operation result and 1 bit is the C (carry out).

Electronics 2024, 13, 781

Figure7.7.The
TheALU
ALUcombines
combinestwo
twooperands
operands
and
diﬀerent
ways
according
to the
instruc‐
Figure
(A(A
and
B)B)
in in
different
ways
according
to the
instructions.
tions.

In this way, with this simple circuit, we can perform all the necessary operations in
The To
operations
performed by
the we
adder
are bit 0
determined
two
multiplexers.
The
our ALU.
perform a logical
operation,
insert
into theby
first
multiplexer,
which
firstbe added
multiplexer,
in logic
short,defined
definesby
thethe
arithmetic
operations. Using
selector,
it is
will
to the
second multiplexer:
AND, the
OR,aSel
or XOR.
In this
possible
to
choose
the
operand
A,
the
inverse
of
A,
0,
or
‐2.
way, it is as if the adder were removed and the result of the logical operation was passed
The
multiplexer is mainly responsible for logical operations. Using the logSel
directly
to second
the output.
selector,
is perform
possible to
choose between
A and
A or
or B, or just
B. to send the
Now,itto
arithmetic
operations,
weB,set
theB, A
second
multiplexer
In B
this
way, to
withthe
this
simple
circuit,
perform all
necessarythe
operations
in
operand
directly
adder,
while
the we
firstcan
multiplexer
canthe
determine
operation.
our
perform
a logical
operation,
insert bit
0 into
the first
multiplexer,
which
WhenALU.
we To
pass A
directly,
we perform
an we
addition;
when
passing
the inverse
of A,
we
will
be added
to the but
logictodefined
bythis
the second
multiplexer:
AND,
OR,
orwe
XOR.
In the
this
perform
subtraction,
conduct
operation, we
send 1 in
Cin so
that
have
way, it is as
if the adder were removed and the result of the logical operation was passed
two’s
complement.
directly to the output.
4. Results
Now, to perform arithmetic operations, we set the second multiplexer to send the
All the
presented
in Tables
and 8
were
evaluatedcan
using
both scripts
data
operand
B results
directly to
the adder,
while7 the
first
multiplexer
determine
the and
operation.
availablewe
bypass
the A
authors
in their
repository.
Thewhen
results are
divided
twof A,
tables,
When
directly,
we Github
perform an
addition;
passing
the into
inverse
we
divided
RISC-V™ and
non-RISC-V™
compatibility.
performinto
a subtraction,
but to conduct
this operation,
we send 1 in Cin so that we have the
two’s complement.
Table 7. The ASIC and FPGA resources used by the RISC-V processors related to Baby8.

4. Results
Device

Measured
Item

Dark
Vex
Pico
Baby8
Glacial
All the results
presented inRISC-V
Tables 7 and 8
were evaluated
using both SERV
scripts and
RISC-V
RV32

ASIC
(130 nm)

Max.Clock
(MHz)
Power
(mW)
Efficiency
(MHz/mW)
DIE area
CORE area
(µm2 )

ASIC/
FPGA

NAND
Gates

FPGAs
Xilinx
7

LUTs
Registers
D. Memory
B. Memory
DSPs

31
8
4
-

1018
184
12
-

1233
914
3
-

142
84
-

1072
573
12
-

212
182
-

FPGAs
Cyclone
V

LUTs
Registers
D. Memory
B. Memory
DSPs

29
8
16
-

920
196
64
-

1184
944
28
3
-

146
84
-

907
609
2
-

197
182
-

data available by the authors in their Github repository. The results are divided into two
57.69
41.39
61.33
102.33
59.88
116.29
tables, divided into RISC‐V™ and non‐RISC‐V™ compatibility.
We show the main
as ASICs,
1.99
5.46 results classified
30.04
1.52 NAND gates,
14.25 and FPGAs.
2.38For the
ASICs, we inform the maximum clock frequency, the power consumption, the eﬃciency,
and the
and DIE (DIE is
a small block
of semiconducting
28.99eﬀective area
7.58of the CORE2.04
76.32
4.20
48.86 ma‐
terial on which a given functional circuit is fabricated).
26,106
147,331
375,121 the plain
18,815
28,436
For the NAND
gates, we provide
number of259,337
gates used. And
for the
20,888
134,792
354,847
14,423
242,546
22,778
FPGAs, we inform the number of LUTs, registers, distributed memories, block memo‐
ries, and DSP units used for each family of FPGA (Xilinx 7, Cyclone V, ICE 40, Gowin,
and 3020
ECP 5).
18,076
49,206
2063
34,508
3245

## PDF page 14

Electronics 2024, 13, 781

14 of 20

Table 7. Cont.
Device

Measured
Item

Baby8

Dark
RISC-V

Vex
RISC-V

Glacial

Pico
RV32

SERV

FPGAs
ICE40

LUTs
Registers
D. Memory
B. Memory
DSPs

285
136
-

1414
210
4
-

1697
1112
8
-

232
84
-

1648
597
4
-

259
182
-

FPGAs
GoWin

LUTs
Registers
D. Memory
B. Memory
DSPs

48
8
4
-

1750
184
16
-

2010
1112
4
-

280
84
-

1299
574
32
-

343
182
-

FPGAs
ECP5

LUTs
Registers
D. Memory
B. Memory
DSPs

77
8
4
-

1378
184
16
-

1774
1112
4
-

267
84
-

1233
574
32
-

287
182
-

Table 8. The ASIC and FPGA resources used by the non-RISC-V processors related to Baby8.
Device

Measured
Item

ASIC
(130 nm)

Max.Clock
(MHz)
Power
(mW)
Efficiency
(MHz/mW)
DIE area
CORE area
(µm2 )

Baby8

6502

Femto
16

J0

MCPU

UKP

ZPU

57.69

58.87

65.10

55.68

102.91

135.05

63.94

1.99

1.47

1.23

5.06

0.31

4.42

14.55

28.99

40.04

52.92

11.00

331.96

30.55

4.39

26,106
20,888

43,788
36,697

61,532
53,495

166,680
153,327

4799
2733

34,026
27,858

70,809
61,171

ASIC/FPGA

NAND
Gates

3020

4890

6976

21,003

424

3909

8025

FPGAs
Xilinx
7

LUTs
Registers
D. Memory
B. Memory
DSPs

31
8
4
-

352
114
1
-

630
194
-

382
43
6
1

36
24
-

252
163
-

646
239
1
-

FPGAs
Cyclone
V

LUTs
Registers
D. Memory
B. Memory
DSPs

29
8
16
-

307
96
3
-

635
194
-

338
67
2
1

26
24
-

154
151
1
-

512
240
2
-

FPGAs
ICE40

LUTs
Registers
D. Memory
B. Memory
DSPs

285
136
-

544
96
7
-

1100
194
-

821
67
2
-

35
24
-

273
151
1
-

851
240
5
-

FPGAs
GoWin

LUTs
Registers
D. Memory
B. Memory
DSPs

48
8
4
-

502
95
2
-

1099
194
-

1085
43
16
-

29
24
-

285
151
1
-

796
239
1
-

## PDF page 15

Xilinx
7

D. Memory
B. Memory

DSPs
LUTs
Electronics
2024, 13, 781
FPGAs
Registers

Cyclone
V

Device
FPGAs
ICE40
FPGAs
ECP5

FPGAs
GoWin

FPGAs
ECP5

D. Memory
B. Memory
DSPs
LUTs
Measured
Registers
Item
D. Memory
B. LUTs
Memory
Registers
DSPs
D. Memory
LUTs
B. Memory
Registers
DSPs
D. Memory
B. Memory
DSPs
LUTs
Registers
D. Memory
B. Memory
DSPs

4
‐
‐

‐
1
‐

‐
‐
‐

6
‐
1

‐
‐
‐

‐
‐
‐

‐
1
‐

29
8
16
‐
Table
‐ 8. Cont.

307
635
338
26
154
512
15 of 20
96
194
67
24
151
240
‐
‐
‐
‐
‐
‐
3
‐
2
‐
1
2
‐
‐
1
‐
‐
‐
285
544
1100
821
35
273
851
Femto
136
96
194
24
151
240
J067
MCPU
UKP
ZPU
Baby8
6502
16
‐
‐
‐
‐
‐
‐
‐
9015
2991
30‐
7842
1159
478
77‐
7
‐
239‐
151‐
24‐
43‐
194‐
95‐
8‐
16
4
48
502
1099
1085
29
285
796
1
1
2
8
95
194
43
24
151
239
1
4
‐
‐
16
‐
‐
‐
‐
2
‐
‐
‐
1
1
‐ We show the‐ main results ‐classified as ‐
‐
ASICs, NAND ‐gates, and
FPGAs. For the ‐
ASICs,
we77
inform the 478
maximum clock
frequency, the
consumption, the
efficiency, and
30
299
901 the
1159
784 power
effective area of 95
the CORE and
material
8
194DIE (DIE is43a small block
24of semiconducting
151
239 on
4 a given ‐
‐ is fabricated).
16
‐
‐
‐
which
functional circuit
‐
1
1
‐ For the NAND
2 gates, we provide
‐
‐
the plain number of gates used. And for the FPGAs,
‐
‐
1
‐
‐
we inform
the number
of LUTs,‐ registers, distributed
memories,
block memories,
and‐ DSP

units used for each family of FPGA (Xilinx 7, Cyclone V, ICE 40, Gowin, and ECP 5).
Figures8 8and
and9 9show
showthe
thetotal
totalutilization
utilizationofofthe
theDIE
DIEarea
areaand
andthe
thenumber
numberofofNAND
NAND
Figures
gatesused
usedby
byeach
eachprocessor.
processor.
gates

Figure8.8.The
Theutilization
utilizationofofthe
thetotal
totalDIE
DIEarea
areabybythe
theCORES
CORESprocessor.
processor.
Figure

As shown in Figure 10, the number of LUTs can vary greatly depending on the chosen
FPGA family for the same processor. The best use of resources is often linked to the
improvement of development tools and the integration of the synthesis results generated
into their own internal hardware. So a project decision cannot be based only on lower
prices of the FPGA chips but also on their efficiency in the synthesis due to a greater use of
resources based on the company’s technology.
Figure 11 shows an extremely low use of FPGA resources for the I/O generic purpose
processor Baby8 (that was exactly our initial goal in this project) in comparison with
Figure 12 (darkRISCV) and Figure 13 (J0). Only the FPGA family ICE40 synthesized the
Baby8 soft-core processor with a high use of resources.

## PDF page 16

Electronics 2024, 13, 781
Electronics 2024, 13, x FOR PEER REVIEW

18 of1623of 20

Figure 9. Soft‐core processor resource utilization for the ASICs/FPGAs based on the number of
NAND gates.

As shown in Figure 10, the number of LUTs can vary greatly depending on the
chosen FPGA family for the same processor. The best use of resources is often linked to
the improvement of development tools and the integration of the synthesis results gen‐
Figure 9.
Soft‐core
processor
resource
utilization
the decision
ASICs/FPGAs
basedbeonbased
the number
of
erated
into
their own
internal
hardware.
So a for
project
cannot
only on
Figure 9. Soft-core processor resource utilization for the ASICs/FPGAs based on the number of
NANDprices
gates. of the FPGA chips but also on their eﬃciency in the synthesis due to a
lower
NAND gates.
greater use of resources based on the company’s technology.
As shown in Figure 10, the number of LUTs can vary greatly depending on the
chosen FPGA family for the same processor. The best use of resources is often linked to
the improvement of development tools and the integration of the synthesis results gen‐
erated into their own internal hardware. So a project decision cannot be based only on
lower prices of the FPGA chips but also on their eﬃciency in the synthesis due to a
greater use of resources based on the company’s technology.

Electronics 2024, 13, x FOR PEER REVIEW

19 of 23

Figure 10. The proportion of LUTs allocated per soft‐core processor and per FPGA model.
Figure 10. The proportion of LUTs allocated per soft-core processor and per FPGA model.

Figure 11 shows an extremely low use of FPGA resources for the I/O generic pur‐
pose processor Baby8 (that was exactly our initial goal in this project) in comparison
with Figures 12 (darkRISCV) and Figure 13 (J0). Only the FPGA family ICE40 synthe‐
sized the Baby8 soft‐core processor with a high use of resources.
Figure 10. The proportion of LUTs allocated per soft‐core processor and per FPGA model.

Figure 11 shows an extremely low use of FPGA resources for the I/O generic pur‐
pose processor Baby8 (that was exactly our initial goal in this project) in comparison
with Figures 12 (darkRISCV) and Figure 13 (J0). Only the FPGA family ICE40 synthe‐
sized the Baby8 soft‐core processor with a high use of resources.

Figure 11. Proportion of LUTs, registers, distributed memories, block memories, and DSP units al‐
Figure
Proportion
of LUTs,per
registers,
distributed memories, block memories, and DSP units
located11.
for the
Baby8 processor
FPGA model.
allocated for the Baby8 processor per FPGA model.

## PDF page 17

Electronics 2024, 13, 781

17 of 20

Figure 11. Proportion of LUTs, registers, distributed memories, block memories, and DSP units al‐
located for the Baby8 processor per FPGA model.

Electronics 2024, 13, x FOR PEER REVIEW
of al‐
23
Figure 12. Proportion of LUTs, registers, distributed memories, block memories, and DSP 20
units

Figure 12. Proportion of LUTs, registers, distributed memories, block memories, and DSP units
located for the darkRISC‐V processor per FPGA model.
allocated for the darkRISC-V processor per FPGA model.

One can notice that the same processor, darkRiscV (Figure 10), could be synthesized
using more registers or more LUTs, depending on the FPGA family chosen.
The J0 processor is the only processor in this study that used FPGA DSP units for
the FPGAs Xilinx 7, Cyclone V, and ECP 5. This is the reason why the FPGAs ICE40 and
GoWin are consuming much more LUTs and registers than other ones in J0 on the radar
plot of Figure 9. And despite the fact that the J0 processor consumes almost the same
number of NAND gates as the darkRISCV processor (Figure 8), it consumes much less of
the FPGA’s LUTs and registers due to the use of these FPGA’s DSP units.

Figure 13. Proportion of LUTs, registers, distributed memories, block memories, and DSP units al‐
Figure 13. Proportion of LUTs, registers, distributed memories, block memories, and DSP units
located for the J0 processor per FPGA model.
allocated for the J0 processor per FPGA model.

4.1. Performance
One can notice that the same processor, darkRiscV (Figure 10), could be synthesized
Although
performance
not adepending
measure of
resource
utilization
se, resource con‐
using more
registers or
more is
LUTs,
on the
FPGA
family per
chosen.
tention
certainly
impacts
directly on
the final
performance
a FPGA
processor
design.
The J0
processor
is the only
processor
in this study
that of
used
DSP
units for the
FPGAs
Cyclone V,
and of
ECPthis
5. This
is is
thetoreason
whya the
FPGAs with
ICE40low
andresource
GoWin
AsXilinx
much7,as the
objective
paper
develop
processor
are
consuming
much
and registers
ones in
on the
radarwe
plot
of
usage (in
terms
of more
internalLUTs
components
for than
FPGAsother
or even
areaJ0for
ASICs),
must
Figure
despite athe fact
that the J0
processor
consumes almost
the of
same
of
show 9.
in And
this section
comparative
analysis
of the final
performance
the number
developed
NAND
gates
as
the
darkRISCV
processor
(Figure
8),
it
consumes
much
less
of
the
FPGA’s
processor compared to the others analyzed.
LUTs In
and
registers
duecan
to the
these
FPGA’s DSP
units.
Figure
14, we
see use
thatofour
processor,
Baby8,
successfully achieves an average
performance in maximum clock frequency as well as eﬃciency in power consumption
4.1.
Performance
among
all other processors.
Although performance is not a measure of resource utilization per se, resource contention certainly impacts directly on the final performance of a processor design.
As much as the objective of this paper is to develop a processor with low resource
usage (in terms of internal components for FPGAs or even area for ASICs), we must show
in this section a comparative analysis of the final performance of the developed processor
compared to the others analyzed.

## PDF page 18

4.1. Performance

Electronics 2024, 13, 781

Although performance is not a measure of resource utilization per se, resource con‐
tention certainly impacts directly on the final performance of a processor design.
As much as the objective of this paper is to develop a processor with low resource
usage (in terms of internal components for FPGAs or even area for ASICs), we
must
18 of
20
show in this section a comparative analysis of the final performance of the developed
processor compared to the others analyzed.
Figure14,
14,we
wecan
cansee
seethat
thatour
our
processor,
Baby8,
successfully
achieves
average
InInFigure
processor,
Baby8,
successfully
achieves
anan
average
performance
in
maximum
clock
frequency
as
well
as
eﬃciency
in
power
consumption
performance in maximum clock frequency as well as efficiency in power consumption
amongallallother
otherprocessors.
processors.
among

Figure 14. Maximum clock frequency (MHz) vs. efficiency (MHz/mW) in an ASIC simulation with a
130 nm process and using the worst-case scenario: 1.6 volts at a temperature of 100 ◦ C.

The frequency measurements were performed with OpenLane2 [11,12]. For each
project, the OpenLane2 was configured to synthesize using the Sky130A PDK from Skywater and to use a 100 ns clock period (10 MHz) for the timing analysis.
This analysis was performed several times during the chip generation process, including after placement and routing. The timing analysis is done for the best case (low
temperature and high supply voltage), the typical case, and the worst case (high temperature and low supply voltage). In addition, the analysis is performed for the minimum,
nominal, and maximum delays for the components.
The limiting factor of how high the clock for the device can be is indicated by the
worst case setup time slack for the maximum delay with high temperature and low supply
voltage. Subtracting this value from the clock period gives us a higher clock than the
original 10 MHz.
Synthesis is run again, and the same circuit should result, but the timing analysis will
give a different setup slack in the worst case. It might seem that the new number would be
zero, but there are several complicating factors, and the actual result will be smaller than
the first time but still a positive value. The new number is subtracted from the new clock
period, and the process is repeated. This allows a successive approximation to the actual
maximum clock possible for each processor.
4.2. Layouts
The chip layouts were also produced using the Open Lane 2 tool [12], and the layouts
of the smallest area (MCPU) and largest area (vexRISC-V) processors implemented are
shown in Figure 15.

## PDF page 19

the new clock period, and the process is repeated. This allows a successive appro
tion to the actual maximum clock possible for each processor.
4.2. Layouts
Electronics 2024, 13, 781

19 of 20
The chip layouts were also produced using the Open Lane 2 tool
[12], and th
outs of the smallest area (MCPU) and largest area (vexRISC‐V) processors implem

(a) MCPU

(b) vexRISC‐V

Figure area
15. The
smallest
(MCPU)
and largest area
chip layouts.
Figure 15. The smallest
(MCPU)
andarea
largest
area (vexRISC-V)
chip(vexRISC‐V)
layouts.

5. Discussion 5. Discussion

Although our developed
Baby8
soft-core
processor
achieves
very good
results
Although our
developed
Baby8
soft‐core
processor
achieves
veryingood res
performance (~57
MHz) and(~57
energy
consumption
we need
make
can
performance
MHz) and
energy(~2 mW),
consumption
(~2 to
mW),
we sure
needitto
make sure
meet the initially
proposed
requirements
of
using
few
FPGA
internal
resources.
meet the initially proposed requirements of using few FPGA internal resources.
In order to runInthis
analysis,
results were
compared
withcompared
6502 results,
order
to runBaby8
this analysis,
Baby8
results were
withboth
6502 results
implemented inimplemented
the ICE40 FPGA
family.
in the ICE40 FPGA family.
Baby8 uses practically half as many LUTs (285) as 6502 (544) in the same FPGA. It still
uses a bit more registers—136—against 96 of 6502, but does not use any additional memory
blocks, despite the fact that 6502 uses seven blocks or memory RAM.
Since both processors are very similar in all other aspects (both are CISC 8-bits with
the same power consumption and the same maximum achieved frequency clock), we can
consider that the Baby8 architecture could save up to half of the FPGA resources compared
with the 6502 for the same features in the project.
6. Conclusions
Our developed soft-core processor architecture successfully achieves the goals of
staying tiny and saving nearly half of the resources in FPGA implementation, keeping the
same performance and power consumption as similar processors.
Author Contributions: Conceptualization, methodology, software: J.M.d.A.J.; formal analysis, investigation, data curation: M.G.; review, supervision, project administration and funding acquisition: O.H.A.J., M.R.C. and J.P.C. All authors have read and agreed to the published version of
the manuscript.
Funding: This research was funded by the Brazilian Ministry of Science, Technology, and Innovations
by providing five undergraduate grants in PMN-Design microelectronics program 2B, managed by
the Eldorado Institute, Grant #SSJ14547.
Data Availability Statement: All data and software are available online at the authors’ Github
repositories: https://github.com/jeceljr/baby8 and https://github.com/jeceljr/SoftCoreCompare
accessed on 11 February 2024.
Acknowledgments: The Brazilian Ministry of Science, Technology, and Innovations, Eldorado Institute,
Chandler Klüser, Alejandra Victoria Herrera, Hugo Puertas, Beatriz Aimee Teixeira Furtado Braga,
Gabriel Valizi, Gabriel Victor Santana, Samuel Rocha Silva, Vinicius Caffeu, and Maximiliam Luppe.
Conflicts of Interest: The authors declare no conflict of interest.

## PDF page 20

Electronics 2024, 13, 781

20 of 20

Abbreviations
The following abbreviations are used in this manuscript:
ALU
ASIC
CISC
CPU
FPGA
I/O
RAM
RISC

Arithmetic logic unit
Application-specific integrated circuit
Complex instruction set computer
Central processing unit
Field-programmable gate array
Input/output
Random access memory
Reduced instruction set computer

References
1.

2.

3.
4.
5.

6.
7.

8.

9.
10.
11.
12.

Glaser, J.; Wolf, C. Methodology and Example-Driven Interconnect Synthesis for Designing Heterogeneous Coarse-Grain
Reconfigurable Architectures. In Proceedings of the Models, Methods, and Tools for Complex Chip Design; Haase, J., Ed.; Springer:
Cham, Switzerland, 2014; pp. 201–221.
Shah, D.; Hung, E.; Wolf, C.; Bazanski, S.; Gisselquist, D.; Milanovic, M. Yosys+nextpnr: An Open Source Framework from
Verilog to Bitstream for Commercial FPGAs. In Proceedings of the 2019 IEEE 27th Annual International Symposium on FieldProgrammable Custom Computing Machines (FCCM), San Diego, CA, USA, 28 April–1 May 2019; pp. 1–4. [CrossRef]
Assumpção, J. Baby8. 2023. Available online: https://github.com/jeceljr/baby8 (accessed on 11 February 2024).
Patterson, D.A.; Hennessy, J.L. Computer Organization and Design ARM Edition: The Hardware Software Interface; Morgan Kaufmann:
Cambridge, MA, USA, 2016.
Hiremath, S.; Chickerur, S.; Dandin, J.; Patil, M.; Muddinkoppa, B.; Adakoli, S. Open-source Hardware: Different Approaches
to Softcore implementation. In Proceedings of the 2022 International Conference on Distributed Computing, VLSI, Electrical
Circuits and Robotics (DISCOVER), Shivamogga, India, 14–15 October 2022; pp. 76–83. [CrossRef]
SiFive. 2023. Available online: https://www.sifive.com/about (accessed on 11 February 2024).
Heinz, C.; Lavan, Y.; Hofmann, J.; Koch, A. A Catalog and In-Hardware Evaluation of Open-Source Drop-In Compatible RISC-V
Softcore Processors. In Proceedings of the 2019 International Conference on ReConFigurable Computing and FPGAs (ReConFig),
Cancun, Mexico, 9–11 December 2019; pp. 1–8. [CrossRef]
Gruin, A.; Carle, T.; Cassé, H.; Rochange, C. Speculative Execution and Timing Predictability in an Open Source RISC-V Core. In
Proceedings of the 2021 IEEE Real-Time Systems Symposium (RTSS), Dortmund, Germany, 7–10 December 2021; pp. 393–404.
[CrossRef]
Coluccio, A.; Ieva, A.; Riente, F.; Roch, M.R.; Ottavi, M.; Vacca, M. RISC-Vlim, a RISC-V Framework for Logic-in-Memory
Architectures. Electronics 2022, 11, 2990. [CrossRef]
Copeland, B. TheManchester Computer: A Revised History Part 2: The Baby Computer. IEEE Ann. Hist. Comput. 2011, 33, 22–37.
[CrossRef]
Ghazy, A.A.; Shalan, M. OpenLANE: The Open-Source Digital ASIC Implementation Flow. 2020. Available online: https:
//woset-workshop.github.io/PDFs/2020/a21.pdf (accessed on 11 February 2024).
Wang, H.; Li, T.; Li, Y.; Chen, L.; Sima, C.; Liu, Z.; Wang, B.; Jia, P.; Wang, Y.; Jiang, S.; et al. OpenLane-V2: A Topology Reasoning
Benchmark for Unified 3D HDMapping. In Proceedings of the Thirty-Seventh Conference on Neural Information Processing
Systems Datasets and Benchmarks Track, New Orleans, LA, USA, 10–16 December 2023.

Disclaimer/Publisher’s Note: The statements, opinions and data contained in all publications are solely those of the individual
author(s) and contributor(s) and not of MDPI and/or the editor(s). MDPI and/or the editor(s) disclaim responsibility for any injury to
people or property resulting from any ideas, methods, instructions or products referred to in the content.
