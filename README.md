# Differential Amplifier

A **differential amplifier** is a type of electronic amplifier that amplifies the difference between two input voltages but suppresses any voltage common to the two inputs.It is an analog circuit with two inputs Vin- and Vin+ and one output Vout, in which the output is ideally proportional to the difference between the two voltages:

![image](https://github.com/user-attachments/assets/fbd3352d-99e1-4286-9137-79cd83cc1df4)

 <pre>                  
                        Vout = A [(Vin+)−(Vin-)]
<br>                       where , A is the gain of the amplifier.

                        Adiff = gm × RD
                           where , gm = Transconductance 
                                   RD = Drain resistance
 </pre>
 
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
                          Vid(max) = Vgs1 + Vs
    </pre> 
    
 <p></p> <pre>  The current I can be steered from one transistor to the other by varying  Vid in the range 
                                 -√2 Vov ≤  Vid  ≤  √2Vov
   </pre> 

 ## Experiment 
**Aim :** Design and analyse the mos differential amplifier circuit for the following specification. 
<pre> VDD = 3.2 V ; P ≤ 2.8 mW  ; Vicm = 1.6 V  ; Vocm = 1.7 V ; Vp = 0.6 V  </pre>
Perform DC analysis ,transient analysis and frequency response and extract the required parameter .

![image](https://github.com/user-attachments/assets/b8017d40-dae2-4f17-bb25-4938ad6f5bf9)

<pre> 
         Power (P) = voltage (V) / current (I)

          Iss = P / V 
              = 2.8*10^-3 / 3.2
              = 0.875*10^-3 A

       Ohm's Law,
          Vss = Iss * Rss
         
          Rss = V / I
              = 0.6 / 0.875*10^-3
              = 685.71 Ω

          RD = ( Vdd - Vocm )/ ( Iss/2 )
             = ( 3.2 -1.7 )/ (0.825*10^-3/2)
             = 3.428k Ω 
</pre>

**Procedure :**

• Make the circuit connection.

• Connect resistor RD(3.428k ohms) to the drain of the mosfet , voltage source of 1.6V at gate of mosfet  and source of mosfet is grounded  .

• Apply voltage source of VDD(3.2V) to the resistor RD.

• Perform DC analysis, Transient analysis and AC analysis by giving a sine wave to the voltage source at gate .

1) DC Analysis :
   Select the dc output point(DC op pnt) in Simulation command and then Run.
2) Transient Analysis:
   Select the Transient analysis in Simulation ,  Give the stop time as 5 ms and then Run. Put value of V2 voltage 
   source at gate as sine wave of DC offset 1.6 v, amplitude as 50m and frequency 1k Hz.
3) AC Analysis:
   Select the ac analysis in configure analysis inside  Simulation ,with decade as type of sweep , number of points as 20 , start frequency 0.1Hz and stop frequency 1T Hz and then Run.

## Observation

### Circuit 1

 ![image](https://github.com/user-attachments/assets/594d7258-e18b-489c-97f0-1cc445cd34b9)

**1) DC Analysis :**
 
 ![image](https://github.com/user-attachments/assets/7621b1ef-1738-46bb-b269-d6a9ed9448f1)

![image](https://github.com/user-attachments/assets/48e295a9-7f8b-458e-beec-dee7bc117056)

**2) Transient Analysis:**

![image](https://github.com/user-attachments/assets/dba6cc4e-dfd5-486d-98e0-309fe93a7f21)

<pre>
     Vin p-p = 1.6484 - 1.5515
             = 0.0969 V
     Vout p-p = 1.7680-1.6329
              = 0.1351 V

     Av =  Vout p-p / Vin p-p
        = 0.1351 / 0.0969
        = 1.3942

     Av (dB) = 20 log(1.3942) = 2.8866
 
</pre>

#missing swing 

**3) AC Analysis:**

![image](https://github.com/user-attachments/assets/92523cd1-9a9a-492a-bf67-5f09b7bad7bd)

<pre>
      Av = 2.885 dB
</pre>













  




