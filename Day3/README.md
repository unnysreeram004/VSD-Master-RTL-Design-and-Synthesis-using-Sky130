---
Scripts for the following labs are as shown below

Combinatorial Opt

<img width="592" height="516" alt="image" src="https://github.com/user-attachments/assets/716ce556-361e-4e88-a522-27d63ab10e71" />

Sequential Opt

<img width="631" height="623" alt="image" src="https://github.com/user-attachments/assets/b37cfbd2-58c3-4bea-bab8-6c6cac15ef24" />

---
Goal: To verify different combinatorial optimization techniques using Yosys.

Design: opt_check.v

Schematic

<img width="733" height="160" alt="image" src="https://github.com/user-attachments/assets/041636f9-028e-468e-a85a-6d61a33af42d" />

Design: opt_check2.v

Schematic

<img width="733" height="164" alt="image" src="https://github.com/user-attachments/assets/dbc943df-4f1d-45f4-bea3-f1a2163ac1b8" />

Design: opt_check3.v

Schematic

<img width="745" height="245" alt="image" src="https://github.com/user-attachments/assets/a2f8aaab-9ccc-4561-817b-0583287905dc" />

Design: opt_check4.v

Schematic

<img width="615" height="198" alt="image" src="https://github.com/user-attachments/assets/210ead24-d655-4b62-8637-bc0157d62d0c" />

Design: multiple_module_opt.v

Script

<img width="585" height="157" alt="image" src="https://github.com/user-attachments/assets/ccae1d79-9dc6-4026-a613-6081fc725da3" />

Schematic

<img width="734" height="355" alt="image" src="https://github.com/user-attachments/assets/faa68ee9-7a3c-4886-991e-289620cb56b1" />

---

Goal: To verify different sequential optimization techniques using Yosys.

Design: dff_const1.v

RTL SIM

<img width="680" height="122" alt="image" src="https://github.com/user-attachments/assets/702ecb3b-f121-4770-8157-854bf077932e" />

Schematic

<img width="734" height="120" alt="image" src="https://github.com/user-attachments/assets/04a08bd1-c7c2-4288-abcc-893da7153468" />

Design: dff_const2.v

RTL SIM

<img width="774" height="167" alt="image" src="https://github.com/user-attachments/assets/46a15046-ff38-40f5-a3d2-501970278824" />

Schematic

<img width="262" height="221" alt="image" src="https://github.com/user-attachments/assets/1cd36e73-f190-4753-a867-7c1fbe67beb6" />

Design: dff_const3.v

RTL SIM

<img width="1462" height="137" alt="image" src="https://github.com/user-attachments/assets/abf57b0b-a61b-4eec-90f5-5a803ae09f75" />

Schematic

<img width="1662" height="240" alt="image" src="https://github.com/user-attachments/assets/0a6eeeed-c325-48aa-af73-f50f28bd8c37" />

Design: dff_const4.v

Schematic

<img width="428" height="439" alt="image" src="https://github.com/user-attachments/assets/e15de876-d18c-400f-b7c0-f63036cc4330" />

Design: dff_const5.v

Schematic

<img width="1329" height="191" alt="image" src="https://github.com/user-attachments/assets/8f0cd835-678b-4ead-8483-c610b5563f44" />

---

The instructor then proceeds to prove that unused output signals gets optimized away using the HDL counter_opt.v. If you change the assign statement to the following (i.e. all three bits are being used to compute the output), the circuit schematic becomes more complex. 
<img width="602" height="315" alt="image" src="https://github.com/user-attachments/assets/c08b675e-4bb5-4ef6-a2eb-545451c5feab" />





