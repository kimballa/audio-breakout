
Breadboard audio breakout
=========================

This board is intended to sit next to a pair of breadboards and plug into the power bus rows and the
first few columns of each breadboard. Measurements were taken on Adafruit breadboards.

Power
-----

Power bus rows are filled with +12V, GND, and -12V from the onboard power header.
* This takes a molex 3-pin MicroFit 3.0 cable from a GS-101-PWR.
* There is a power switch, and LEDs to show you when it's engaged.
* There are jumper headers that the power flows through before accessing your board.
  * Close these with SPC02SYAN shunt jumpers to let the power flow.
  * Or hook your ammeter here to measure current consumption precisely.
  * The onboard opamp and LEDs are upstream of the jumpers and will not be included 
    in your current measurements.
* There is also a 3-pin MicroFit 3.0 header to daisy-chain a cable to a module under test,
  for current measurement purposes.


Leveling feet
-------------

The two mounting holes on the outboard edge of the PCB are sized for an M3 screw. A 20mm machine
screw with an integral end-stop like JLCPCB Mechatronics' EKLF-W-P12-M3-L20 can be used to balance
this edge of the board so that it lies flat when you adjust potentiometers or plug in cables.


Reference voltages
-------------------

There are two reference voltages generated onboard and brought out to pins, at 8.0V and 6.0V. Use
the two trimpots on the bottom of the PCB to calibrate these.

Jacks
-----

There are six jacks, `IO1..IO4`, `OUT1`, and `OUT2`. 

The I/O jacks are general purpose and bidirectional. Shields are attached to GND via 1M resistance.
The tip goes to the labeled pin on the breadboard.

OUT1 and OUT2 are unity buffered by an opamp with 220kOhm input impedence. These are intended to
drive a signal to a speaker or other external system. The TL074H opamp is specified to deliver at
least 25mA before losing voltage fidelity. The shields for OUT1 and OUT2 are directly connected to
GND. 

There are also header pins on the top of the board for accessing OUT1 and OUT2 on a 'scope or
multimeter.

Pots
----

There are four PTV09 potentiometers, two at 100kOhm and two at 10kOhm resistance. All three pins of
each pot are brought out to the breadboard. Pin numbers are indicated with one to three dots.

