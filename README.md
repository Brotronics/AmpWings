# AmpWings
Tiny current sensor for planes and multirotors

## Configuration

AmpWings provides both current and voltage outputs for analog
sensors.

### Voltage

The voltage reading may be raw or divided as configured by two pairs
of pads in the bottom right of the top of the PCB (see images below).
You must place a solder blob on exactly one of these for voltage to be
read correctly.

The top pair (labeled `div`) is for 1:15.7 divided voltage on the V
pad.  e.g., a reading of 750mV corresponds to about 11.77 volts.

The bottom pair (labeled `raw`) will send the raw voltage over the V
pad.  This is useful for a pre-divided ADC such as in naze32.

### Current

For the 90A variant, you can measure 36.6mV per Amp over the C pad.

For the 180A variant, measure 18.3mV per Amp.

## Usage

AmpWings goes inline with your power as soon as it leaves the battery
as you can reasonably place it.

The easiest way to do this is to cut the positive (red) lead of an
XT60 cable and solder the side nearest the XT60 plug to the bottom on
the side marked `IN`.  Solder the remaining remaining bit of red wire
to the other end.

For the negative side, just shave a little of the insulation off so
that the wire is exposed just at the negative pad on the top and
solder it securely to the large negative pad.

## BOM

* U1 [INA169 Current Monitor](http://www.digikey.com/product-detail/en/0/296-26063-1-ND)
* U2 Shunt Resistor – chose one:
  * [.0005Ω for 90A](http://www.digikey.com/product-detail/en/CSS2725FTL500/CSS2725FTL500CT-ND)
  * [.00025Ω for 180A](http://www.digikey.com/product-detail/en/0/CSS2725FTL250CT-ND)
* U3 [Op Amp](http://www.digikey.com/product-detail/en/0/296-36218-1-ND)
* C1,C2 [0603 0.1μF cap](http://www.digikey.com/product-detail/en/GRM188R71C104KA01D/490-1532-1-ND/587771)
* R1 [0603 73.2kΩ resistor](http://www.digikey.com/product-detail/en/0/P73.2KHCT-ND)
* R2 [0603 4.7kΩ resistor](http://www.digikey.com/product-detail/en/0/P4.70KHCT-ND)
* R3 [0603 10kΩ resistor](http://www.digikey.com/product-detail/en/0/RMCF0603FT10K0CT-ND)
* R4 [0603 1kΩ resistor](http://www.digikey.com/product-detail/en/0/P1.00KHCT-ND)

## Assembly

### Top

![top](http://i.imgur.com/0cU4cir.png)

### Bottom

![bottom](http://i.imgur.com/NfhLJEU.png)

<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License</a>.
