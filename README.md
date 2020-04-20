# Lebowski-board-SMD
Single version of Lebowski board to fit Volt/Ampera inverter.
Included in new board is voltage sensing option and temperature sensing.
I added CAN bus chip 
Also to keep the same wiring in my car as with Johannes controler i added signal inversion chip 
There is also an option of using one signal to pull down both throttles so motor is freerunning and we can shift. 
Arduino interface is controlling precharge and is telling main chip of the voltage reading.
There is a 5pin connector on LED lines that could be used to transmit controler status inside a cabin on the dash. 

Revision 2 was not viable since Rev 3 has some major changes and will be used directly.
In R3 i changed design of voltage sensing with isolated op amp and a second op amp to boos signal to be accepted by Arduino Nano chip.

In R3.1 i decided to discard Nano because of its inherent bootlayer instability. I will use a simple Pic12F1822 chip programmed to detect voltage, then trigger Tip122 for precharge. Its other pins maight be used to translate HV voltage to Lebowski brain and to keep brain in reset untill precharge is done.
