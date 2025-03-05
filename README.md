# Differential-Amplifier
## Introduction
The MOS differential pair is a type of amplifier configuration, which consists of two perfectly matched MOSFETs, with identical source resistances, and matching or common inputs. The output voltage will be
the difference between the two drain source voltages (V<sub>D</sub>) of the MOSFETs. Differential amplifiers consist of two transistors M1 and M2, whose sources are joined together. If the two transistors are connected to different voltage inputs, then the current across M1 and M2 are different due to the gate voltage. If the voltage supply at the gate terminal is the same, then the current through M1 and M2 is also the same. 

## Aim
Design the differential amplifier for the following specifications V<sub>DD</sub> = 2V, P ≤ 1mW, V<sub>iCM</sub> = 1V, V<sub>OCM</sub> = 1.1V, V<sub>p</sub> = 0.4V. Perform DC analysis,transient analysis,frequency response and extract the required parameters.

![image](https://github.com/user-attachments/assets/15cf072c-61f5-47d6-b563-518b3e7d5514)

Calculate the values of R<sub>SS</sub>, R<sub>D1</sub>, R<sub>D2</sub>.

Given:<br>
V<sub>DD</sub> = 2V<br>
P ≤ 1mW<br>
V<sub>iCM</sub> = 1V<br>
V<sub>OCM</sub> = 1.1V<br>
V<sub>p</sub> = 0.4V<br>

P = 1mW = V<sub>DD</sub> x I<sub>SS</sub> = 2 x I<sub>SS</sub>

I<sub>SS</sub> = 1mW / 2V = 0.5mA

I<sub>D1</sub> = I<sub>D2</sub> = I<sub>SS</sub>/2 = 0.25mA

R<sub>D</sub> = (V<sub>DD</sub> - V<sub>OCM</sub>)/I<sub>D1</sub><br>
              = (2 – 1.1) V / 0.25mA<br>
              = 3.6KΩ<br> 

R<sub>SS</sub> = V<sub>p</sub> / I<sub>SS</sub><br>
               = 0.4 V / 0.5mA <br>
               = 0.8KΩ<br>


From our analysis, we have now calculated the values –

I<sub>SS</sub> = 0.5mA

R<sub>D</sub> = 3.6KΩ

R<sub>SS</sub> = 0.8KΩ


