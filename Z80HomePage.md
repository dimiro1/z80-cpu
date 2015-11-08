# **Z80 Microprocessor Java Emulation** #

A general purpose implementation of the ZiLOG Z80 microprocessor core in Java.  This core accurately emulates all valid op-codes while attempting to cover all undocumented features.

The emulator features:

  * All standard instructions
  * All flags, including unused bits
  * All undocumented instructions I can find including IX / IY as HL, missing shifts, bit twiddling (Expanded in 3.0.1)
  * Accurate T state timings
  * Simulated R register
  * IFF1 and IFF2 handling
  * NMI handling


![http://www.cpu-world.com/CPUs/Z80/L_Zilog-Z80%20CPU%20(wgg).jpg](http://www.cpu-world.com/CPUs/Z80/L_Zilog-Z80%20CPU%20(wgg).jpg)

White-ceramic Z80 photo by Gennadiy Shvets.  [Link](http://www.cpu-world.com/CPUs/Z80).