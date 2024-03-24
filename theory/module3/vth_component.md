# Threshold Voltage and it's components
<p>The threshold voltage is said to be the boundary between the ON and OFF states of a logic transistor. Theoretically, it is the minimum value of gate voltage required to establish the strong inversion condition.</p>
<p>Different Components of&nbsp; Threshold voltage are:</p>
<ul>
<li>Work-function difference between the gate and the substrate ($\phi_{ms}$).</li>
<li>Amount of gate voltage component to be applied to achieve strong inversion condition i.e. $-2 \phi_{f}$</li>
<li>The amount of gate voltage component required to nullify or compensate the voltage developed by depletion charges (Q<sub>B0</sub>/Cox, where Q<sub>B0</sub>&nbsp;is the depletion charge density).</li>
<li>Due to oxide impurity and lattice mismatch between two different regions, there is always a significant amount of trapped charge. the gate voltage component required to offset the trapped charge is also another component of threshold voltage (Qox/Cox, where Qox is the amount of trapped charge.).</li>
</ul>
<p>Adding all these, the final expression of threshold voltage (V<sub>TO</sub>) is given as:</p>
<p>$V_{T,0}=\phi_{GC}-2\phi_f-\frac{Q_{B0}}{C_{ox}}-\frac{Q_{ox}}{C_{ox}}$</p>
<p>where $Q_{B0}=-\sqrt{2qN_A\epsilon_{si}|-2\phi_f|}$, is the expression for depletion charge. Note that if the source and body terminal of MOSFET is not at the same potential i.e. V<sub>SB</sub> is nonzero, then the expression for depletion charge will be</p>
<p>$Q_{B}=-\sqrt{2qN_A\epsilon_{si}|-2\phi_f+V_{SB}|}$</p>
<p>Note that, the above expression of the threshold voltage is valid for zero source-body voltage (VSB=0). For non-zero VSB, the expression is modified to</p>
<p>$V_{T}=\phi_{GC}-2\phi_f-\frac{Q_{B}}{C_{ox}}-\frac{Q_{ox}}{C_{ox}}$ and can be expressed in the form</p>
<p>$V_T=V_{T0}+\gamma[\sqrt{|-2\phi_f+V_{SB}}-\sqrt{-2\phi_f}]$</p>
<p>where $\gamma=\sqrt{2qN_A\epsilon_{si}}/C_{ox}$ is called the body factor.</p>
<p>Note that, the expression of the threshold voltage is only valid for long channel MOSFET where gradual channel approximation is valid. In the case of short-channel MOS transistors, due to the enhanced 2-D nature of the electric field, threshold voltage decreases from its long channel value. In general, this effect is called threshold voltage roll-off due to <em>Drain induced barrier lowering (DIBL)</em> phenomenon.</p>
