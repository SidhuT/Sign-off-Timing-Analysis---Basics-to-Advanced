# **[Sign-off-Timing-Analysis - Basics-to-Advanced](https://github.com/SidhuT/Sign-off-Timing-Analysis---Basics-to-Advanced)**

5- day workshop where I covered all the basic concepts in STA and Timing constraints.
Static timing analysis (STA) is a method of validating the timing performance of a design by checking all possible paths for timing violations. STA breaks a design down into timing paths, calculates the signal propagation delay along each path, and checks for violations of timing constraints inside the design and at the input/output interface.

In theworkshop, we covered all the basic concepts in STA and Timing constraints. It started with basics of Static Timing Analysis, timing paths, startpoint, endpoint and combinational logic definitions. It explainsed setup and hold checks, how STA tools calculate setup and hold violations. Then it covered all aspects of STA like multiple types of timing paths, design rule checks, checks on async pins and clock gates. Then we go into slightly advanced topics like Time borrowing on latches, timing arcs, cell delays and models, impact of clock network on STA. Since STA and timing constraints go hand in hand the workshop covered basics of all the timing constraints that an engineer should know for STA like clock definitions, clock groups, clock characteristics, port delays and timing exceptions. Each day of the workshop we applied the concepts that I have leant that day on practical examples.

