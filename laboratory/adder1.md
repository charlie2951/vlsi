# Lab-01: Verilog Code for Single bit adder
## Design code (Using dataflow modeling style)
```verilog

module fa1(s,co,a,b,ci);
input a,b,ci;
output s,co;
//dataflow modeling
assign s=a^b^ci;
assign co=(a&b)|(b&ci)|(a&ci);
endmodule
```
## Testbench code
```verilog
module fa1_tb();
reg a,b,ci;
wire s,co;
fa1 U0 (s,co,a,b,ci);
initial begin
$dumpfile("dump.vcd");
$dumpvars;
a=0;b=0;ci=0;
#20;
a=0;b=0;ci=1;
#20;
a=0;b=1;ci=0;
#20;
a=0;b=1;ci=1;
#20;
a=1;b=0;ci=0;
#20;
a=1;b=0;ci=1;
#20;
a=1;b=1;ci=0;
#20;
a=1;b=1;ci=1;
#20;
$finish;
end
endmodule
```
