# Super Buffer (Chain of Inverters)
A super buffer is a chain of inverters connected in a cascade that is used to drive a large capacitive load. When the load capacitor value increases, the delay of the logic gate also increases. So, to drive the load with minimum delay, a large amount of current is required to charge and discharge the capacitor. In a MOS transistor, current can be increased by increasing device width (W). As a result, overall device size increases. The parasitic capacitances associated with the MOS transistor are proportional to the device size. With an increase in size, parasitic components also increase which in turn further increases output load capacitance.</p>



![image](https://github.com/charlie2951/vlsi/assets/90516512/24e56f8c-24e2-4038-b17d-165fcaa162f1)

<p>So, instead of taking a large device, a smart designer will increase the size of the device gradually so that it will not be a burden for the next stage. For this purpose, one intermediate stage called super buffer is used to connect the logic gate and load capacitor. A super buffer is a chain of inverters connected in a cascade and the device size in each stage increases gradually. In Figure-1, the portion within the rectangular box indicates the buffer. For the 1st stage of the buffer, the device size is $\alpha$, in the next stage it is $\alpha^2$, and so on. The gate and drain capacitance (input and output capacitance) of each stage are represented by Cg and Cd and multiplied by device size ($\alpha^N$).</p>



<p>The objective is to find out the optimum multiplying factor $\alpha$ so that the delay will be minimal. To calculate this, 1st, we need to calculate the total delay of the network. It may be noted that: $C_{load}=\alpha^{N+1}C_g$ (because Cload is equivalent to the input capacitance of the $(N+1)$-th stage.</p>



<p>So, $C_{load}=\alpha^{N+1}C_g$, from here we can write: $N+1=\frac{ln(Cload/Cg)}{ln\alpha}$</p>



<p>Let, the delay of each stage in a chain of unit size inverter (device size is 1 in each stage) stage having input and output capacitance (Cg and Cd) be $\tau_0$. Considering the 1st block where total capacitance at the output is (Cd+ $\alpha$ Cg), the delay will be $\tau_0(C_d+\alpha C_g)/(C_d+C_g)$.</p>



<p>Hence, the total delay for (N+1) number of stages will be: $\tau_{total}=\frac{(N+1).\tau_0.(C_d+\alpha C_g)}{(C_d+C_g)}$</p>



<p>The term N+1 can be replaced by the previous equation. To achieve minimum delay, the derivative of the above equation concerning $\alpha$ must be zero. After taking the derivative and some mathematical simplification, the following relationship can be obtained: $\alpha(ln\alpha-1)=\frac{C_d}{C_g}$.</p>



<p>Special case: Considering Cd=0, the above equation is simplified to $\ln\alpha=1$, so $\alpha=2.713$.</p>



<p>Hence, for minimum delay (assuming Cd=0, although in real cases Cd is nonzero), the optimum value of $\alpha$ is 2.713=3.</p>
