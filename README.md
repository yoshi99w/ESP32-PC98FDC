# ESP32-PC98FDC

I want to import the contents from an old floppy disk(FD) that has some
read errors.  For example, I would like to retrieve data from the FD of
an old personal computer(PC) such as PC-9801, X68000, and so on.

It is challenging to recover data with read errors from original PC's
FD controller(FDC).  Read errors occur when the recorded magnetic pulses
have either disappeared or weakened.  Consequently, data recovery involves
determining the position of the magnetic pulse recorded on the FD and
locating the missing pulse to eliminate read errors.  In other words,
ensuring the correctness of the recorded cyclic redundancy check(CRC) value
facilitates successful data recovery.

Plannning to do this in two steps:

1. Retrieve the position of the magnetic pulse recorded on the FD.

 Utilize ESP-WROOM-32(ESP32), which is more cost-effective and offers
 higher performance than Arduino, along with the actual FD drive(FDD).

 Referencing several similar projects shared online, I am considering
 the circuit for connectiong ESP32 and FDD.

 Taking inspiration from the excellent tool
 [ArduinoFDC](https://github.com/dhansel/ArduinoFDC),
 I will develop an ESP32 version of the limited-function FDC.  This version
 will read the position of magnetic pulse recorded on the FD and transfers
 it to the terminal.

2. Identify and recover the missing pulse to eliminate read errors.

 Proceed with the operation on the destination terminal.

---
## References
programming
- [ArduinoFDC](https://github.com/dhansel/ArduinoFDC)

circuit design
- [Create an FDD controller with FPGA](http://s-sasaji.ddo.jp/bml3mk5/fddctrl01.htm) in Japanese
