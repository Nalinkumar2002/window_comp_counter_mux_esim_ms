</br>

<div align="center">
  
![-------](Images/rainbowline.png)

![logo](Images/logo.png)

![-------](Images/rainbowline.png)

</br>


![Size](https://img.shields.io/github/repo-size/Nalinkumar2002/window_comp_counter_mux_esim_ms?color=red)
![Last Commit](https://img.shields.io/github/last-commit/Nalinkumar2002/window_comp_counter_mux_esim_ms?color=green)
![tool](https://img.shields.io/badge/Tool-eSim-28A745)


</div>

</br>

# 📚 Window Comparator Along With MOD-16 Counter For Counting Based Data Line Selection Operation


This repository gives a detailed report on the design of a Window Comparator Along With MOD-16 Counter For Counting Based Data Line Selection Operation using open-source EDA tools. The simulation being carried out is in mixed-mode (i.e.) both analog and digital simulation. Later the obtained simulation, is verified for it's correctness and functionality.

<br>

<p align="center">
  <img src="https://github.com/Nalinkumar2002/barrel_shifter_snps_cc/blob/main/Images/bs_logo.gif">
</p>

<br>

# 📑 Table of Contents

* [Introduction](#-Introduction) 
* [8x4 Right Barrel Shifter](#-8x4-Right-Barrel-Shifter) 
    * [Circuit Schematic](#-Circuit-Schematic) 
    * [Truth Table for Control Shift Bits in 8 × 4 Barrel Shifter](#-Truth-Table-for-Control-Shift-Bits-in-8-×-4-Barrel-Shifter) 
    * [Circuit Output Waveforms](#-Circuit-Output-Waveforms) 
* [Software Tools Used](#-Software-Tools-Used) 
* [Synopsis Custom Compiler Platform](#-Synopsis-Custom-Compiler-Platform) 
* [Implemented Circuit Design using Synopsis](#-Implemented-Circuit-Design-using-Synopsis) 
    * [Schematics](#-Schematics) 
    * [Symbol](#-Symbol) 
    * [Testbench Design](#-Testbench-Design) 
* [Resultant Waveforms](#-Resultant-Waveforms) 
* [Resultant Waveforms For Different Control Shift Input](#-Resultant-Waveforms-For-Different-Control-Shift-Input) 
* [Author](#-Author)
* [Acknowledgements](#-Acknowledgements)
* [References](#-References)


<br>

# 📝 Introduction

Window comparator is a circuit which uses the two comparator in parallel to determine if a signal is between tworeference voltages. If the input signal is outside of the window, the output is Low. If the input signal is within the window, the output is High. A MOD-16 counter has 16 states in its count sequence and used for counting operation. A 16x1 Multiplexer is also used in this design for data selection operation. In this paper, a window comparator along with mod-16 counter followed by 16x1 multiplexer is designed and output waveforms are plotted. This design can be used for two reference voltages based comparing followed by counting based data line selection applications.

 
 </br>

*[Back To Top](#-Table-of-Contents)* ⤴️ 

</br>

# 📝 Window Comparator Along With MOD-16 Counter and 16x1 Mux


The Operational amplifier also known as Op-Amp which are mainly used for mathematical operations like addition, subtraction, integration, differentiation and so on. An Op-Amp
based comparator is used for comparing analogue voltage level with another reference voltage VREF and produce an output signal based on the magnitudes of two input voltages. If the given analog voltage is greater than the reference voltage, the output of comparator is `+VCC` . If the given analog voltage is lower than reference voltage, the output of comparator is `-VCC` . A window comparator is a circuit consists of two Op-Amp in parallel which can take two reference voltages VH and VL and an input analog voltage and produces output based on the comparison of voltages. If the given input voltage lies between two reference voltages, then the output of comparator is `’HIGH’`. Otherwise, the output of comparator is `’LOW’`. This output is given to a MOD-16 counter. MOD-16 counter is also called as 4 bit counter, which have 16 states and count from `’0000’` to `’1111’`. After reaching `’1111’` state it reset to ’0000’ state. The output of comparator is given to 16x1 multiplexer. Multiplexer is a combinational circuit which has maximum of 2n data inputs, `‘n’` selection lines and single output line. Among these data inputs only one will be connected to the output based on the select line values. So, a `16x1` mux have `16` data input lines, `4` select lines and one output line. The output of the `MOD-16` counter is given as input to the `4` select lines of the multiplexer. So, based on the count of counter the corresponding data line is connected to the output line.




# 📝 Software Tools Used

<br>

🌟 eSim 

  * eSim is a free and open-sourced EDA tool for circuit design, simulation, analysis and PCB design. It is an integrated tool built using free/libre and open source software such as KiCad, Ngspice, Verilator, makerchip-app, sandpiper-saas and GHDL. eSim is released under GPL.
  
   🔗 https://esim.fossee.in/home


🌟 KiCad

 * KiCad's Schematic Editor supports everything from the most basic schematic to a complex hierarchical design with hundreds of sheets. It helps to create our own custom symbols or use some of the thousands found in the official KiCad library. We can verify our design with integrated SPICE simulator and electrical rules checker.
    
   🔗 https://www.kicad.org/

🌟 Ngspice

 *  Ngspice is a mixed-level/mixed-signal electronic circuit simulator. Ngspice implements three classes of analysis: nonlinear DC analyses, Nonlinear transient analyses, linear AC analyses.

   🔗 http://ngspice.sourceforge.net/
   
🌟 Verilator

 *  Verilator is a free and open-source software tool which converts Verilog code to a cycle-accurate behavioral model in C++ or SystemC.

   🔗 https://www.veripool.org/verilator/
   
🌟 Makerchip

 *  A web-based IDE that is used to design and simulate digital circuits using Verilog, and the language extension of Verilog, TL-Verilog.

   🔗   https://www.makerchip.com/
   
   
   
 

</br>

*[Back To Top](#-Table-of-Contents)* ⤴️ 

</br>


# 📝 Implemented Circuit Design using eSim

## 📋 Schematics

Schematic designed for window comparator

![bssch](Images/sch3.png)

Schematic designed for astable multivibrator

![bssch](Images/sch2.png)

Schematic designed for 4-bit counter and 16x1 mux 

![bssch](Images/sch4.png)

Complete Schematic design

![bssch](Images/sch1.png)


# 📝 Resultant Waveforms

Resultant waveform of window comparator

![bstbout](Images/o2.png)

Resultant waveform of Window Comparator Along With MOD-16 Counter and 16x1 Mux

![bstbout](Images/o4.png)


</br>

*[Back To Top](#-Table-of-Contents)* ⤴️ 

</br>

# 📝 Netlist

The Netlist for the designed circuit is generated after simulating the circuit.

```
*  Generated for: PrimeSim
*  Design library name: barrel_shifter
*  Design cell name: 8x4_barrel_shifter_tb
*  Design view name: schematic
.lib 'saed32nm.lib' TT

*Custom Compiler Version S-2021.09
*Sat Feb 26 14:03:55 2022

.global gnd!
********************************************************************************
* Library          : barrel_shifter
* Cell             : 8x4_barrel_shifter
* View             : schematic
* View Search List : hspice hspiceD schematic spice veriloga
* View Stop List   : hspice hspiceD
********************************************************************************
.subckt _8x4_barrel_shifter in0 in1 in2 in3 in4 in5 in6 in7 out0 out1 out2 out3
+ sh0 sh1 sh2 sh3 sh4
xm30 out3 sh4 in7 gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm29 out3 sh0 in3 gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm28 out3 sh1 in4 gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm27 out3 sh2 in5 gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm26 out3 sh3 in6 gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm25 out2 sh4 in6 gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm24 out2 sh3 in5 gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm22 out1 sh4 in5 gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm15 out1 sh1 in2 gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm13 out0 sh4 in4 gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm20 out2 sh1 in3 gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm19 out2 sh0 in2 gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm18 out1 sh3 in4 gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm17 out1 sh2 in3 gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm16 out1 sh0 in1 gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm21 out2 sh2 in4 gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm3 out0 sh2 in2 gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm2 out0 sh1 in1 gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm1 out0 sh0 in0 gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm4 out0 sh3 in3 gnd! n105 w=0.1u l=0.03u nf=1 m=1
.ends _8x4_barrel_shifter

********************************************************************************
* Library          : barrel_shifter
* Cell             : 8x4_barrel_shifter_tb
* View             : schematic
* View Search List : hspice hspiceD schematic spice veriloga
* View Stop List   : hspice hspiceD
********************************************************************************
xi0 in0 in1 in2 in3 in4 in5 in6 in7 out0 out1 out2 out3 sh0 sh1 sh2 sh3 sh4
+ _8x4_barrel_shifter
v8 in0 gnd! dc=0 pulse ( 0 1.05 4m 200p 200p 10m 20m )
v7 in1 gnd! dc=0 pulse ( 0 1.05 8m 200p 200p 10m 20m )
v6 in2 gnd! dc=0 pulse ( 0 1.05 12m 200p 200p 10m 20m )
v5 in3 gnd! dc=0 pulse ( 0 1.05 16m 200p 200p 10m 20m )
v4 in4 gnd! dc=0 pulse ( 0 1.05 20m 200p 200p 10m 20m )
v3 in5 gnd! dc=0 pulse ( 0 1.05 24m 200p 200p 10m 20m )
v2 in6 gnd! dc=0 pulse ( 0 1.05 28m 200p 200p 10m 20m )
v1 in7 gnd! dc=0 pulse ( 0 1.05 32m 200p 200p 10m 20m )
c30 out2 gnd! c=1p
c29 out3 gnd! c=1p
c28 out1 gnd! c=1p
c27 out0 gnd! c=1p
v35 sh0 gnd! dc=0
v36 sh1 gnd! dc=0
v37 sh3 gnd! dc=0
v39 sh2 gnd! dc=0
v38 sh4 gnd! dc=1.05



.tran '0.001*(50m-0)' '50m' name=tran

.option primesim_remove_probe_prefix = 0
.probe v(*) i(*) level=1
.probe tran v(in0) v(in1) v(in2) v(in3) v(in4) v(in5) v(in6) v(in7) v(out0)
+ v(out1) v(out2) v(out3)

.temp 25


.option primesim_output=wdf


.option parhier = LOCAL



.end

```
</br>

*[Back To Top](#-Table-of-Contents)* ⤴️ 

</br>

# 🚶 Run this project 

1. Clone this repository locally 
```
git clone https://github.com/Nalinkumar2002/window_comp_counter_mux_esim_ms.git
```
2. Go to *nali_win_comp_count_mux* directory
```
cd nali_win_comp_count_mux
```
3. Run NgSpice
```
ngspice nali_win_comp_count_mux.cir.out
```

# 📜 Author
 
 🖊️ Nalinkumar S, Pre-Final year student, B.E. ECE, Madras Institute of Technology, Anna University, Chennai, India
 
 
# 🎓 Acknowledgements

 📖 Kunal Ghosh, Co-Founder of VLSI System Design (VSD) Corp. Pvt. Ltd. - kunalpghosh@gmail.com
 
 📖 Sumanto Kar, eSim Team, FOSSEE
 
 📖 Steve Hoover, Founder, Redwood EDA
 
 📖 FOSSEE, IIT Bombay

# 🔍 References

📔 Laknaur, R. Xiao, S. Durbha and H. Wang, ”Design of a Window Comparator with Adaptive Error Threshold for Online Testing Applications,”
8th International Symposium on Quality Electronic Design (ISQED’07),
2007.

📔  R. Singh and K. S. Pande, ”4-bit Counter Using High-Speed Low-Voltage
CML D-Flipflops,” 2018 3rd International Conference on Communication
and Electronics Systems (ICCES), 2018.

📔  J. Park, J. Song, S. Lim and S. Kim, ”A high speed and low power
41 multiplexer with cascoded clock control,” 2010 IEEE Asia Pacific
Conference on Circuits and Systems, 2010.
