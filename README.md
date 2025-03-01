# Differential Amplifier

A **differential amplifier** is a type of electronic amplifier that amplifies the difference between two input voltages but suppresses any voltage common to the two inputs.It is an analog circuit with two inputs Vin- and Vin+ and one output Vout, in which the output is ideally proportional to the difference between the two voltages:

![image](https://github.com/user-attachments/assets/fbd3352d-99e1-4286-9137-79cd83cc1df4)

**Vout = A [(Vin+)−(Vin-)]**
<br>        where , A is the gain of the amplifier.

**Adiff = gm × RD**
 
### Why differential amplifier is more efficient than mosfet ?
A differential amplifier is considered considerably more efficient than a single MOSFET because it has a superior ability to reject common-mode noise, increasing only the difference between two input signals while thoroughly filtering out any noise on both inputs; a single MOSFET would increase the desired signal and any common-mode noise on the input, making the differential amplifier ideal for sensitive applications where noise reduction is important. And also differential configuration enables us to bias the amplifier and to couple amplifier stages together without the need for bypass and coupling capacitor.

### Types of operation
#### 1.Commom mode operation  
<p>When the same voltage is applied to both input terminals, it is considered a common-mode signal. In an ideal differential amplifier, the output voltage in common mode operation should be zero because the circuit is designed to only respond to the difference between the input signals. 
<p></p> **Common mode rejection ratio (CMRR):**This parameter indicates how well a differential amplifier can suppress common-mode signals, with a higher CMRR signifying better rejection. 

![image](https://github.com/user-attachments/assets/3ac461ca-54dd-4c0f-b0a6-cc3e90dc3a8d)

Range in which common mode differential pair works properly, means both the mosfet Q1 and Q2 are in saturation is 
<p></p><br>           <pre>                        Vcm(max) = Vt + Vdd - (1/2 Rd)
<p></p>                       Vcm(min) = -Vss + Vs + Vt + Vov


</pre>

#### 2.Differential mode operation 
<p>Differential mode operation of a differential amplifier occurs when the two input voltages change in opposite directions. In this mode, the two voltage followers oppose each other, keeping the common emitter point's voltage from changing. 
  
![image](https://github.com/user-attachments/assets/ed5f11f5-b8e6-4351-9220-c8effbf2b6d5)

 <p></p> <pre> I = 1/2*(kn'* W/L)(Vgs1 -Vt)
 </pre> 
 
 <p></p> <pre> The value of Vid at the entire current I is steered into Q1 is
 <p></p>  Vid(max) = Vgs1 + Vs
    </pre> 
    
 <p></p> <pre>  The current I can be steered from one transistor to the other by varying  Vid in the range 
 <p></p> -√2 Vov ≤  Vid  ≤  √2Vov
   </pre> 











