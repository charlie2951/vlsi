# VLSI Design Styles
A VLSI system sometimes is referred to as an ***Application Specific Integrated Circuit (ASIC)***. There are several methodologies to implement a VLSI system. Each one has its own advantages and drawbacks. They are (1) Full custom design (2) Semi-custom design and (3) Programmable design style. 

**(1) Full Custom Design**

In this design, the designer starts from scratch. This means that the designer abandons the approach of pre-designed and pre-tested and pre-characterized cells for all or part of the design. This might be because existing cell libraries are not fast enough, or the logic cells are not small enough or consume too much power. You may need to use full-custom design if the ASIC technology is new or so specialized that there are no existing cell libraries or because the ASIC is so specialized that some circuits must be custom designed. Fewer and fewer full-custom ICs are being designed because of the problems with these special parts of the ASIC. As a designer, you can optimize your design for speed, power, and area requirements. The full custom design approach needs more time and the cost of prototyping is higher compared to other design styles.

**(2) Semi-Custom Design**

In this type of design process, some part of the design is customized. That means the designer can pick up a pre-designed and tested cell from the cell library. Each cell library may contain an adder, subtractor, multiplier, flip flops, etc. For a single design, category say adder, there may be different variants with different speed and power ratings. This drastically reduces design time and cost. This is further divided into two categories: standard cell-based and gate array-based design.

2.1 Standard Cell-Based Design: In a standard cell-based design approach, the designer uses pre-designed logic cells such as gates (AND, OR, NOR, NAND, etc.), multiplexers, flip flops, etc., and they are commonly known as standard cells. Those pre-designed and tested cells are stored in a library. Different cells with different speed grades, power, and area requirements are also available. The chip designer only defines the placement and interconnections between different cells. By using standard cells, a designer can save time, and risk of failure by using a pre-designed tested, and characterized cell library.



 

The disadvantage of this type of design approach is the expense of purchasing the cell library. Also, it may take time to interconnect all layers. The average manufacturing lead time is six to eight weeks.

2.2 Gate Array-Based Design

In this design style, the transistors are predefined on a silicon wafer. These are called base arrays or base cells. Only the top few layers of metal which are used to make interconnections are customized. The designer chooses a pre-verified gate array library of logic cells. These are termed “macros“. The designer needs to define the interconnections between the base array.  Depending upon the configuration of base cells, there are three different types of gate array-based design, (i) channel-less (ii) Channelled, and (iii) Structured gate array.

 2.2.1 Channel-less gate array:

Only some of the mask layers are customized.
Manufacturing lead time between two days to two weeks
2.2.2  Channeled gate array:

Only interconnect is customized.
Interconnect uses pre-defined spaces between the row and base cell.
Manufacturing time is the same as a channel-less gate array.
2.2.3 Structured gate array:

Only interconnect is customized.
Custom blocks can be embedded by the designer.
Manufacturing time is almost the same as other types of gate array-based design.
