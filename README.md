# OpenAg Eagle Library
Common Parts Library for PCBs designed in Eagle for OpenAg

## Usage
1. When starting a new design, fork this library onto your personal github account
2. Clone your fork into the eagle library on your local machine
3. Use an existing component whenever possible to maximize the number of shared parts between designs
4. Add new components as needed
5. Once the PCB has been fabricated and tested, create a pull request back to the OpenAgInitiative's eagle library repo
6. Merge must be approved by someone other than you


## Guide for Creating Parts in Eagle
### Packages
	* >NAME above >VALUE
	* >NAME on tNames layer
	* >VALUE on tValues layer
	* Pads with clean names (e.g. 1, 2, 3 instead of $P.1, etc.)
	* Part outline on tPlace layer

### Schematics
	* >NAME above >VALUE
	* >NAME on names layer
	* >VALUE on values layer

### Devices
#### Description (build this with HTML tags)
	* Manufacturer & Manufacturer P/N
	* Technical Specs (examples include:)
		* recommended supply voltage
		* operating temperature
		* <just the most important specs from datasheet>
	* Vendors
		* Vendor: Vendor P/N linked to url

#### Description Template
```
<b> Manufacturer - Manfacturer P/N - Short Description</b>
<p>Description:
<ul>
<li>Add a description...usually the detailed description from digikey if they have one. If not then just use the short one</li>
</ul>
</p>

<p> Technical Specifications:
<ul>
<li>Useful Info</li>
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
</ul>
</p>

<p>Datasheet(s):
<ul>
<li><a href="Link to Datasheet">Datasheet Name</a></li>
</ul>
</p>

<p>Vendor(s):
<ul>
<li>Digikey: <a href="link to part">Vendor P/N</a></li>
</ul>
</p>
```

#### Attributes
	* VALUE
		* variable or constant
	* POPULATE
		* variable
		* default to YES, can change to NO in schematic if necessary
	* VERIFIED
		* constant
		* default to NO, once verify physically change to YES

### Enable Updates to Value Field
	* Select YES on the radio button
	* Set prefix value
		* C - capacitor 
		* D - diode/LED 
		* J - header pins or connectors 
		* JP - jumper L - inductor 
		* Q - transistor/FET 
		* R - resistor 
		* SW - switch 
		* TP - test point 
		* U - integrated circuit (sensor, MCU, etc.) 
		* X - crystal or oscillator


