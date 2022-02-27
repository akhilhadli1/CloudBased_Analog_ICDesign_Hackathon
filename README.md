# Three-Transistor-Two-Input-Universal-NAND-Gate
3T two input NAND gate is a low power implementation of Conventional CMOS NAND gate which requires 4 transistor using pass transistor logic

# This repository contains the following contents

- [About Hacakthon](#about-hacakthon)
- [Abstract](#abstract)
- [Circuit description](#circuit-description)
- [Reference Circuit](#reference-circuit)
- [Reference Wave form.](#reference-wave-form)
- [Tools Used](#tools-used)
- [Simulated Circuit Using Synopsys Tool](#simulated-circuit-using-synopsys-tool)
- [Challenges](#challenges)
- [Author](#author)
- [Acknowledgements](#acknowledgements)

# About Hacakthon
IIT Hyderabad in collaboration with Synopsys & VSD wants to generate skilled manpower in the domain of IC design, which will strengthen the decision of the Indian Government for the silicon revolution. The Indian Govt initiative Chips to Startup (C2S) aims to propel innovation, build domestic capacities to ensure hardware sovereignty, and build a Semiconductor Ecosystem that requires 85,000+ highly trained engineers. Working towards this vision statement, we have planned the 3-Week “Cloud based Analog IC Design Hackathon using Synopsys Custom Design Platform”.


# Abstract
VLSI circuits consists of various analog and digital elements to achive the system specifications. Most of the systems we see currently are digital and  with some part as analog block.These blocks are bulit with the basic building blocks namely logic gates AND,OR,NOR,XOR,NAND.In these gates NAND and NOR are Universal gates i.e all the gates  can be obtaines using universal gates .In particular NAND gate is most used due to its advantages over NOR gate like it is  fast than NOR .So optimizing NAND gate implemetation with less area will automatically reduce the cost in bulding large circ  uits.In this Project NAND gate is implemented with 3 transistor unlike the CMOS implementation which has four tansistor to reduce area and power.This gate is Implemented in 28 nm Bulk Cmos Synopsys PDK.

# Circuit description
NAND gate is a logic gate which gives the output as HIGH when one or more input are at logic low level,and low if both the inputs are HIGH.This gate is majorly implemented using CMOS logic Implementation.Shown below

![nanna](https://user-images.githubusercontent.com/99066092/155873381-01faf299-a87b-4a16-8234-39a635e69eac.png)




Truth Table for the above gate is shown below.

![image](https://user-images.githubusercontent.com/99066092/155870985-54568206-f40a-4c8c-a1e1-b8262f773eaa.png)

The Above Implementation requries 4 transistor (2-PMOS and 2-NMOS) .Where as In the paper proposed the NAND Gate is Implemented with Three transistor (2-PMOS and 1-NMOS) which can reduce the area on core and power optimized.This is a Low power implementation of traditional CMOS Implementation .This Implementation uses Pass Transistor logic to achive the functionality.
# Reference Circuit
![WhatsApp Image 2022-02-27 at 1 55 27 PM](https://user-images.githubusercontent.com/99066092/155874700-1a84afa3-8be1-469d-9713-0e676cd2fa94.jpeg)


Circuit operation
The design is basedon modified CMOS inverter and PMOS pass-transistorlogic. When input A is at logic one, the inverter on theleft (M0 & M2) functions as a normal CMOS inverter.Therefore, the output is the complement of input B. Whenthe input A is at logic zero, the CMOS inverter output is at high impedance. However, the PMOS pass-transistor M1 is turned ON and the output gets the logic value as logic 1 (VDD). This circuit achives same output as CMOS NAND gate with optimization in area and power.

# Reference Wave form.
![referance waveform](https://user-images.githubusercontent.com/99066092/155871615-c476d500-bed8-42e4-9135-7f8e4ad2a669.PNG)

Circuit operation
The design is basedon modified CMOS inverter and PMOS pass-transistorlogic. When input A is at logic one, the inverter on theleft (M0 & M2) functions as a normal CMOS inverter.Therefore, the output is the complement of input B. Whenthe input A is at logic zero, the CMOS inverter output is at high impedance. However, the PMOS pass-transistor M1 is turned ON and the output gets the logic value as logic 1 (VDD). This circuit achives same output as CMOS NAND gate with optimization in area and power.
# Tools Used

. Synopsys Custom Compiler:  The Synopsys Custom Compiler™ design environment is a modern solution for full-custom analog, custom digital, and mixed-signal IC design. As the       heart of the Synopsys Custom Design Platform, Custom Compiler provides design entry, simulation management and analysis, and custom layout editing features. This tool was used   to design the circuit on a transistor level.

. Synopsys Primewave:  PrimeWave™ Design Environment is a comprehensive and flexible environment for simulation setup and analysis of analog, RF, mixed-signal design, custom-     digital and memory designs within the Synopsys Custom Design Platform. This tool helped in various types of simulations of the above designed circuit.

. Synopsys 28nm PDK:  The Synopsys 28nm Process Design Kit(PDK) was used in creation and simulation of the above designed circuit.

# Simulated Circuit Using Synopsys Tool

 Schematic of NAND gate:
 
![Schematic](https://user-images.githubusercontent.com/99066092/155871790-dccc26d8-3175-4475-bce4-5a15bc5c06a6.PNG)
 TestBench:
 
![TBschematic](https://user-images.githubusercontent.com/99066092/155871802-ef06d592-a8cf-4e96-b20a-ddfc17c2c44a.PNG)

 WaveForms Obtained:
 
I was able to get the correct waveforms as the reference circuit
![visible waveform](https://user-images.githubusercontent.com/99066092/155874113-c0186fe9-78f0-41c5-8ff7-1a01a92f73b7.PNG)


# Challenges 

The major challenege  faced during implementation wa sto decide the W/L ratio as the reference circuit was implemented in 90nm technology .So while implementing in 28nm Technology W/L needs to be calcuated accordingly.So after many iterations  a correct W/L ratio was adjusted and reference waveform were captured.
 The Final W/L ratio for  all there transistor are:
  Transistor M1(PMOS) :w=3.5um ,l=0.03um(30nm)
  Transistor M1(NMOS) :w=0.11um ,l=0.03um(30nm)
  Transistor M1(PMOS) :w=0.1um ,l=0.43um(30nm)
 @ VDD 1V supply and 1 V inputs



# Author
Akhil Hadli,BLDEACET,Vijayapura
# Acknowledgements 
Synopsys India

Indian Institue of Techonology Hyderabad

Kunal P Ghosh, Co-founder, VSD Corp. Pvt. Ltd. - kunalpghosh@gmail.com

Chinmay Panda,IIT Hyderabad

