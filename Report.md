Name: Maryn Kunthara

EID: mhk724

Team Number: Angela, Christian, Hector, Mark

## Questions

1. Why does your program need a setup and a loop?

    It needs a setup so you can initialize the hardware with the specifications of what you need for that certain program, like which pins are input. It needs a loop so that the functions you call are continuously running and if needed, continuously reading and writing data from and to ports.

2. What is the downside to putting all your code in a loop?

    The code obviously continuously runs without stopping, doing the same thing over and over again.
    

3. Why does your code need to be compiled?

    A compiler translates a programming language to machine language so that the machine can actually execute the program you wrote.

4. When lowering the frequency in procedure A, step 4, what is going wrong? Brainstorm some solutions. Dimmers exist in the real world. What is their solution?

    The LED looks to be flickering because the frequency is too low. The human eye shouldn't be able to detect the on-and-off in the duty cycle while it's dimming. One obvious solution is increasing the frequency.

5. Why do you need to connect the logic analyzer ground to the ESP32 ground?

    So that you have a reference difference for the voltage for the analyzer to actually work.

6. What is the difference between synchronous and asynchronous communication?

    Synchronous is when every change in state/cycle runs in conjunction with the clock cycles. Asynchronous is when data can be transmitted sporadically instead of in a set, repeated clock pace. 

7. Profile of UART: Sent X bytes in Y time 

    11 bytes in 0.9465 ms

8. Profile of SPI: Sent X bytes in Y time

    11 bytes in 0.288 ms

9. Why is SPI so much faster than UART?

    It has more wires which connect the master and slave devices. Each direction of communication has its own line (MOSI/MISO). There's also seperate lines for the clock and the chip select. 

10. list one pro and one con of UART

     One pro is that it's simplest to use in terms of hardware complexity. As this is one to one connection between two devices, software addressing is not required. 
     One disadvantage is that it's only suitable for communication between only 2 devices.

11. list one pro and one con of SPI

    One pro is that SPI is faster than UART because it has individual lines for communication between master and slave devices. 
    One con is that the more slave devices you add, the more CS lines you have to add, which increases hardware complexity.

12. list one pro and one con of I2C

    One pro is that the I2C can support multiple devices to be the master device and allows for switching a device between master and slave status.
    One con is that the protocol is managed by a software stack which means the microcontroller/s processing overheads increase.

13. Why does I2C need external resistors to work?

    On the I2C, each signal line has a pull-up resistor to restore the signal to high when no master or slave device is asserting it low.

## Screenshots

Procedure A, step 1:
![Put path to your image here ->](C:\Users\InvenioAI\Desktop\ee109k\109k_Lab1\arduino-lab-1-marynkunthara\timed_blink_sc.PNG)

Procedure A, step 4:
![Put path to your image here ->](C:\Users\InvenioAI\Desktop\ee109k\109k_Lab1\arduino-lab-1-marynkunthara\dimmer_logic2.PNG)

Procedure B, UART:
![Put path to your image here ->](C:\Users\InvenioAI\Desktop\ee109k\109k_Lab1\arduino-lab-1-marynkunthara\uart_message_final.PNG)

Procedure B, SPI:
![Put path to your image here ->](C:\Users\InvenioAI\Desktop\ee109k\109k_Lab1\arduino-lab-1-marynkunthara\SPI_timing.PNG)
