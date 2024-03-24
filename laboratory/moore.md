# Lab-05: Sequence Detector Design using Moore FSM in Verilog
In this post, one sequence detector is designed in Verilog HDL using a Moore-type Finite state machine. A Finite State Machine is said to be a Moore state machine if outputs depend only on
present states. You can find the Mealy FSM-based sequence detector here. <br>
![image](https://github.com/charlie2951/vlsi/assets/90516512/145ee580-227e-48fd-984a-3dd8ecf4c6e0)

## Verilog Code for Moore 1011 Sequence Detector
```verilog
module moore1011(
    input rst,clk,din,
    output reg dout
    );
    reg [2:0] state;
    parameter s0=0,s1=1,s2=2,s3=3,s4=4;
    initial dout=0;
    always @(posedge clk) begin
    if(rst) begin
     state=s0;
    end
    else
    case(state)
    s0: state=din?s1:s0;
    s1: state=din?s1:s2;
    s2: state=din?s3:s0;
    s3: state=din?s4:s2;
    s4: state=din?s1:s0;
    default:state=s0;
    endcase 
    end
    always @(state)begin
    if(rst)
    dout=0;
    else
    case(state)
        s0:dout=0;
        s1:dout=0;
        s2:dout=0;
        s3:dout=0;
        s4:dout=1;
        default:dout=0;
        endcase
    end
    endmodule
```
## Testbench
```verilog
module moore1011_test();
    reg rst,clk,din;
     wire dout;
      moore1011 DUT(rst,clk,din,dout);
      initial begin
      clk=0;din=0;
      rst=1; #40;
      rst=0;
      //test input
      din=0;#20;
      din=1;#20;
      din=0;#20;
      din=1;#20;
      din=1;#20;
      din=0;#20;
      din=1;#20;
      din=1;#20;
      din=0;#20;
      din=0;#20;
      din=1;#20;
      din=0;#20;
      din=1;#20;
      din=1;#100;
      $finish;
      end
      always #10 clk=!clk;
    endmodule
```
## Simulation Result
![image](https://github.com/charlie2951/vlsi/assets/90516512/10e720c3-c60e-4fbb-a12f-aed442044aed)