## Tool - OpenSTA
   [DAY 1](https://github.com/SidhuT/Sign-off-Timing-Analysis---Basics-to-Advanced/blob/main/README.md#day-1)
   
   [DAY 2](https://github.com/SidhuT/Sign-off-Timing-Analysis---Basics-to-Advanced/blob/main/README.md#day-2)
   
   [DAY 3](https://github.com/SidhuT/Sign-off-Timing-Analysis---Basics-to-Advanced/blob/main/README.md#day-3)
   
   

# **[DAY 1](https://github.com/SidhuT/Sign-off-Timing-Analysis---Basics-to-Advanced/blob/main/README.md#day-1)**

Studied topics like STA definition, timing paths, timing path elements, setup and hold checks, slack calculation, SDC overview, Clocks, generated clocks and boundary constraints.

## *LAB 1 - Opensta Introduction, Inputs to Opensta, Constraints creation and Opensta Runscript*

#### **OpenSTA (Static Timing Analysis tool) : Introduction**
OpenSTA is a gate level static timing verifier. As a stand-alone executable it can be used to verify the timing of a design using standard file formats.

• Verilognetlist

• Libertylibrary

• SDCtimingconstraints 

• SDFdelayannotation 

• SPEFparasitics

OpenSTA is architected to be easily bolted on to other tools as a timing engine. By using a network adapter, OpenSTA can access the host netlist data structures without duplicating them. An STA tool takes design, standard cell, constraints as input and performtiming checks on the design, delay calculation and analysis.

### Below instructions are used to complete the lab

*•	‘git clone https://github.com/vikisachdeva/openSTA_sta_workshop’ – adding files from Github*

*•	Type ‘ls’ – shows added files.*

*•	‘cd openSTA_sta_workshop’ – opens file.*

*•	Tpye ‘ls’ to open respective file*

*•	Enter ‘cd vlsideepdive_openSTA_labs’*

*•	Type ‘ls’*

*•	“lab1 lab2 lab3 lab4 lab5 lab6 lab7 sky130_fd_sc_hd_tt_025C_1v80.lib”*

*•	‘cd lab1’*

*•	‘ls’*

*•	“run.log run.tcl simple.sdc simple.v”*

*•	To view files, enter “leafpad (FILE NAME WITH EXTENSION)”*

*•	“leafpad simple.v” -- Design in Verilog format*

<img width="800" alt="Simple_v" src="https://user-images.githubusercontent.com/125822919/220534603-48be62a5-56a3-43ad-ae1d-30f6b81d08e0.png">

*•	“leafpad simple.sdc” – Design Constraints file*

<img width="800" alt="simple_sdc" src="https://user-images.githubusercontent.com/125822919/220534659-2dbe845e-ee69-4a47-a500-e9c416684c30.png">

*•	“leafpad run.tcl” – Commands file to run in openSTA tool*

<img width="800" alt="run_tcl" src="https://user-images.githubusercontent.com/125822919/220534714-f35c58cb-72ef-40e5-8e6e-d2d38a41470e.png">

*•	“sta run.tcl -exit | tee run.log” -- to run the program*

<img width="800" alt="terminal_1" src="https://user-images.githubusercontent.com/125822919/220534789-c6af8b70-425d-49a5-a098-576ea633e048.png">
<img width="800" alt="terminal_2" src="https://user-images.githubusercontent.com/125822919/220534799-b7e9c2ee-fc75-457d-8359-c712b2a7036f.png">

*•	“leafpad run.log” – Opens Log file*

<img width="800" alt="run_log_1" src="https://user-images.githubusercontent.com/125822919/220534836-dc8202a4-ad0b-4c3a-b56b-4a0a1ca70ff9.png">
<img width="800" alt="run_log_2" src="https://user-images.githubusercontent.com/125822919/220534842-ffae7a6b-1397-465e-8b35-2d5298cc3d4a.png">


# **[DAY 2](https://github.com/SidhuT/Sign-off-Timing-Analysis---Basics-to-Advanced/blob/main/README.md#day-2)**

Gained knowledge on topics:

Timing checks

Design rule checks

Latch Timing

STA Text Report

## *LAB 2 - Liberty Files, SPEF, timing reports*

*•	Liberty file - .lib file is an ASCII representation of the timing and power parameters associated with any cell in a particular semiconductor technology and contains timing models and data to calcumax like I/O delay paths, Timing check values, Interconnect delays.*

*•	‘read_liberty’ command in ‘run.tcl’ for reading liberty file.*

*•	Type ‘cd lab2’ and then ‘ls’ then all files in lab2 appears.*

<img width="800" alt="run_tcl" src="https://user-images.githubusercontent.com/125822919/220536642-f8914b35-aa9c-49f4-9d4a-a0737dd55cd2.png">

<img width="800" alt="simple_sdc" src="https://user-images.githubusercontent.com/125822919/220537584-e608a2a4-4696-4df5-bb5b-b4f9176d6e44.png">


<img width="800" alt="simple_v" src="https://user-images.githubusercontent.com/125822919/220536952-47b7e3ad-0efc-4ec8-933e-5805829e37c5.png">
                                                                                                                                             
<img width="800" alt="Terminal_run" src="https://user-images.githubusercontent.com/125822919/220536994-230b759d-21d0-4689-87ee-ad81b698bb2a.png">

                                                                                                                                             
*•	Open ‘simple_min.lib’ using ‘leafpad simple_min.lib’; open ‘simple_max.lib’ using ‘leafpad simple_max.lib’, then compare.*

<img width="800" alt="simple_max_lib" src="https://user-images.githubusercontent.com/125822919/220536712-8c71e3a1-970a-4f46-8c64-8d62a7e390d9.png">
<img width="800" alt="simple_min_lib" src="https://user-images.githubusercontent.com/125822919/220536803-b26b7167-7bc2-4908-8514-78d3db0c05ad.png">
                                                                                                                               
### **•	Exercise:**

     o	All cells in ‘simple_max.lib’ – 211 cells (30 INV + 30 NAND2 + 30 NAND3 + 30 NAND4 + 30 NOR2 + 30 NOR3 + 30 NOR4 + 1 DFF)

     o	All pins of cell NADN2_X1 in ‘simple_max.lib’ – 3 Pins (pin(“o”); pin(“a”); pin(“b”))

     o	Difference between NAND2_X1 and NAND3_X1 – pins (Extra pin in NAND3_X1 i.e., pin(“c”))

     o	Difference between ‘simple_min.lib’ and ‘simple_max.lib’ is in values.

*•	SPEF file (Standard Parasitic Exchange Format) - .spef file describes parasitic information, never created manually, always generated by tool.*

     o	Contains – Header – Name Map – Top Level Ports – Parasitic Description.

*•	‘read_spef’ command in ‘run.tcl’ for spef parsing.*

<img width="800" alt="simple_spef_1" src="https://user-images.githubusercontent.com/125822919/220537858-2ed4dadd-3114-46b0-9b9f-29f0f67fba27.png">

<img width="800" alt="simple_spef_2" src="https://user-images.githubusercontent.com/125822919/220537877-d4e1ce71-0d9f-4e6b-9ae9-87c8c2d5ffe2.png">


*•	‘report_checks’ command in ‘run.tcl’ is used to report timing on design.*

*•	Add ‘report_timing -num_paths 5’ in ‘run.tcl’ and run ‘sta run.tcl -exit | tee run.log’.*

<img width="800" alt="Terminal_run" src="https://user-images.githubusercontent.com/125822919/220537989-2180d188-25d0-4939-ad8a-ba1ef4298c08.png">

*•	Open ‘leafpad run.log’ file and observe and understand report.*

<img width="800" alt="run_log" src="https://user-images.githubusercontent.com/125822919/220538101-c7fb4f05-355a-4b0d-a1dd-56d6615edaeb.png">

# **[DAY 3](https://github.com/SidhuT/Sign-off-Timing-Analysis---Basics-to-Advanced/blob/main/README.md#day-3)**

MultipleClocks

Timing Arc's and Timing Sence

Cell dalays and Clock networks

Setup and Hold checks detailed

STA Text report

## *LAB 3 - Understanding full reg to reg STA analysis, slack computation and review setup check report*

*•	Open Lab3 in ‘vlsideepdive_openSTA_labs’*

*•	‘cd lab3’*

<img width="800" alt="run_tcl_1" src="https://user-images.githubusercontent.com/125822919/220539578-f86a958a-bff5-4533-a99a-1c517c516875.png">

<img width="800" alt="s27_sdc" src="https://user-images.githubusercontent.com/125822919/220539599-d6fae898-d4c1-4266-9b36-3acc3ce6fc77.png">

<img width="800" alt="s27_v" src="https://user-images.githubusercontent.com/125822919/220539618-eee4c7c1-1baf-483a-8f0f-fb73df967e06.png">

*•	Run ‘sta run.tcl -exit | tee out.txt’*

<img width="800" alt="run" src="https://user-images.githubusercontent.com/125822919/220539700-d5896b5e-8bea-4314-9c5e-4d66742b1e1c.png">

*•	See the ouput – ‘leafpad out.txt’ and the SLACK is -217.323, observe why?*

<img width="800" alt="out_txt_1" src="https://user-images.githubusercontent.com/125822919/220539766-6693b498-5603-4fb8-a688-05858f3c400f.png">


*•	And the path for that design in ‘out.txt’ is*

    *“F1:CK->U3->U4->U5:A1->U7:A2->F2:D”*
    
*•	Changing the number of paths being reported to 100, add this command in ‘run.tcl’ file by ‘leafpad run.tcl’.*

*“report_checks -from F1/CK -endpoint_count 100”*

<img width="800" alt="run_tcl 2" src="https://user-images.githubusercontent.com/125822919/220539359-4772fe13-1d11-4ac8-940e-d3351363f8f1.png">

*•	Again run ‘sta run.tcl -exit | tee out.txt’.*

<img width="800" alt="out_txt_2_1" src="https://user-images.githubusercontent.com/125822919/220539411-79fda4e8-7fb3-4778-8f94-93d7011e5456.png">
<img width="800" alt="out_txt_2_2" src="https://user-images.githubusercontent.com/125822919/220539428-11a68e3f-ee75-4d1b-8e87-81c5722046e6.png">
<img width="800" alt="out_txt_2_3" src="https://user-images.githubusercontent.com/125822919/220539436-8fa24edc-70fb-4e60-96cc-a21a67886ee7.png">
<img width="800" alt="out_txt_2_4" src="https://user-images.githubusercontent.com/125822919/220539451-0f45e902-20ba-4b89-bad2-6895eb8c8b1d.png">
<img width="800" alt="out_txt_2_5" src="https://user-images.githubusercontent.com/125822919/220539465-a4f89c8f-435f-433e-8458-b7b3f235b07e.png">

# **[DAY 4](https://github.com/SidhuT/Sign-off-Timing-Analysis---Basics-to-Advanced/blob/main/README.md#day-4)**

CROSSTALK and NOISE

Operating nodes and other variations

Clock Gating Checks

Checks on Asyn Pins

## **LAB 6 & Lab 7 - Understanding clock gating check and async pin checks**



# **[DAY 5](https://github.com/SidhuT/Sign-off-Timing-Analysis---Basics-to-Advanced/blob/main/README.md#day-5)**

Clock Groups

Clock Properties

Timing exceptions

Multiple nodes

## *LAB 4 - Revisit slack computation, understand CRPR and ECO insertion*



### Instructor
**[Vikas Sachdeva](https://www.linkedin.com/in/vikas-sachdeva-0849577/)** - Semiconductor design professional with more than 17 years of experience in the VLSI Industry and also working as an Advisor, Tech and VLSI Coach and Trainer for vlsideepdive in his spare time.
**[Kunal Ghosh](https://www.linkedin.com/in/kunal-ghosh-vlsisystemdesign-com-28084836/)** - Co-Founder at VLSI System Design(VSD).
