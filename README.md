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

# Circuit 1
## DC Analysis
**Procedure**: Design Rd and Rss.Observe Vocm, Vp. Justify the results.

![image](https://github.com/user-attachments/assets/4603418b-2566-4f86-9473-f3cc7dc191ad)

![image](https://github.com/user-attachments/assets/bd3603d0-497a-48cd-ad19-b8d21a9cf21c)

Here in dc analysis we got the Vout as expected and Id1 and Id2 we got the same for the Width value 19.3um and Length value 180nm.

## Transient analysis:
**Procedure**: To perform transient analysis we have to select the transient analysis in the edit simulation and give the stop time as 5ms and run the simulation.

![image](https://github.com/user-attachments/assets/62374293-9027-430f-a04b-873ba4105f77)

Voltage gain,AV = Voutp-p/Vinp-p<br>
AV=(1.18-1.001)/(1.05-0.95)<br>
AV=1.8<br>

## AC Analysis

![image](https://github.com/user-attachments/assets/0159c8b4-148e-4732-80aa-c24c11c39a42)

Gain in dB= 20log(AV)<br>
         =20log(1.8)<br>
         =5.105dB<br>

# Circuit 2 
Now replace the resistor Rss with a current source Iss = 0.5mA.

![image](https://github.com/user-attachments/assets/92bbed5a-c9ab-4883-95d8-ae026084c12d)


## DC Analysis
To perform the DC analysis we have to select the {DC op pnt} in the edit simulation command and run the simulation the figure below is the values obtained from the DC analysis

![image](https://github.com/user-attachments/assets/ed082fbb-411a-40b9-8a4b-c9f9b51f128a)

Width = 19.3um ; Length = 180nm
We obtained the required Iss value of 0.5mA for the above mentioned W/L values.

## Transient Analysis
**Procedure**: Set 180degree and AC amplitude 0 for one mosfet and 0degree and AC amplitude 1 for another circuit.

![image](https://github.com/user-attachments/assets/bfb3c9d4-7aa7-4294-a5c7-3d15badafe33)

Voltage gain,AV = Voutp-p/Vinp-p<br>
AV=(1.53-0.64)/(1.04-0.95)<br>
AV=9.8<br>

## AC Analysis

![image](https://github.com/user-attachments/assets/f684391a-a3dc-4bc3-ac6c-4e0316a28e58)

Gain in dB= 20log(AV)<br>
         =20log(9.8)<br>
         =19.82dB<br>
         
# Circuit 3
Now replace the R3 resister with a Mosfet.

![image](https://github.com/user-attachments/assets/5e636b77-7392-4d27-a6fc-d51c4e7d9f6f)

## Inference

From the above experiment we observed the three different configurations for the differential amplifier, i.e., with resistance RSS, current source ISS, the NMOS biased as a current source operating in saturation region.
1. With resistor:We observed low CMRR(Common-Mode Rejection Ratio) and high bandwidth and also it provides negative feedback.It also has reduced gain voltage.
2. With Current source: We observed high CMRR and low bandwidth compared to that of with the resistor and has high gain voltage.
3. With Mosfet: The highest gain we observed was in this compared to the other two configurations. However, the frequency response for this configuration seems very unstable, with constant fluctuations before the midband.




















