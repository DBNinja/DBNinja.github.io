I use the [mriscoc "professional" firmware](https://github.com/mriscoc/Ender3V2S1) , but I've enabled certain configurations that have to be done in the programmer. Note that this is a "Marlin" firmware.

Here's the options enabled (I can help you out if you ever need it by the way)
1. Support a higher temperature by using the **Volcano** AKA **T5** thermistor setting (ATC Semitec 104GT-2/104NT-4-R025H42G) 
2. Full beeper
3. Enable the BLTouch (with UBL bed leveling)
4. [Linear Advance](https://github.com/mriscoc/Ender3V2S1/wiki/Linear-Advance-(LA)) Enabled (also known as Pressure Advance)
	1. Tuning guide for this can be found on [the ellis3dp page](https://ellis3dp.com/Print-Tuning-Guide/articles/index_pressure_advance.html)
5. Input Shaping Enabled
6. [MPC Enabled](https://github.com/mriscoc/Ender3V2S1/wiki/Model-Predictive-Temperature-Control-(MPC) (better temperature control than PID)


 Note that my firmware has a special configuration with the following options (I'll help you out if you ever need it)
		- Support a higher temperature by using the **Volcano** AKA **T5** thermistor setting (ATC Semitec 104GT-2/104NT-4-R025H42G) 
		- Full beeper
		- Enable the BLTouch (with UBL bed leveling)
		- Linear Advance Enabled
		- Input Shaping Enabled
		- [MPC Enabled](https://github.com/mriscoc/Ender3V2S1/wiki/Model-Predictive-Temperature-Control-(MPC) (better temperature control than PID)
