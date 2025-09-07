## Analog Front End for IoT 
Averaged 12 hours a day in `Cory Hall` working on this. Built on Sky130 and consists of an ADC block, ADC front end, and power block. Meant to interface with a digital microcontroller. 

### Programmable Gain Amplifier (PGA) 
Programmable gain amplifier with gain steps of 1, 2, 3, 4, 5, 6, 7, and 8. Supports outputs between 0 V to 1 V. Built using two-stage folded cascode architecture. Takes inputs from an analog mux (V_BAT/4, VPTAP, VIN1, VIN2). Gain error of <1 LSB (4 mV) for all gain settings at all temperatures assuming ideal rail.

### Analog to Digital Converter (ADC) 
8-bit ADC using a 1 V reference voltage. Implemented using a switch capacitor CAPDAC and a strongarm comparator. 

### Bandgap Reference (BGR) and Low Dropout Regulator (LDO) 
Designed for battery voltage of between 3.3 V and 2 V (2  alkaline batteries). Supplies a 1.8 V rail with drift of +/- 10% across temperature and supply voltage. 
