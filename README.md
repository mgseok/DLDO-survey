# Digital Low-Dropout Voltage Regulator (DLDO) Survey 

The CSV file contains the digital low-dropout voltage regulators (DLDO) published in 2010--2020. It contains the reported and estimated parameters and metrics of each regulator. The paramete/metric definition can be found in the table below. 

For use in publications and presentations please cite this data collection as follows:
M. Seok, Z. Wang, S. J. Kim, "Digital Low-Dropout Voltage Regulator (DLDO) Survey," [Online]. Available: https://github.com/mgseok/DLDO-survey

Please contact to report any errors:  
Zhaoqing Wang: zw2711@columbia.edu  
Sung Justin Kim: sjk2206@columbia.edu  
Mingoo Seok: ms4415@columbia.edu  

| Metric | Symbol | Definition |
|--------|--------|------------|
| Technology | n/a | Fabrication process node|
| Output capacitance [nF] | Cout | Output capacitor's capacitance |
| Active area [mm^2] | n/a | Total silicon area excluding output capacitor(s) area |
| Active & passive area [mm^2]	| n/a | Total silicon area including on-chip output capacitor(s) area (designs with off-chip capacitor are exclueded) |
| Input voltage [V] | Vin	| Supply voltage to an LDO (used in dynamic load regulation test) |
| Output voltage [V] | Vout | Output voltage of an LDO (used in dynamic load regulation test) |
| Output reference voltage [V] | Vref | The set point of the output voltage of an LDO |

Dropout voltage [V]						Vdropout				Voltage drop from input voltage to output voltage (Vin-Vout)
Voltage droop [V]						Vdroop					Vout's maximum downward deviation from output reference voltage (Vref) when the load current changes by its maximum (tested) load current change (dIload)
Voltage overshoot [V]						Vovershoot				Vout's maximum upward deviation from output reference voltage (Vref) when the load current changes by its maximum (tested) load current change (dIload)
Max load current [mA]						Iload,max				Maximum load current that an LDO can support under the output voltage error (Verror) constraints
Min load current [mA]						Iload,min				Minimum load current that an LDO can support under the output voltage error (Verror) constraints
Max (tested) load current change (droop) [mA]			dIload,max,droop			Maxium tested load current change for voltage droop
Max (tested) load current change (overshoot) [mA]		dIload,max,overshoot			Maxium tested load current change for voltage overshoot
Edge time [ns]							tedge					Time for the max (tested) load current change 
Settling time (droop) [ns]					tsettle,droop				Time to take for Vout to settle within less than a small % of Vref for voltage droop
Settling time (overshoot) [ns]					tsettle,overshoot			Time to take for Vout to settle within less than a small % of Vref for voltage overshoot
Quiescent current [uA]						Iq					Current draw of an LDO when it supports steady-state load current
Peak current efficiency 					CEpeak					Iload,max/(Iload,max+Iq)
Peak power efficiency						PEpeak					(Vout*Iload,max)/(Vin*(Iload,max+Iq))
PSRR [dB]							PSRR					The ratio of output voltage change to input voltage change, 20*log(dVout/dVin)
Power-FET unit current [nA]					Iu					Unit current in the power-FET array
Output ripple voltage						Vripple					Output ripple size
Output voltage deadzone [mV]					Vdz					A voltage range where controller does not update its output
Output voltage error [mV]					Verror					Maximum output voltage deviation from Vref in the steady-state load and line condition. Typically larger of Vripple/2 or Vdz/2
Output voltage temperature coefficient				TC					Output voltage drift over temperature variation
Current Density [mA/mm^2]					-					current density	Max load current/Active & passive area
Load-regulation FoM 1 [ps]					ps-FoM					([Cout*dVout]/dIload)*[Iq/dIload], smaller FoM is better
Load-regulation FoM 2 [pF]					pF-FoM					[dVout/(Vout*dIload)]*(Cout*Iq), smaller FoM is better
Load-regulation FoM 3 [edge-adj ps]				edge-adj ps-FoM				([Cout*dVout]/dIload+0.5*Tedge)*[Iq/dIload], smaller FoM is better
Load-regulation FoM 4 [pC]					pC-FoM					([Cout*dVout]/dIload+0.5*Tedge)*Iq, smaller FoM is better



