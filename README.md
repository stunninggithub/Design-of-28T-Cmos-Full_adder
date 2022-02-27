# Design-of-28T-Cmos-Full_adder
This Repository represents the design and implementation of 28T  Full adder using Synopsis custom compiler based on 28nm Cmos Technology.
## Table of contents 
  * [Abstract](#abstract)
  * [Reference Circuit Details](#reference_circuit_details)
  * [Reference Circuit Diagram](#refernce_circuit_diagram)
  * [Reference Circuit Waveform](#reference_circuit_waveform)
  * [Desirable Truth Table](#desirable_truth_table)
  * [Tools Used](#tools-used)
- [Simulation in Synopsys](#simulation-in-synopsys)
  * [Full_Adder_Block](#full-adder-block)
  * [Parameters set for Voltage Source for Input A](#parameters-set-for-voltage-source-for-input-a)
  * [Parameters set for Voltage Source for Input B](#parameters-set-for-voltage-source-for-input-b)
  * [Parameters set for Voltage Source for Input Cin](#parameters-set-for-voltage-source-for-input-cin)
  * [Transient Settings](#transient-settings)
  * [Output Waveform](#output-waveform)
  * [Netlist](#netlist)
  * [Conclusion](#conclusion)
  * [Author](#author)
  * [Acknowledgement](#acknowlegement)
  * [References](#references)
## Abstract
In this,I design full_adder circuit Using Cmos 28nm Technology. Design and Implementation will be done using Esim Software. Full adder is the functional building block and basic component in several architectures found in VLSI and DSP applications, Adder is a versatile component and mainly used in addition and multiplication as the basic processing element; Adder in a VLSI application is used in ALU design, Address generation in processors, Multipliers and so on. In DSP applications it is used code for conversion, Signed addition and Signed multiplication,Transformations and signal processing applications. This defines the need and importance of designing an adder block in effective way
## Reference Circuit Diagram 
Conventional CMOS Full Adder is the most basic full adder implementation techniques. Conventional CMOS Full Adder consists of 28 transistors. A, B and Cin are the inputs and Sum & Cout are the outputs.Full adder adds the incoming inputs and gives the result along with a carry.A full adder contains two half adders which are being connected to input A and B of one-half adder and other is being connected to sum (output)which have the one input as Cin and other is the output of XNOR.
The Relations between the inputs and the outputs are expressed as:
          Cout=Cin(A+B)+AB 
          Sum=ABCin+Cout_bar(A+B+Cin) 

## Reference Circuit Diagram
<img width ="1329" alt="Reference_Circuit" src="https://user-images.githubusercontent.com/100271073/155868887-b53607d0-2bf8-4a89-b0e4-01e9d825b7f7.JPG">

## Reference Circuit Waveform
<img width="1156" alt="Reference_waveform" src="https://user-images.githubusercontent.com/100271073/155868939-216e8f82-8717-413f-a29c-d59cc68a8fae.JPG">

## Desirable Truth Table
![Full_adder_Truth_Table](https://user-images.githubusercontent.com/59500283/155389650-b7823b97-2f40-4cf2-bb7a-72e5364af9b2.jpeg)


## Tools Used:
• Synopsys Custom Compiler:
 The Synopsys Custom Compiler™ design environment is a modern solution for full-custom analog, custom digital, and mixed-signal IC design. As the heart of the Synopsys Custom Design Platform, Custom Compiler provides design entry, simulation management and analysis, and custom layout editing features. This tool was used to design the circuit on a transistor level.
 
 ![custom_compiler](https://user-images.githubusercontent.com/59500283/155473715-c6a1fd5b-71c7-4655-936a-5fe3befabfd8.png)


• Synopsys Primewave:
 PrimeWave™ Design Environment is a comprehensive and flexible environment for simulation setup and analysis of analog, RF, mixed-signal design, custom-digital and memory designs within the Synopsys Custom Design Platform. This tool helped in various types of simulations of the above designed circuit.

• Synopsys 28nm PDK:
 The Synopsys 28nm Process Design Kit(PDK) was used in creation and simulation of the above designed circuit.

# Simulation in Synopsys
## Full_Adder_Block
<img width="1440" alt="Full_Adder_Schematic" src="https://user-images.githubusercontent.com/100271073/155869406-965cd3b5-e32b-49f3-91e2-25ece457daeb.png">

<img width="660" alt="Full_Adder_Symbol" src="https://user-images.githubusercontent.com/100271073/155869508-da41764f-81a4-42e1-83ea-d6ddeb9a1f34.png">
<img width=1265" alt="Full_Adder_Testbench" src="https://user-images.githubusercontent.com/100271073/155869571-c367ea61-2709-447f-b8f9-29dac4217985.png">
## Parameters set for Voltage Source for Input A
<img width="346" alt="A_Pulse" src="https://user-images.githubusercontent.com/100271073/155869918-45f335c6-a013-46e5-9786-ec15b6d9e7bc.png">

## Parameters set for Voltage Source for Input B
<img width="367" alt="B_Pulse" src="https://user-images.githubusercontent.com/100271073/155869974-06b89f42-4892-482c-8455-e53adef3e313.png">
## Parameters set for Voltage Source for Input Cin 
<img width="350" alt="Cin_Pulse" src="https://user-images.githubusercontent.com/100271073/155870051-621d173f-6de1-42f4-af30-80fcf67c0667.png">
## Transient Settings
<img width="1326" alt="Transient_Analysis" src="https://user-images.githubusercontent.com/100271073/155870475-db1a4bb8-63c1-439e-985c-38ea3259ba3d.png">

## Output Waveform
<img width="1458" alt="Output_waveform" src="https://user-images.githubusercontent.com/100271073/155870570-f095cfea-d91a-45a6-901b-1f1252a2e977.png">

## Netlist
```

*  Generated for: PrimeSim
*  Design library name: cp_lib1
*  Design cell name: cp_fulladder1_tb
*  Design view name: schematic
.lib 'saed32nm.lib' TT

*Custom Compiler Version S-2021.09
*Sun Feb 27 06:38:54 2022

.global gnd! vdd!
********************************************************************************
* Library          : cp_lib1
* Cell             : cp_fulladder1
* View             : schematic
* View Search List : hspice hspiceD schematic spice veriloga
* View Stop List   : hspice hspiceD
********************************************************************************
.subckt cp_fulladder1 cout d_a d_b d_cin sum vdd vss vt_bulk_n_gnd!
+ vt_bulk_p_vdd!
xm37 sum net68 vss vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm19 net68 net60 net42 vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm18 net68 d_a net55 vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm17 net55 d_b net52 vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm16 net52 d_cin vss vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm15 net42 d_cin vss vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm14 net42 d_b vss vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm13 net42 d_a vss vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm12 cout net60 vss vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm5 net60 d_cin net10 vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm4 net10 d_b vss vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm3 net10 d_a vss vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm2 net60 d_b net5 vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm0 net5 d_a vss vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm28 net85 d_a net107 vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
xm33 net107 d_a vdd vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
xm34 net107 d_b vdd vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
xm35 net107 d_cin vdd vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
xm36 sum net68 vdd vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
xm22 net68 d_cin net67 vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
xm21 net67 d_b net85 vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
xm20 net68 net60 net107 vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
xm11 cout net60 vdd vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
xm10 net29 d_a net28 vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
xm9 net28 d_b vdd vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
xm8 net29 d_cin vdd vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
xm7 net60 d_b net29 vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
xm6 net60 d_a net29 vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
.ends cp_fulladder1

********************************************************************************
* Library          : cp_lib1
* Cell             : cp_fulladder1_tb
* View             : schematic
* View Search List : hspice hspiceD schematic spice veriloga
* View Stop List   : hspice hspiceD
********************************************************************************
xi0 cout d_a d_b d_cin sum net9 gnd! gnd! vdd! cp_fulladder1
v1 net9 gnd! dc=1.8
v18 d_cin gnd! dc=0 pulse ( 0 1.5 0 0.1u 0.1u 15u 20u )
v17 d_b gnd! dc=0 pulse ( 0 1.5 0 0.1u 0.1u 10u 15u )
v3 d_a gnd! dc=0 pulse ( 0 1.5 0 0.1u 0.1u 5u 10u )
c7 cout gnd! c=1p
c6 sum gnd! c=1p


.tran '0.1u' '20u' name=tran

.option primesim_remove_probe_prefix = 0
.probe v(*) i(*) level=1
.probe tran v(cout) v(d_a) v(d_b) v(d_cin) v(sum)

.temp 25



.option primesim_output=wdf


.option parhier = LOCAL



.end

```

## Conclusion
Thus, the addition for a single-bit is achieved using 28T full adder.

## Author
M Kasturi,Sphoorthy Engineering college,Nadargul,Hyderabad.
## Acknowledgement
1. Kunal Ghosh, Co-founder, VSD Corp. Pvt. Ltd. - kunalpghosh@gmail.com
2. Chinmay panda, IIT Hyderabad
3. Sameer Durgoji, NIT Karnataka
4. [Synopsys Team/Company](https://www.synopsys.com/)
5. https://www.iith.ac.in/events/2022/02/15/Cloud-Based-Analog-IC-Design-Hackathon/

## References
[1].http://www.ijatest.org/wp-content/uploads/2017/01/37.FULL-ADDER-USING-CMOS-TECHNOLOGY.pdf
[2].https://dayonmyplate.in/
[3].https://www.youtube.com/watch?v=p4jgNRjwluA

