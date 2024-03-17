# Lab-04: Conversion of Flip flops
### D Flip flop design using S-R flip flop

**Note:** Copy SR Flip flop design code from Lab-03.

```verilog
module dff(q,qb,d,clk);
output q,qb;
input d,clk;
srff UU0(q,qb,d,!d,clk);
endmodule
```
### Testbench
```verilog
module dff_tb;
reg d,clk;
wire q,qb;
dff L0(q,qb,d,clk);
initial
begin
clk=0;
d=0;#10;
d=1;#10;
d=0;#10;
$finish;
end
always #5 clk=!clk;
endmodule
```
