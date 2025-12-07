Goal: To understand the trends in area, leakage as a function of cell-drive. 

Model: lib/sky130_fd_sc_hd__tt_025C_1v80.lib (Typical, 25C, 1.8V, Skywater 130nm)

Results
<img width="2019" height="805" alt="image" src="https://github.com/user-attachments/assets/0885e53f-cf31-41a4-90c4-bbf41a58d707" />
As expected, area and leakage increases with cell-drive. 

---

Goal: To understand the difference between hierarchical synthesis and flat synthesis

Design: multiple_modules.v

Design Description:\
<img width="739" height="453" alt="image" src="https://github.com/user-attachments/assets/5d03afcf-6256-4209-a81f-91cd419cb3b8" />

\
Script
<img width="1136" height="179" alt="image" src="https://github.com/user-attachments/assets/8704621d-b3e6-420e-a164-25ed2a164e13" />

\
Schematic
<img width="1262" height="281" alt="image" src="https://github.com/user-attachments/assets/5013e729-dfa1-49c1-a829-12aa8123a11e" />

\
Hierarchical Netlist

<img width="308" height="937" alt="image" src="https://github.com/user-attachments/assets/151e5d5e-9340-4a7c-9d37-517423ce53a8" />

\
Flattened Netlist (using "flatten" command)

<img width="371" height="1006" alt="image" src="https://github.com/user-attachments/assets/93b2a4bc-0c35-4008-9ccc-2162846e75df" />

\
Synthesis can also be done at the submodule level (synth -top 'submodule') for the following reasons:
1. Divide and Conquer (for large SoCs)
2. BLA Reuse (should there be multiple instances of the same module)

--- 
The script for performing RTL simulation for the following three DFFs is shown below:
<img width="445" height="309" alt="image" src="https://github.com/user-attachments/assets/fa10203f-bd60-4122-beee-78190f45e92f" />

The script for performing logic synthesis for the following three DFFs is shown bellow:
<img width="623" height="454" alt="image" src="https://github.com/user-attachments/assets/6ccde85a-1e19-4640-b677-3354d171a20f" />

---

Goal: To simulate a flop with asynchronous reset using iverilog and view the waveforms with GTKWave. 

Design: dff_asyncres.v

RTL SIM
<img width="965" height="167" alt="image" src="https://github.com/user-attachments/assets/6f01ca5d-2326-4cbd-b59f-56894e03917a" />

Synthesis Schematic
<img width="971" height="148" alt="image" src="https://github.com/user-attachments/assets/766f82a0-4bcc-46b2-8353-4ad059faaee0" />
There is an inverted since the instantiated flop has an active low RESET. 

---

Goal: To simulate a flop with asynchronous set using iverilog and view the waveforms with GTKWave.

RTLSIM
<img width="988" height="172" alt="image" src="https://github.com/user-attachments/assets/8dcb2fd4-eec0-4560-be2d-cd29058487aa" />

Synthesis Schematic\
<img width="735" height="117" alt="image" src="https://github.com/user-attachments/assets/24aa1f7e-9b1e-45ad-b41a-58d7f7549de6" />

---

Goal: To simulate a flop with synchronous reset using iverilog and view the waveforms w/ GTKWave. 

RTLSIM
<img width="967" height="165" alt="image" src="https://github.com/user-attachments/assets/27439a77-7594-4af6-8936-887735f3e72b" />

Synthesis Schematic
<img width="1661" height="321" alt="image" src="https://github.com/user-attachments/assets/27af7a85-62ba-473e-9061-36b0c17ff398" />

---
Notes

1. The instructor demonstrates certain special use-cases whereby arithmetic operations can be implemented solely by rewiring. Corresponding HDLs are mult_2.v and mult_8.v.
2. Schematic from Yosys when synthesising mul2 is as follows:
   <img width="730" height="220" alt="image" src="https://github.com/user-attachments/assets/06d64702-d661-4c62-b1bc-459d7d99796e" />

   y[1:3] is mapped to a[0:2]
   
   y[0] = 0
