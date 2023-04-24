# On the Gemini V3 batch of temperature failure motherboard processing program
According to the answer I got from the official communication with mellow, I roughly sorted out two ways to solve about the host temperature error.

1、The solution from the software is:  

remove the FLY-Gemini temperature sensor inside the printer.cfg    
![Host-temperature-failure 1!](https://github.com/Lzhikai/SIBOOR-Voron-0.2/blob/main/Host-temperature-failure/1.png "Host-temperature-failure 1")

2、The solution in terms of hardware is：

Replace one R8 element above the H5 chip with a "0402 450K 1%" type resistor.   
![Host-temperature-failure 2!](https://github.com/Lzhikai/SIBOOR-Voron-0.2/blob/main/Host-temperature-failure/2.png "Host-temperature-failure 2")


3、Use type-c to power the motherboard, use a multimeter to measure the capacitance value of "C6", the return value of 3.3V is normal.
## ！！！！Be careful not to shake the hands of other accidents occur！！！！  

![Host-temperature-failure 3!](https://github.com/Lzhikai/SIBOOR-Voron-0.2/blob/main/Host-temperature-failure/3.png "Host-temperature-failure 3")
![Host-temperature-failure 4!](https://github.com/Lzhikai/SIBOOR-Voron-0.2/blob/main/Host-temperature-failure/4.png "Host-temperature-failure 4")
## Attention：If you are not sure to replace the components, it is recommended to modify the printer.cfg to solve it from the top of the software.
