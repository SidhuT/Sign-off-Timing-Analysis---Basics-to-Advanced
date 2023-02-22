# **Sign-off-Timing-Analysis - Basics-to-Advanced**
5- day workshop where I covered all the basic concepts in STA and Timing constraints.
Static timing analysis (STA) is a method of validating the timing performance of a design by checking all possible paths for timing violations. STA breaks a design down into timing paths, calculates the signal propagation delay along each path, and checks for violations of timing constraints inside the design and at the input/output interface.

In theworkshop, we covered all the basic concepts in STA and Timing constraints. It started with basics of Static Timing Analysis, timing paths, startpoint, endpoint and combinational logic definitions. It explainsed setup and hold checks, how STA tools calculate setup and hold violations. Then it covered all aspects of STA like multiple types of timing paths, design rule checks, checks on async pins and clock gates. Then we go into slightly advanced topics like Time borrowing on latches, timing arcs, cell delays and models, impact of clock network on STA. Since STA and timing constraints go hand in hand the workshop covered basics of all the timing constraints that an engineer should know for STA like clock definitions, clock groups, clock characteristics, port delays and timing exceptions. Each day of the workshop we applied the concepts that I have leant that day on practical examples.

### Tool - OpenSTA

## **DAY 1**

Studied topics like STA definition, timing paths, timing path elements, setup and hold checks, slack calculation, SDC overview, Clocks, generated clocks and boundary constraints.
### *LAB 1*

#### **OpenSTA (Static Timing Analysis tool) : Introduction**
OpenSTA is a gate level static timing verifier. As a stand-alone executable it can be used to verify the timing of a design using standard file formats.

• Verilognetlist

• Libertylibrary

• SDCtimingconstraints 

• SDFdelayannotation 

• SPEFparasitics

OpenSTA is architected to be easily bolted on to other tools as a timing engine. By using a network adapter, OpenSTA can access the host netlist data structures without duplicating them. An STA tool takes design, standard cell, constraints as input and performtiming checks on the design, delay calculation and analysis.

## Below instructions are used to complete the lab

*•	‘git clone https://github.com/vikisachdeva/openSTA_sta_workshop’ – adding files from Github*

*•	Type ‘ls’ – shows added files.*

*•	‘cd openSTA_sta_workshop’ – opens file.*

*•	Tpye ‘ls’ to open respective file*

*•	Enter ‘cd vlsideepdive_openSTA_labs’*

*•	Type ‘ls’*

*•	“lab1 lab2 lab3 lab4 lab5 lab6 lab7 sky130_fd_sc_hd_tt_025C_1v80.lib”*

*•	‘cd lab1’*

*•	‘ls’*

*•	“run.log run.tcl simple.sdc simple.v”

*•	To view files, enter “leafpad (FILE NAME WITH EXTENSION)”*

*•	“leafpad simple.v” -- Design in Verilog format

<img width="800" alt="Simple_v" src="https://user-images.githubusercontent.com/125822919/220534603-48be62a5-56a3-43ad-ae1d-30f6b81d08e0.png">

*•	“leafpad simple.sdc” – Design Constraints file

<img width="800" alt="simple_sdc" src="https://user-images.githubusercontent.com/125822919/220534659-2dbe845e-ee69-4a47-a500-e9c416684c30.png">

*•	“leafpad run.tcl” – Commands file to run in openSTA tool

<img width="800" alt="run_tcl" src="https://user-images.githubusercontent.com/125822919/220534714-f35c58cb-72ef-40e5-8e6e-d2d38a41470e.png">

*•	“sta run.tcl -exit | tee run.log” -- to run the program*

<img width="800" alt="terminal_1" src="https://user-images.githubusercontent.com/125822919/220534789-c6af8b70-425d-49a5-a098-576ea633e048.png">
<img width="800" alt="terminal_2" src="https://user-images.githubusercontent.com/125822919/220534799-b7e9c2ee-fc75-457d-8359-c712b2a7036f.png">

*•	“leafpad run.log” – Opens Log file

<img width="800" alt="run_log_1" src="https://user-images.githubusercontent.com/125822919/220534836-dc8202a4-ad0b-4c3a-b56b-4a0a1ca70ff9.png">
<img width="800" alt="run_log_2" src="https://user-images.githubusercontent.com/125822919/220534842-ffae7a6b-1397-465e-8b35-2d5298cc3d4a.png">


## **DAY 2**
### *LAB 2*


## **DAY 3**
### *LAB 3*


## **DAY 4**
### **LAB 6 & Lab 7**



## **DAY 5**
### *LAB 4*



## Instructor
Vikas Sachdeva - semiconductor design professional with more than 17 years of experience in the VLSI Industry and also working as an Advisor, Tech and VLSI Coach and Trainer for vlsideepdive in his spare time.
