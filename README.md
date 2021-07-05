# VSD Advanced Physical Design Worshop with sky130nmPDK and OpenLane


Table of contents
=================

<!--ts-->
   * [Day 1](https://github.com/manjunathrv/VSD_RTL_Design_using_sky130nmPDK_workshop#day-1)
      * [Introduction to Physical Design flow](https://github.com/manjunathrv/VSD_RTL_Design_using_sky130nmPDK_workshop#introduction-to-open-source-eda-tools---iverilog-gtkwave-and-yosys)
      * [Introduction to Openlane flow](https://github.com/manjunathrv/VSD_RTL_Design_using_sky130nmPDK_workshop#introduction-to-open-source-eda-tools---iverilog-gtkwave-and-yosys)
      * [Openlane directory structure](https://github.com/manjunathrv/VSD_RTL_Design_using_sky130nmPDK_workshop#introduction-to-open-source-eda-tools---iverilog-gtkwave-and-yosys)
      * [Design prepartion and synthesis flow](https://github.com/manjunathrv/VSD_RTL_Design_using_sky130nmPDK_workshop#introduction-to-open-source-eda-tools---iverilog-gtkwave-and-yosys)
   * [Day 2](https://github.com/manjunathrv/VSD_RTL_Design_using_sky130nmPDK_workshop#day-2)
      * [Introduction to technology library file](https://github.com/manjunathrv/VSD_RTL_Design_using_sky130nmPDK_workshop#1-introduction-to-technology-library-file)
      * [Lab Session 1 - Hierachal and Flatten synthesis](https://github.com/manjunathrv/VSD_RTL_Design_using_sky130nmPDK_workshop#2-lab-session-1---hierachal-and-flatten-synthesis)
      * [Lab Session 2 - Flip-Flop implementation and synthesis](https://github.com/manjunathrv/VSD_RTL_Design_using_sky130nmPDK_workshop#3-lab-session-2---flip-flop-implementation-and-synthesis)
    
   * [Day 3](https://github.com/manjunathrv/VSD_RTL_Design_using_sky130nmPDK_workshop#day-3)
      * [VSD CMOS Inverter Cell](https://github.com/manjunathrv/VSD_RTL_Design_using_sky130nmPDK_workshop#1-introduction-to-optimisation-)
      * [Spice simulation of the VSD CMOS Inverter Cell](https://github.com/manjunathrv/VSD_Advanced_Physical_Design_with_sky130nmPDK#spice-simulation-of-the-vsd-cmos-inverter-cell)

   	
   * [Day 4](https://github.com/manjunathrv/VSD_RTL_Design_using_sky130nmPDK_workshop#day-4)
      * [Verification of Gate level Synthesized (GLS) netlist ](https://github.com/manjunathrv/VSD_RTL_Design_using_sky130nmPDK_workshop#1-verification-of-gate-level-synthesized-gls-netlist-)
      * [Lab Session 1 GLS Synthesis simulation mismatch](https://github.com/manjunathrv/VSD_RTL_Design_using_sky130nmPDK_workshop#2-lab-1-gls-synthesis-simulation-mismatch-)
 
   * [Day 5](https://github.com/manjunathrv/VSD_RTL_Design_using_sky130nmPDK_workshop#day-5)
      * [If - Else statement](https://github.com/manjunathrv/VSD_RTL_Design_using_sky130nmPDK_workshop#1-if---else-statement)
      * [Case structure](https://github.com/manjunathrv/VSD_RTL_Design_using_sky130nmPDK_workshop#2-case-structure)
      * [Lab Session 1 Incomplete If-Else statement](https://github.com/manjunathrv/VSD_RTL_Design_using_sky130nmPDK_workshop#4-lab-session-1-incomplete-if-else-statement)
      * [Lab Session 2 Incomplete Case statement](https://github.com/manjunathrv/VSD_RTL_Design_using_sky130nmPDK_workshop#4-lab-session-2-incomplete-case-statement)
   * [Acknowledgement](https://github.com/manjunathrv/VSD_RTL_Design_using_sky130nmPDK_workshop#acknowledgement)

<!--te-->

# Day 1 

## Introduction to Physical Design flow
## Introduction to Openlane flow
## Openlane directory structure
## Design prepartion and synthesis flow

# Day 2

## Introduction to Physical Design flow
## Introduction to Openlane flow
## Openlane directory structure
## Design prepartion and synthesis flow

# Day 3 

## VSD CMOS Inverter Cell

A schematic of a CMOS inverter is shown in the below figure. <br/> 
<img src="Images/Day_3_Fig.PNG" width="200"> <br/> 
<br/> 
The input to the CMOS inverter is labelled as A and the output is Y.<br/>

The VSD CMOS inverter cell for the lab is taken from the github link <br/>

The CMOS inverter is checked in Magic layout editor using the following commands. <br/>


The image in Magic Layout editor can be centered by pressing v and the top cell is shown by pressing s.<br/> 

The output obtained is shown below.<br/> 

<img src="Images/Day_3_1a.PNG" width="400"> <br/> 
<br/> 
<br/> 
The layer of N-well in the PMOS region can be found by moving the cursor close to the large box surrounding the PMOS layer and typing the command what in the tkon console window as shown below, <br/> 

<img src="Images/Day_3_1b.PNG" width="400"> <br/> 

Similarly, NMOS, PMOS and poly layers of the inverter are found as shown below, <br/> 

<strong>NMOS</strong> <br/> 

<img src="Images/Day_3_1c.PNG" width="400"> <br/> 

<strong>PMOS</strong>

<img src="Images/Day_3_1d.PNG" width="400"> <br/> 
 
 <strong>poly</strong> 
 
<img src="Images/Day_3_1e.PNG" width="400"> <br/> 

## Spice simulation of the VSD CMOS Inverter Cell
### Static simulation of the CMOS Inverter

The circuit for the static simulation of the CMOS inverter is shown below, <br/> 

<img src="Images/Day_3_Fig_2.PNG" width="400"> <br/> 

The typical voltage transfer characteristices for the static simulation of the CMOS inverter is shown below, <br/> 

<img src="Images/Day_3_Fig_3.PNG" width="400">

### Dynamic simulation of the CMOS Inverter

The circuit for the dynamic simulation of the CMOS inverter is shown below, <br/> 

<img src="Images/Day_3_Fig_2.PNG" width="400"> <br/> 

The spice netlist obtained from magic tool is done by using the commands extract all, ext2spice thresh 0 rthresh 0, ext2spice as shown below, <br/> 

<img src="Images/Day_3_1h.PNG" width="400"> <br/> 

The output spice netlist from the CMOS inverter layout is shown below, <br/> 

<img src="Images/Day_3_1i.PNG" width="400"> <br/> 

For dynamic simulation, the netlist is modified as below, <br/>
<img src="Images/Day_3_1j.PNG" width="400"> <br/> 

Next, the spice simulation is done in ngspice by the following commands.<br/> 

<img src="Images/Day_3_1k.PNG" width="400"> <br/> 

<img src="Images/Day_3_1l.PNG" width="400"> <br/> 

The output waveform of the VSD CMOS inverter is shown below, <br/> 

<img src="Images/Day_3_1m.PNG" width="400"> <br/> 

From the CMOS Output waverform, the calculation of rise slew time taken to go from 20% to 80% of the Vout(y) as shown below,  <br/> 
<img src="Images/Day_3_1m.PNG" width="400"> <br/> 

<img src="Images/Day_3_1m.PNG" width="400"> <br/> 

The rise slew time obtained is ps  <br/> 

Similarly, the falling slew time is obtained with the time taken to go from 20% to 80% of the Vout(y) as shown below as shown below,  <br/> 
<img src="Images/Day_3_1m.PNG" width="400"> <br/> 

<img src="Images/Day_3_1m.PNG" width="400"> <br/> 

The fall slew time obtained is ps  <br/> 

In the next step, the rise time and the fall time is calculated. <br/>
The rise taken with the midpoint of the Vin(a) and Vout(y) <br/> 
<img src="Images/Day_3_1m.PNG" width="400"> <br/> 
<img src="Images/Day_3_1m.PNG" width="400"> <br/> 
The fall slew time obtained is ps  <br/>

The fall taken with the midpoint of the Vin(a) and Vout(y) <br/> 
<img src="Images/Day_3_1m.PNG" width="400"> <br/> 
<img src="Images/Day_3_1m.PNG" width="400"> <br/> 
The fall slew time obtained is ps  <br/>











## Introduction to Openlane flow
## Openlane directory structure
## Design prepartion and synthesis flow

# Day 4 

## Introduction to Physical Design flow
## Introduction to Openlane flow
## Openlane directory structure
## Design prepartion and synthesis flow

# Day 5 

## Introduction to Physical Design flow
## Introduction to Openlane flow
## Openlane directory structure
## Design prepartion and synthesis flow



