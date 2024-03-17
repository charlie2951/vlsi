# 4-bit Ripple carry adder using single bit adder
*Note:* You need to include 1-bit adder code in your project/design<br>

*Copy 1-bit adder design code from Lab-01.* <br>
**4bit adder using 1bit adder** <br>
*Let module name of 1bit adder is fa1*
**Design code** <br>
```verilog
module fa4(s,co,a,b);
input [3:0] a,b;
output [3:0] s;
output co;
wire w1,w2,w3;
//call 1bit adder module and defn connection
fa1 U0 (s[0],w1,a[0],b[0],0);
fa1 U1 (s[1],w2,a[1],b[1],w1);
fa1 U2 (s[2],w3,a[2],b[2],w2);
fa1 U3 (s[3],co,a[3],b[3],w3);
endmodule
```
**Testbench code**
```verilog
module fa4_tb();
reg [3:0]a,b;
wire [3:0] s;
wire co;
fa4 U0 (s,co,a,b);
initial begin
$dumpfile("dump.vcd");
$dumpvars;
a=2;b=3;
#20;
a=1;b=4;
#20;
a=4;b=6;
#20;
$finish;
end
endmodule
```
