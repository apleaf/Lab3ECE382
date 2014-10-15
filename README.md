Lab3ECE382
==========

Required Functionality Checked off by Captain Trimble 15 October 2014.

##Lab 3 Objective
The purpose of lab 3 was to understand/ comprehend the assembly code Dr. Coulston wrote to set up the Nokia LCD display used with the MSP430.  After understanding what was going on, we were then to modify the code, which originally wrote a vertical bar of pixels, to display an 8x8 block of pixels with each press of the button.

## Pre Lab

The prelab consisted of using the manual for the MSP430 and the Nokia LCD to fill in the charts in the pre lab to understand what was happening in the code, and what the purpose of certain things were.

![alt text](http://i62.tinypic.com/2dw55y1.png)

##Logic Analyzer

next, we used examined the code to fill out the two tables given for the logic analyzer section.  the filled in tables are shown below.

![alt text](http://i61.tinypic.com/2cyini0.png)

Hooking up the MSP430 to the logic analyzer is shown below.

![alt text](http://i57.tinypic.com/10fqjjr.jpg)

Below are photos zoomed on on each call to writeNokiaByte

###Entire Waveform

![alt text](http://i62.tinypic.com/33ojhc9.jpg)

###Line 66

![alt text](http://i61.tinypic.com/fkz1wj.jpg)

###Line 276

![alt text](http://i62.tinypic.com/33d9yit.jpg)

###Line 288

![alt text](http://i60.tinypic.com/5p4l08.jpg)

###Line 294

![alt text](http://i62.tinypic.com/bhnjmv.jpg)

###Reset

![alt text](http://i60.tinypic.com/e5shtj.jpg)

##Writing Modes
We were then tasked with filling out the corresponding charts when anded, ored, and xored together.

![alt text](http://i59.tinypic.com/ri5dlj.png)

##Coding
To get the required functionality, it was simply a matter of setting up a loop that wrote the vertical bar of pixels eight times next to each other each time the button was pressed.  The original code also had a bar with a two pixel hole in the center.  To change that, one simply wrote 0xFF to the register instead, indicating no holes in the bar of pixels.

##Testing methodology/results
To test the code, all I had to do was run the code and see if an 8x8 block of pixels was drawn to the LCD Screen.  This functionality was checked off by Captain Trimble.

##Debugging
I ran into a problem where the block was only being output every two button clicks.  AS it turns out, i had accidently deleted some of Dr. Coulston's code, which caused my program to function incorrectly.  After looking at the original code, i added what i had deleted and the code worked.

##Observations and Conclusions
This lab was very hard to grasp conceptually at the beginning and understand what was going on.  After really pouring over the code though, it began to click and understanding where the loop to print the block needed to be was not that difficult.

Documentation:
C2C Terragnoli showed me how to hook up and use the logic analyzer.
