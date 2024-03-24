# Modeling Finite State Machine in Verilog HDL: Mealy FSM
## Implementation of Sequence Detector (1011 sequence) using Mealy FSM
We know that synchronous sequential circuits change and affect their states for every positive or negative transition of the clock signal based on the input. So, this behavior of synchronous sequential circuits can be represented in a graphical form and it is known as a state diagram. A synchronous sequential circuit is also called a Finite State Machine FSM if it has a finite number of states. There are two types of FSMs.
1. Mealy State Machine
2. Moore State Machine

### Modeling of Mealy FSM: Implementation of 1011 Sequence Detector (Non-overlapping)
![image](https://github.com/charlie2951/vlsi/assets/90516512/e6296725-7d7d-464b-93c8-c52663cd41fd)
### Design Code for 1011 Sequence detector using Mealy type FSM
```verilog
module mealy1011(
    input rst,clk,din,
    output reg dout
    );
    
    reg [1:0] state;
    parameter s0=0,s1=1,s2=2,s3=3;
    always @(posedge clk) begin
    if(rst) begin
    dout=0;
    state=s0;
    end
    else
    case(state)
    s0: begin
    if(din)
    state=s1;
    else
    state=s0;
    dout=0;
    end
    s1: begin
        if(din)
        state=s1;
        else
        state=s2;
        dout=0;
        end
s2: begin
                if(din)
                state=s3;
                else
                state=s0;
                dout=0;
                end
s3: begin
        if(din) begin
        state=s0;
        dout=1;
        end
        else begin
        state=s2;
        dout=0;
        end
        end
    
    endcase
    end
    endmodule
```
### Testbench 
```verilog
module mealy1011_test(   );
    
    reg rst,clk,din;
     wire dout;
      mealy1011 DUT(rst,clk,din,dout);
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
      din=1;#20;
      $finish;
      end
      always #10 clk=!clk;
    endmodule
```
### Simulation Result
![image](https://github.com/charlie2951/vlsi/assets/90516512/dc57ba5c-e74f-4051-a42f-ba27b8137bf6)

