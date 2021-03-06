# MPPC Sensor
The sensor board has just the MPPC and a coaxial connector to feed in the high voltage and inside shielding pull the signal out. There are two mounting holes on the sides and the board is designed to be small and mounted inside a plastic carrier. An ambient temperature sensor is required to set the voltage but is not provided on the board, as the gain is dependent on temperature and bias voltage, a constant gain can be maintained by changing the bias in response to temperature.

![][renderAssembly]

## Hardware
This board houses a surface mount 2.0mm MPPC by Hamamatsu. Specifically, S13360-20**VE series. Both ports are routed directly out to the connector. The board is  0.25in (6.35) tall, 0.5in (12.7mm) wide and approximately XXin deep. It is attached to the housing with two M2 screws. 

![][renderFront]

## Cable
A U.FL coaxial connector is mounted on the back. It is rated for 50 mattings. HV is brought in through shielding (connected to cathode) and should be insulated. signal is returned (anode) through the inner conductor. The connector and the board have no polarity.

![][renderBack]

## Housing
Housing is designed in Autodesk inventor, more info later.

## Fabrication/Assembly
Documents such as gerbers, PNP, BOM, STL, images and renderings are availible in the `production` directory.

The PCB is a two sided 63mil (1.6mm) with 6/6 routing. Front and back silk and soldermask is not needed but prefered. Assembly requires PNP on two sides, but ideally should be done manually. The MPPC should be handeled delicately and its part number and parameters should be kept. After assembly place the part back in its original bag. 

### Front PCB
Only MPPC on front with though mounting holes shown. The polarity is shown with the notch visible at the bottom. 
![][frontAsy]

### Back PCB
Back has only the U.FL connector. There is only one polarity but since there are two tabs generally available on the connectors the bottom must be ckeced or the pin one cut corner to determine orientation.
![][backAsy]

### Soldering
Solder the back first (reflow or by hand) before placing and reflowing the MPPC, surface tension should be enough to hold in place for the reflow, but CA can be applied to make sure it does not shift. The MPPC ideally should be reflowed with the Hamamatsu temperature profile.
![][mppcTemp]

### Housing
The housing is to be made form a opaque material. Can be 3D printed or IM (if design permits). More infor after design.

[renderAssembly]: production/images/renderAssembly.png "Full assembly permutations inculding housings."
[renderFront]: production/images/renderFront.png "Assembled board front render showing MPPC."
[renderBack]: production/images/renderBack.png "Assembled board back render showing connector."
[frontAsy]: production/images/frontAsy.png "Component location and markings for front."
[backAsy]: production/images/backAsy.png "Assembled board back render showing connector."
[mppcTemp]: production/images/mppcTemp.png "Reflow temperature profile for Hamamatsu MPPC from datasheet."


