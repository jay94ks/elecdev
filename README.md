# Custom Development Board Projects.
This project is for making custom development boards with minimal circuits to power MCUs, including programming them.

## MISC
* USB-C breakout: https://github.com/jay94ks/elecdev/tree/main/misc/USB_C_BREAKOUT

## Raspberry-Pi Silicon
### RP2040
See this directory: https://github.com/jay94ks/elecdev/tree/main/rp2040 <br />
ARM® Cortex®-M0+ Dual-core, 32bit, QFN-56.<br />
Features: 133 MHz max, 256kB SRAM, `UART` x2, `SPI` x2, `I2C` x2, `PWM` x 16 channel.<br/>

### TODO: RP2350A, RP2354A 
### TODO: RP2350B, RP2354B
I'm waiting for these chips are available on chip stores. :)

## STM32
I love STMicroelectronics's `TSSOP-20` and `TSOP-8` (G03xJ6Mx).
It is small, has few pins, is easy to use by plugging it into a breadboard,
and has a simple peripheral circuit. I even like the size of the flash memory and the size of the built-in RAM. 
Additionally, they fit well on any board that can be made easily, and there is little need to configure an external clock circuit.
I hope more chips will be released in `TSSOP-20`, `TSSOP-16` or `TSOP-8` versions. And it would be better if they could have USB DP/DM pins.

### G030F6
See this directory: https://github.com/jay94ks/elecdev/tree/main/stm32/g030f6 <br />
ARM® Cortex®-M0, 32bit, TSOC-20.<br />
Features: 64 MHz MAX, 32K Flash, 8K RAM, `USART`, `SPI`,  `I2C`.<br/>
Board Size: 17.78 mm * 25.4 mm.<br />
Price: about 2,800 KRW, 2.11 USD.<br/>
![STM32G030F6Px](https://github.com/jay94ks/elecdev/blob/main/stm32/g030f6/v1/STM32G030F6Px_BRD.png)

### F042F6
See this directory: https://github.com/jay94ks/elecdev/tree/main/stm32/f042f6 <br />
ARM® Cortex®-M0, 32bit, TSOC-20.<br />
Features: 48 MHz MAX, 32K Flash, 6K RAM, `USART`, `SPI`, `USB FS`, `CAN`, `I2C`.<br/>
Board Size: 22.86 mm * 32.05 mm.<br />
Price: about 5,500 KRW, 4.15 USD.<br/>
![STM32G030F6Px](https://github.com/jay94ks/elecdev/blob/main/stm32/f042f6/v1/STM32F042F6Px_BRD.png)

### F107RBT6
See this directory: https://github.com/jay94ks/elecdev/tree/main/stm32/f107rbt6 <br />

### G030K8
See this directory: https://github.com/jay94ks/elecdev/tree/main/stm32/g030k8 <br />

## WCH
### CH32V003F4P6
See this directory: https://github.com/jay94ks/elecdev/tree/main/wch/ch32v003f4p6 <br />

### CH32V003F4U6
See this directory: https://github.com/jay94ks/elecdev/tree/main/wch/ch32v003f4u6 <br />

### CH32X033F6P6
TODO: I bought this chip few weeks ago, I'll design this one soon. (100 pcs)

### CH32X035G8U6
See this directory:  https://github.com/jay94ks/elecdev/tree/main/wch/ch32x035g8u6 <br />