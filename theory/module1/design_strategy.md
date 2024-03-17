# VLSI Design Strategy
From our previous discussions, it is clear that the VLSI design process is complex. 
There are some useful techniques to reduce the design complexity. These are discussed below.
## Design Hierarchy  <br>
This is similar to the divide-and-rule approach. A larger system with unmanageable complexity is further divided into smaller parts. This decomposition process will continue until and unless the complexity of the generated blocks is manageable. For example, one eight-bit full adder can be decomposed into eight single-bit adders. Now it is much easier to design a single-bit adder. Each single-bit adder can be further divided into sum and carry parts. Finally, at the end of the design process, all eight adders are connected and form the eight-bit adder. The hierarchy process is shown in the figure below.

## Regularity <br>
At the time of decomposition, the designer must look for not only simple blocks but also similar types of blocks as much as possible. This strategy reduces the design time. For example, if one designer designs a single-bit adder, then the same design will be repeated to form a complete eight-bit adder quickly.

## Modularity
After decomposition, the generated sub-modules must have well-defined, independent functions and interfaces. This property permits the designer to test each sub-module independently and to allow the design of multiple components parallelly (since each module is independent of the other).

## Locality
This property ensures that the interconnection between sub-modules should be within local places. That means, the modules should be placed close to each other to avoid long-distance wiring and thus reduces interconnect delays and also fabrication cost.
