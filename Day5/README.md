---
Scripts for Synthesis

<img width="601" height="339" alt="image" src="https://github.com/user-attachments/assets/647bc599-f20d-49a0-8033-9a97c61fa659" />
<img width="597" height="514" alt="image" src="https://github.com/user-attachments/assets/238b160e-0cb0-41c1-beb4-e2c29d615f97" />


\
Scripts for RTL SIM

<img width="380" height="210" alt="image" src="https://github.com/user-attachments/assets/02a16738-7e32-405b-827d-ba9fc79ef418" />

\
<img width="469" height="522" alt="image" src="https://github.com/user-attachments/assets/1e137e44-254e-45ff-a4a7-c87553cd6422" />


---

Goal: To understand latch inference if there is an incomplete if-else. 

\
Design: incomp_if.v

Designer Expectation

<img width="810" height="317" alt="image" src="https://github.com/user-attachments/assets/ab85248a-84b4-47eb-afe5-56a77667fe23" />

\
RTL SIM

<img width="965" height="171" alt="image" src="https://github.com/user-attachments/assets/9a648426-7d5e-4166-932f-ae345fd9dc5d" />

If i0 = 0, then there is no change in y. This is mimicking the behavior of a latch.

Schematic

<img width="733" height="347" alt="image" src="https://github.com/user-attachments/assets/57a727a5-3f3a-48d8-9414-8a4d14a5f23b" />

Expectation upfront was completely proven to be wrong after synthesis.

\
Design: incomp_if2.v

Designer Expectation

<img width="831" height="407" alt="image" src="https://github.com/user-attachments/assets/ce8fa477-422a-4aae-934c-4e094762ef33" />

RTL SIM

<img width="968" height="205" alt="image" src="https://github.com/user-attachments/assets/69162d69-89ec-4e7b-aed1-bd19a4e2ea47" />

Schematic

<img width="733" height="171" alt="image" src="https://github.com/user-attachments/assets/a5af0662-28ba-4364-8152-8f9d5c028619" />

--- 

Goal: To understand latch inference if there is an incomplete case statements. 

\
Design: incomp_case.v

Designer Expectation

<img width="829" height="342" alt="image" src="https://github.com/user-attachments/assets/b0e52710-5dd7-4970-9520-5b6cdd2a6cc1" />

RTL SIM

<img width="967" height="202" alt="image" src="https://github.com/user-attachments/assets/1c0d7191-7e1c-49a1-9891-95aec389948c" />


Schematic

<img width="1532" height="273" alt="image" src="https://github.com/user-attachments/assets/f57d8763-ebde-4562-95cc-501890e82e6b" />

\
Design: comp_case.v

Designer Expectation

<img width="626" height="405" alt="image" src="https://github.com/user-attachments/assets/3b86c515-905a-42c7-aca3-75c6b83e6e32" />

RTL SIM

<img width="969" height="202" alt="image" src="https://github.com/user-attachments/assets/5f936308-9eb4-416f-b237-fed414dedaa2" />

Schematic

<img width="1373" height="247" alt="image" src="https://github.com/user-attachments/assets/e45b3cfa-8ea4-4d71-a70d-ba1b56c28742" />

There are no latches in the schematic as expected. 

\
Design: partial_case_assign.v

Designer Expectation (LHS)

<img width="831" height="314" alt="image" src="https://github.com/user-attachments/assets/400ecba0-5910-4012-8363-00dc222fd612" />

Schematic
<img width="1893" height="611" alt="image" src="https://github.com/user-attachments/assets/525f6714-82d5-4dcb-b832-296afae1dfef" />

No latches in the path of Y as expected. 

\
Design: bad_case.v

RTL SIM

<img width="964" height="232" alt="image" src="https://github.com/user-attachments/assets/2b24216e-fd33-4602-b92e-28e110c94a92" />

Note that when select is 11, the output does not follow the inputs but stays constant at 1

GLS

<img width="1465" height="189" alt="image" src="https://github.com/user-attachments/assets/e3906ca7-9e3a-4bb4-9db8-78a516ce3310" />

Waveforms from GLS look correct but we see a functional mismatch w/ RTL. 

\
Design: mux_generate.v

Designer Expectation

<img width="866" height="359" alt="image" src="https://github.com/user-attachments/assets/316f6bee-64d1-41d9-a880-87fff4b5d15b" />

RTL SIM
<img width="1637" height="235" alt="image" src="https://github.com/user-attachments/assets/33918443-e7f8-4c04-a46b-c632d24a40c6" />

Schematic

<img width="850" height="593" alt="image" src="https://github.com/user-attachments/assets/41760061-79ce-4db8-a26c-78297aae1970" />

Waveforms based on the above schematic matches 1:1 w/ RTL.

\
Design: demux_generate.v

RTL SIM

<img width="968" height="345" alt="image" src="https://github.com/user-attachments/assets/9028776d-f3ac-4861-a703-d80d71c9447d" />

There is also a demux_case.v. One can easily prove that the waveforms from both these designs are 1:1. As you can guess, one is more elegant than the other. 

\
Design: fa.v, rca.v (full_adder, ripple_carry_adder)

Script for RTL SIM

<img width="355" height="100" alt="image" src="https://github.com/user-attachments/assets/509e69d2-86a2-4055-9acd-a943e96474b9" />

\
RTL SIM

<img width="967" height="193" alt="image" src="https://github.com/user-attachments/assets/9eea9f52-fa5b-474f-bf40-f5e8445bcda4" />

\
Script for Synthesis

<img width="591" height="159" alt="image" src="https://github.com/user-attachments/assets/51548336-123d-42d7-881a-be75251c5573" />

\
Schematic

<img width="952" height="816" alt="image" src="https://github.com/user-attachments/assets/fc280ff5-a639-44ae-a255-f85576cf667e" />

Waveforms based on the above schematic matches 1:1 w/ RTL.

---








