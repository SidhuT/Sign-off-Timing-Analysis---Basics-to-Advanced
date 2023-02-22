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

*•	‘ls’ – shows it.*

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

*•	“leafpad simple.sdc” – Design Constraints file

*•	“leafpad run.tcl” – Commands file to run in openSTA tool

*•	“leafpad run.log” – Opens Log file

*•	“sta run.tcl -exit | tee run.log” -- to run the program*



<img width="800" alt="run_log_1" src="https://user-images.githubusercontent.com/125822919/220407405-2cac5241-cdbe-4d10-859b-6bf1b29db761.png">

<img width="800" alt="run_log_2" src="https://user-images.githubusercontent.com/125822919/220407416-4d06ab9c-64c7-456b-8ed2-08d50839c8a4.png">

<img width="800" alt="run_tcl" src="https://user-images.githubusercontent.com/125822919/220407421-be2c83ab-d8a2-404c-b256-e32ca690fe21.png">

<img width="800" alt="simple_sdc" src="https://user-images.githubusercontent.com/125822919/220407424-6fe525c9-506a-42ed-921c-c25109c181a2.png">

<img width="800" alt="Simple_v" src="https://user-images.githubusercontent.com/125822919/220407430-fbb6ec1e-b881-4f90-9ce0-376510b1d8ea.png">

<img width="800" alt="terminal_1" src="https://user-images.githubusercontent.com/125822919/220407432-ee614873-1219-46ef-a4b9-9f851f7f2cc7.png"><img width="800" alt="terminal_2" src="https://user-images.githubusercontent.com/125822919/220407438-15aaafd4-bca7-4d78-bd2d-57d5e06f0601.png">

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
