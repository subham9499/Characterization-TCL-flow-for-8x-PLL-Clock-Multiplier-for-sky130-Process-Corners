# Characterization-TCL-flow-for-8x-PLL-Clock-Multiplier-for-sky130-Process-Corners

### Running the Simulation
1. Clone this repo. <br/>
2. cd <repo_name>/Prelayout <br/>
3. open the PLL_PreLay.cir and change .include /home/Characterization-TCL-flow-for-8x-PLL-Clock-Multiplier-for-sky130-Process-Corners/sky130nm.lib accordingly . <br/>
4. Run the PLL circuit by typing `ngspice PLL_PreLay.cir` <br/>

The block diagaram of the PLL as a clock multiplier is as follows:
![](/images/pll_freq.png)
Here M = 8

Tested through spice simulations on skywater 130nm ss corner at room termperature

### PD Circuit ouput

![](/images/pd1.png)

![](/images/pd2.png)

Red: Clock 2 <br />
Blue: Clock 1 <br />
Orange: Up Signal <br />
Green: Down Signal
 
### Frequency Divider Circuit output

![](/images/fd.png)

Red: Output Clock <br />
Blue: Input Clock  <br />

### Charge Pump(CP) output

![](/images/cp.png)

Red: Charge Pump Output Voltage

### VCO Output

![](/images/vco.png)

### PLL Output

The PLL output from the prelayout simulation is as follows:


![](/images/pll3.png)


<!-- ![](/images/pll4.png) -->

<!-- ![](/images/pll5.png) -->

![](/images/pll_100.png)

![](/images/pll_101.png)

### Exact 100 MHz 
![](/images/pll_104.png)

Red: Reference Clock <br />
Blue: Output Clock Divided by 8 <br />
Yellow: Down Signal <br />
Brown: Up Signal <br />
Pink (at top): ChargePump output  <br />

## Layout

### Frequency Divider

![](/images/fd_1.png)

### Charge Pump

![](/images/CP_layout.png)

### Voltage Controlled Oscillator

![](/images/vco_new.png)

## Post Layout Simulation

### Frequency Divider

![](/images/fd_PLS.png)

### Charge Pump

![](/images/CP_PLS.png)



### Future Work
Doing Layout for remaining components and doing a post layout simulation.

### Aknowledgement 
This PLL IP was taken from Lakshmi S 's github page:  https://github.com/lakshmi-sathi/avsdpll_1v8
