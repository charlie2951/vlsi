## Introduction ##
The electronics industry has achieved tremendous growth over the last few decades,
mainly due to the rapid advances in integration technologies 
and large-scale systems design. The use of integrated circuits 
in high-performance computing, telecommunications, and consumer 
electronics has been growing very fast. Typically, the required computational 
and information processing power of these applications is the driving force 
for the fast development of this field. This trend is expected to continue, 
with very important implications for VLSI and systems design.<br>
As more and more complex functions are required in various data processing and
telecommunications devices, the need to integrate these functions in a small package is also
increasing. The level of integration as measured by the number of logic gates in a
monolithic chip has steadily risen for almost three decades, mainly due to the rapid progress
in processing technology and interconnect technology. The table shows the evolution of logic
complexity in the integrated circuit over the last couple of decades.<br>
<img width="520" alt="1" src="https://github.com/charlie2951/vlsi/assets/90516512/5dbe4442-d5f9-4a93-8812-d762dbe9c26a">
<br>
## Moore’s Law ##
Moore’s law is a prediction of the growth rate of logic complexity made by Gordon Moore.
It says that the transistor count per chip increases exponentially over the years
(approximately two times every eighteen months).<br>
## VLSI Design Flow ##
The flowchart of the simplified VLSI design process is shown in the figure below. 
The design process starts with a given specification of the system such as which type of job can be
performed by the system, whether the system is fully analog or digital or mixed-signal type etc.
Also, there may be some specifications regarding the area, power dissipation, etc. By keeping all 
these specifications in mind, the designer decides the type of blocks/modules that will be used and
the specification or nature of each module. Sometimes, this type of design approach is termed as “top-down 
design methodology”.<br>
![image](https://github.com/charlie2951/vlsi/assets/90516512/caaafe85-102e-4fa7-be40-fb0c88a699c1)

After defining the system-level module descriptions, the architecture of each module should be specified.
For example, if one designer going to implement one ALU, the components such as adder, multiplier, etc. 
and their architecture must be clearly defined. There may be different types of adder architecture such 
as CLA adder, carry-save adder, Manchester carry adder, etc. To simplify the design, the designer may 
divide larger blocks into smaller sub-blocks. Sometimes the architectural design is also referred to as
functional design blocks.<br>
The architectural or functional design also tells about the input-output pins of the system. 
Generally, some verification steps are used after every design step. If the design does not satisfy
the system specifications, then the designer changes the functional block’s architecture to get a 
more efficient design.<br>
The next step after the functional design is logic design. This step explores all the functional blocks
and they are represented by their logic-level descriptions i.e. in terms of gates, flip-flops, 
registers, etc. If required, the designer may divide large logical blocks into several smaller parts 
to manage the design complexity. After the successful logic design, testing and verification are done 
to ensure the proper operation of the system. For digital systems, generally, hardware description
languages (HDL) are involved.<br>

In the next steps, the logic-level description of the system is represented by the circuit-level
description. For example, the logic gates are now represented using MOS transistors at the circuit level. 
Again there is testing and verification steps are followed to ensure correctness and also to meet the design metrics such as delay, power, area requirement, etc. Several CAD tools use SPICE to simulate the circuit and to verify the circuit level description.
<br>
Finally, in the physical design step, all transistors are replaced by their physical description i.e. 
layout. This step is very crucial and design metrics such as delay and area requirement strongly depend 
upon this step. A layout vs schematic analysis is performed to compare layout-generated circuit results
with schematic-level circuit performance. If the post-layout simulation does not meet the design criteria
which were mentioned in 1st step i.e. architecture level, the designer may modify the layout to satisfy 
these matrices.
<br>
Although the design process is described in a very brief way with a  couple of steps followed by top-down 
design methodology, the actual design flow involved several steps. In between two steps, as shown in the 
flowchart, there exist several smaller steps. Most of the steps are iterative and for a successful 
design, a top-down with a bottom-up approach is followed.
