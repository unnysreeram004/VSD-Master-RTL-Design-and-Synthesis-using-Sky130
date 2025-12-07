DISCLAIMER:
This README only documents the labs since this is stated as the primary requirement for earning the completion certificate.

---

Goal: To setup the working environment for the upcoming labs. 

STEPS
1. Cloned the repository from https://github.com/kunalg123/sky130RTLDesignAndSynthesisWorkshop
2. Install iVerilog, gtkwave, Yosys. I used "-V" with both these tools to verify if they are installed correctly.

Directory Struture
<img width="1016" height="55" alt="image" src="https://github.com/user-attachments/assets/f173b01f-f763-464b-8647-e16e367bbe0d" />

Notes
* verilog_files/ contains all the design HDLs along with the respective test-benches. This is the primary working directory for all the labs in this course. 
* lib/ contains the liberty models of the std. cells. 
* my_lib/ contains the verilog models of the std. cells. 

---

Goal: To perform RTL SIM using iverilog and view the waveforms in GTKWave.

Design: good_mux.v

Design Testbench: tb_good_mux.v

Script\
<img width="1159" height="115" alt="image" src="https://github.com/user-attachments/assets/ead6ccc0-8c1c-403d-8ee3-967670da22e2" />

\
RTL SIM Waveforms
<img width="1206" height="215" alt="image" src="https://github.com/user-attachments/assets/a022f8a5-0186-4074-bb8d-1dae394caad9" />

---

Goal: To perform RTL synthesis and generate a netlist using Yosys. 

Design: good_mux.v

Script\
<img width="591" height="175" alt="image" src="https://github.com/user-attachments/assets/91f6fc54-6978-448e-86fe-dd0735c945f5" />

\
Schematic\
<img width="746" height="266" alt="image" src="https://github.com/user-attachments/assets/679e30e8-3930-48d6-92fd-e1ef123a6474" />

\
Netlist\
<img width="572" height="679" alt="image" src="https://github.com/user-attachments/assets/315bf0cd-57ec-401b-a484-8a8141ff792c" />

--- 

