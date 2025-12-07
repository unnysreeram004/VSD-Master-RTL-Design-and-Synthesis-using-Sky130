Goal: To synthesize a 2:1 MUX using Yosys and run Gatelevel SIM (GLS) using iverilog. 

Design: ternary_operator_mux.v

RTL SIM

<img width="966" height="167" alt="image" src="https://github.com/user-attachments/assets/4fa6e427-c885-4c30-b82c-4f4e3ef810df" />

Schematic

<img width="735" height="231" alt="image" src="https://github.com/user-attachments/assets/e169db5a-c6c6-4d12-835a-68f523fd3f6c" />

Gatelevel Simulation

<img width="966" height="172" alt="image" src="https://github.com/user-attachments/assets/aaa97adf-5bc1-4b05-9756-e6e871bf6ad9" />

---

Goal: To highlight functional mismatches b/w RTL and Netlist. 

Design: bad_mux.v

RTL SIM

<img width="966" height="193" alt="image" src="https://github.com/user-attachments/assets/2b1235c1-1ea8-4236-b3fb-f1713472c8b2" />
It can be seen clearly that the design does not work as intended.

\
Schematic

<img width="735" height="231" alt="image" src="https://github.com/user-attachments/assets/65e27439-94de-4e42-b982-f077cb45e3b4" />

\
Script for GLS

<img width="1205" height="98" alt="image" src="https://github.com/user-attachments/assets/8e8ce341-f60c-40de-8176-cfe78e300d6f" />

\
GLS

<img width="966" height="166" alt="image" src="https://github.com/user-attachments/assets/90e41bf5-0184-4fbe-b1f2-3c265452d6cc" />

\
Design: blocking_caveat.v

Goal of the designer is to have a circuit as follows:

<img width="377" height="147" alt="image" src="https://github.com/user-attachments/assets/80b6a871-8559-40da-b379-05012813a71e" />

\
RTL SIM
<img width="966" height="192" alt="image" src="https://github.com/user-attachments/assets/e6cb3a27-7162-4acd-ae7d-a8254ea1fc0d" />
It can be seen clearly that the design does not work as intended.

\
Schematic

<img width="733" height="236" alt="image" src="https://github.com/user-attachments/assets/da312a17-7429-499c-9dfe-ddd622cf2c47" />

\
GLS

<img width="966" height="174" alt="image" src="https://github.com/user-attachments/assets/d2d7e4bc-5f0f-4b07-b66c-765e58464eb1" />

--- 

The key message is to avoid blocking statements since it can cause functional deviations b/w RTL and Netlist. 




