```
AP#:      7
Repo:     pinus-rigida
Title:    Agathis Hardware Specification
Author:   md-agathisproject
License:  CC-BY-SA 4.0
```

# Agathis Hardware Specifications

## Table of Content

[0. Release History](#0-release-history )  
[1. Introduction   ](#1-introduction    )  
[2. Overview       ](#2-overview        )  
[3. Tree           ](#3-tree            )  
[4. Trunk          ](#4-trunk           )  
[5. Power Module   ](#5-power-module    )  
[6. Root           ](#6-root            )  
[7. Branch         ](#7-branch          )  

## 0. Release History

## 1. Introduction

- This document describes the electrical and mechanical specifications
for the Agathis gateway to provide developers with precise details to
understand its operation and build new modules, variants and systems.

- Audience: modules designers and systems implementers.

### 1.1. Terminology

This specification uses special CAPITALIZED keywords:

- **RULE**: a rule **SHALL** be followed to ensure compatibility. A
statement containing words **SHALL** or **SHALL NOT** is a rule.

- **RECOMMENDATION**: a recommendation enhances the usability of the
implementation.  A statement containing words **SHOULD** or **SHOULD
NOT** is a recommendation.

- **PERMISSION**: a permission clarifies the details that are not 
specifically prohibited.  A statement containing words **MAY** or
**MAY NOT** is a permission. 


## 2. Overview

## 3. Tree
### 3.1. Overview
- A *tree** is a stack of one power module, one or more root modules and
one or more branch modules; in general, throughout this document, the
word *tree* is equivalent with the word *system*.

+++ one or more diagrams to identify the modules, the cages, the trunk connectors, power rails and signal interfaces - NOTHING MORE THAN THIS

+++ explanation to said diagram

+++ controlling the modules (master-slave behaviors)

## 4. Trunk
[4.1.   Overview           ](#41-overview           )  
[4.2.   Mechanical Stack   ](#42-mechanical-stack   )  
[4.2.1. Cage and Fasteners ](#421-cage-and-fasteners)  
[4.2.2. Connectors         ](#422-connectors        )  
[4.3.   Electrical Stack   ](#43-electrical-stack   )  
[4.3.1. Connectors Pinout  ](#431-connectors-pinout )  

### 4.1. Overview
- The tree is the vertical mechanical and electrical connection stack;
it is made of the stacking cages, connectors and their associated PCB
features - essentially - what holds the tree together with the power and
signal distribution shared by the modules in a tree. 
--- insert a picture/diagram to identify the trunk elements.

### 4.2. Mechanical Stack
### 4.2.1. Cage and Fasteners
### 4.2.2. Connectors
- The up-trunk connector **SHALL** be QTE-060-0x-F-D-A 
manufacture by SAMTEC; where x stands for various stacking height
options.

- The down-trunk connector **SHALL** be of part number QSE-060-01-F-D-A 
manufacture by SAMTEC.

### 4.3. Electrical Stack
### 4.3.1. Connectors Pinout

```
Pin     Up-Trunk       Down-Trunk          
RefDes  Pin Name       Pin Name            Topology  Group      Description
                       (if different)                 
=============================================================================================================
A1      TRIG0                              TMDAD     TRIGGER    Tree MultiDrop Any Driver
A2      TRIG1                              TMDAD     TRIGGER    Tree MultiDrop Any Driver
A3      TRIG2                              TMDAD     TRIGGER    Tree MultiDrop Any Driver
A4      TRIG3                              TMDAD     TRIGGER    Tree MultiDrop Any Driver
A5      NOPP                               TMDPD     PWRSTAT    No Primary Power, driven by Power Module
A6      VSYS                               TPWR                 Tree Power
A7      GPIOA                              RT1BWP    GPIO       Root To 1 Branch With Promoting unused ports
A8      GPIOB                              RT1BWP    GPIO
A9      GPIOC                              RT1BWP    GPIO
A10     GPIOD                              RT1BWP    GPIO
A11     VSYS                               TPWR                 Tree Power
A12     GPIOE                              RT1BWP    GPIO       
A13     GPIOF                              RT1BWP    GPIO
A14     GPIOG                              RT1BWP    GPIO
A15     GPIOH                              RT1BWP    GPIO
A16     VSYS                               TPWR          
A17     I2CASCL        I2CBSCL             RTABAP    I2C        Root To All Branches Alternated Ports
A18     I2CASDA        I2CBSDA             RTABAP    I2C 
A19     I2CBSCL        I2CASCL             RTABAP    I2C 
A20     I2CBSDA        I2CASDA             RTABAP    I2C 
A21     V3P3           VDWN3P3             RTABPWR              Root To All Branches
A22     RGMIIRXD3      RGMIITXD3           MTM       RGMII      Module To Module
A23     RGMIIRXD2      RGMIITXD2           MTM       RGMII
A24     GND                                TPWR      
A25     RGMIIRXD1      RGMIITXD1           MTM       RGMII
A26     RGMIIRXD0      RGMIITXD0           MTM       RGMII
A27     GND                                TPWR      
A28     RGMIIRXCTL     RGMIITXCTL          MTM       RGMII
A29     GND                                TPWR      
A30     RGMIIRXCLK     RGMIITXCLK          MTM       RGMII
A31     GND                                TPWR      
A32     UARTACTS                           RT1BWP    UART       Root To 1 Branch With Promoting unused ports 
A33     UARTARTS                           RT1BWP    UART
A34     UARTARXD                           RT1BWP    UART
A35     UARTATXD                           RT1BWP    UART
A36     UARTBCTS                           RT1BWP    UART
A37     UARTBRTS                           RT1BWP    UART
A38     UARTBRXD                           RT1BWP    UART
A39     UARTBTXD                           RT1BWP    UART
A40     GND                                TPWR      
A41     UARTCCTS                           RT1BWP    UART
A42     UARTCRTS                           RT1BWP    UART
A43     UARTCRXD                           RT1BWP    UART
A44     UARTCTXD                           RT1BWP    UART
A45     UARTDCTS                           RT1BWP    UART
A46     UARTDRTS                           RT1BWP    UART
A47     UARTDRXD                           RT1BWP    UART
A48     UARTDTXD                           RT1BWP    UART
A49     GND                                TPWR      
A50     SDIOCLK                            RTAB      SDIO       Root To All Branches
A51     GND                                TPWR      
A52     SDIOCMD                            RTAB      SDIO
A53     SDIOD0                             RTAB      SDIO
A54     SDIOD1                             RTAB      SDIO
A55     SDIOD2                             RTAB      SDIO
A56     SDIOD3                             RTAB      SDIO
A57     SDIOD4                             RTAB      SDIO
A58     SDIOD5                             RTAB      SDIO
A59     SDIOD6                             RTAB      SDIO
A60     SDIOD7                             RTAB      SDIO
B1      VSYS                               TPWR      
B2      CLK10M                             TMDAD     FREQ
B3      VSYS                               TPWR      
B4      PPS                                TMDAD     TIME
B5      VSYS                               TPWR      
B6      UPADDR0        DNADDR0             RTAB      BCTRL      Branch Control
B7      UPADDR1        DNADDR1             RTAB      BCTRL
B8      UPADDR2        DNADDR2             RTAB      BCTRL
B9      UPGINT         DNGINT              RTAB      BCTRL
B10     UPAINT         DNAINT              RTAB      BCTRL
B11     UPAEN          DNAEN               RTAB      BCTRL
B12     UPLADDR0       DNLADDR0            MTNM      BCTRL      Module To Next Module
B13     UPLADDR1       DNLADDR1            MTNM      BCTRL
B14     UPLADDR2       DNLADDR2            MTNM      BCTRL
B15     SPIAMISO       SPIBMISO            RTABAP    SPI        Root To All Branches Alternated Ports
B16     SPIACS         SPIBCS              RTABAP    SPI
B17     SPIAMOSI       SPIBMOSI            RTABAP    SPI
B18     VSYS                               TPWR        
B19     SPIASCLK       SPIBSCLK            RTABAP    SPI
B20     VSYS                               TPWR      
B21     SPIBSCLK       SPIASCLK            RTABAP    SPI
B22     VUP3P3         VDN3P3              RTABPWR              Root To All Branches Power        
B23     SPIBMISO       SPIAMISO            RTABAP    SPI
B24     SPIBCS         SPIACS              RTABAP    SPI
B25     SPIBMOSI       SPIAMOSI            RTABAP    SPI
B26     GND                                TPWR      
B27     RGMIITXCLK     RGMIIRXCLK          MTM       RGMII
B28     GND                                TPWR      
B29     RGMIITXCTL     RGMIIRXCTL          MTM       RGMII      Module To Module
B30     GND                                TPWR      
B31     RGMIITXD3      RGMIIRXD3           MTM       RGMII
B32     RGMIITXD2      RGMIIRXD2           MTM       RGMII
B33     GND                                TPWR      
B34     RGMIITXD1      RGMIIRXD1           MTM       RGMII
B35     RGMIITXD0      RGMIIRXD0           MTM       RGMII
B36     GND                                TPWR      
B37     RSVD                               RESERVED  RESERVED
B38     RSVD                               RESERVED  RESERVED
B39     GND                                TPWR      
B40     USBGDP                             RT1BWP    USB        Root To 1 Branch With Promoting unused ports
B41     USBGDM                             RT1BWP    USB
B42     GND                                TPWR      
B43     USBFDP                             RT1BWP    USB
B44     USBFDM                             RT1BWP    USB
B45     GND                                TPWR      
B46     USBEDP                             RT1BWP    USB
B47     USBEDM                             RT1BWP    USB
B48     GND                                TPWR      
B49     USBDDP                             RT1BWP    USB
B50     USBDDM                             RT1BWP    USB
B51     GND                                TPWR      
B52     USBCDP                             RT1BWP    USB
B53     USBCDM                             RT1BWP    USB
B54     GND                                TPWR      
B55     USBBDP                             RT1BWP    USB
B56     USBBDM                             RT1BWP    USB
B57     GND                                TPWR      
B58     USBADP                             RT1BWP    USB
B59     USBADM                             RT1BWP    USB
B60     GND                                TPWR      
```



### 4.3.3. Power Management and Distribution

**OBSERVATION**: Primary power is applied from an external source
to the tree through the power module. The tree may store back-up energy
in batteries located in power module or branches. The batteries may be
used for back-up, for peak demands or as distributed power sources to
reduce voltage drop power rail.

**OBSERVATION** A tree has one power distribution rail VSYS (using GND
as return path) sourced in the power module and connected through and to
every module in the system.
--- insert support diagram ----

- The VSYS voltage **SHALL** be within 4.5V to 5.5V when the power 
module delivers from primary power for a loading current between 0 and 
specified maximum; this voltage range includes all impairments.

- The VSYS voltage **MAY** be within 2.75V to 5.5V when power module
delivers from battery for a loading current between 0 and specified
maximum; the battery maximum current MAY be lower than maximum current
while operating from primary power;  this voltage range includes all 
impairments.

- A module **SHALL** have all features operational when VSYS is between
3.2V and 5.5V.

- A module **MAY NOT** have all features operational for VSYS below
3.2V.

- The power module or a battery branch module **SHALL** limit the output
current into VSYS rail to 8A or less.

**OBSERVATION** this limitation is imposed by the thermal effect of the
finite contact resistance of the connector and associated PCB copper
features.

- The power module **SHALL** provide a backup supply that can last at 
least 60sec at its full rated current while maintaining VSYS above 3.2V.

**OBSERVATION**: this rule provides a minimum time for intelligent
modules to gracefully power-down.

- The maximum VSYS voltage vertical drop across a module and one 
connector contact **SHALL** be limited to 28mV for a total load of 8A.

**OBSERVATION**: the rule above is supported by the connector selection
(max 0.025 Ohm/ pin contact), pin current loading of 1A (8 pins are 
used to carry the VSYS), PCB recommended via of 10 mils diameter 1 
mil minimum plating, 63 mils PCB thickness produces a barrel resistance
of about 0.00132 Ohm and PCB recommended copper line from via to pin
soldering pad 16 mils wide and max 20 mils long produces a resistance
of about 0.00036 Ohm.
--- insert support diagram ----

- The maximum GND vertical voltage rise across one module and one 
connector contact **SHALL** be limited to 1mV for a total loading of 8A.

**OBSERVATION**: the rule above is supported by the connector selection
(max 0.0016 Ohm/ground blade contact, 3 blades in parallel, for
simplification, not counting the ground pins used for signal separation), 
pin current loading of 2.67A used to carry the VSYS), a recommended 
number of 10 PCB via per ground blade for a total of 30 via each of
less than 0.00132 Ohm with a negligible resistance from GND via to GND
pad; GND copper flooding in the connector GND pad is recommended.
--- insert support diagram ----

**OBSERVATION**: VSYS rail is susceptible to ripple noise injected by 
any module. This noise must be controlled at the system
level by limiting the amount injected by any card; good decoupling and
filtering practice should be sufficient, but actual noise performance
must be verified for a sound EMC design. 

- The quasi-peak value of the current ripple injected by a module into
the VSYS rail **SHALL** be less than 100mA over a frequency range from
50kHZ to 30MHz; the testing **SHALL** be done as specified in ANNEX A.


**OBSERVATION**: The tree system is susceptible to load step transients.
When a load on VSYS rail is turned on or off, the VSYS voltage will be
affected and the generated current loops may cause interference in other
parts of the system. These noises are optimally controlled by
coordinating the limits of the fast transients at the source (where the
load switching occurs) and the limits for the slow transients at the
power module).
--- insert support diagram ----

- The Power Module **SHALL** limit the over- and under-shoot from 
a load step transient from 0.1x nominal current to full nominal current
and vice-versa to *0.1V* and recover to less than *0.03V* from its
steady-state output voltage within *1ms*; the testing **SHALL** be done
as specified in ANNEX A2.

- A module **SHALL** limit its current transients into trunk VSYS rail
to 1A/10us*; the testing **SHALL** be done as specified in ANNEX A3.

**OBSERVATION**: - the load switching transients can be controlled by
using soft starting techniques or local decoupling capacitors for hard
switched loads; to size the decoupling capacitors one needs to take 
in consideration the finite connector contacts and PCB resistance of 
about 20 mOhm; for conservative designs, an isolation resistor may be
added.
--- insert support diagram ----

*OBSERVATION**: - Each root supplies its branches with a regulated
power over V*3P3 rail intended to feed the shared root/branches
interfaces with same voltage.
This V*3P3 rail has limited current capability and where applications
demand higher current, then the V3P3 voltage may be used as
reference for a down converter supplied from VSYS rail; in this
arrangement, the local converter would track the V3P3 rail and 
simplify the branch design with regard to power-up constraints.

**OBSERVATION**: - As a root behaves like a branch on the down-trunk
connector and as a root for the up-trunk connector, it will need two
separated V3P3 domains - one for the down-trunk (acting as a load) and
one for the up-trunk (acting as a source).
--- insert support diagram ----

A root **SHALL** supply VUP3P3 pin on up-trunk connector with 3.135V to 
3.465V for a current up to 800mA; this range includes all impairments.

**DEFINITIONS**: An *unmanaged branch* is a branch with one nominal level
of power consumption beside power-down level; a *managed branch* is a
branch with multiple levels of power consumption and capable to
negotiate its power consumption with its root.

An unmanaged branch **SHALL** draw less than 100mA from V3P3 rail.

A managed branch **MAY** negotiate up to 500mA after powering-up with
less than 100mA.

POWER MANAGEMENT - OPERATION

- The power module **SHALL** assert NOPP signal high when primary power
source is absent.

- A root or a branch **MAY** react to NOPP signal to adjust its power
consumption based on programmed power policies.

- A battery module (power or branch) **SHALL** transmit its
running parameter: VSYS voltage, VSYS current and battery remaining 
charge over I2C to the nearest root at one second or less interval.

- Every root **SHALL** keep the RGMII drivers for the up-trunk connector
Hi-Z or driven low until the up-trunk root asserts its PWRGOOD high.

- Every root **SHALL** keep the RGMII drivers for the down-trunk
connector Hi-Z or driven low until the down-trunk root VDWN3P3 is in
range.

**OBSERVATION**: the two rules above are meant to reduce root design
complexity related to unpowered devices protection.

- If VSYS is in operational range (3.2V to 5.25V) a root **SHOULD** be
able to communicate on down-trunk I2CA port.

- A root **SHALL** have its power states compatible with the following
diagram:

![alt text](root-power-states.png)

```
Legend:

Operational = uP and uC are both running
Sleep = uP is sleeping and uC is running
Power-Down = uP is powered-down, microcontroller running.
Power-Off = system power is down
SW Ctrl 1:   software command to uP to enter sleep mode
SW Ctrl 2:   interrupt from uC to uP to wake-up
SW Ctrl 3,4: software command to uC to turn-off power to uP.
SW Ctrl 5:   GINT signal from up-trunk asserted low or command over 
down-trunk I2C bus to uC to turn-on the power.
```

- A root **MAY** wake-up from sleep or power-down using, 
programmatically:
  - Falling slope of UPGINT
  - Falling slope of DNGINT
  - Rising slope of VDWN3P3
  - I2C command over down-trunk I2CA
  - internal timer
  
- A branch that consumes less than 100uA **MAY** stay operational
indefinitely.
  
- A branch that consumes more than 100uA **SHALL** have its power states
compatible with the following diagram:

![alt text](branch-power-states.png)

```
Legend:

Operational = all branch features are operational
Power-Down = main branch features are powered down.
Power-Off = system power is down
SW Ctrl 1:   software turn on branch power
SW Ctrl 2:   software turn off branch power

```

- A branch with current consumption over 100uA **SHALL** wake-up from or
go into power-down programmatically, using one or more of the following
sources:
  - trunk GEN signal (general enable)
  - trunk AEN signal (addressed enable)
  - trunk I2C command (over an I2C IO expander)
  - internal timer
  
**OBSERVATION** The detailed operation of the above signals is 
described in the Agathis Branch Specification chapter.
  
### 5.3. Signals Definition and Usage

#### 5.3.1. TRIGGER[0..3] Bus

**OBSERVATION**: The TRIGGER bus is intended to provide simple 
synchronization across entire tree. 

- TRIGGER[0..3] signals **SHALL** have their up-trunk and down-trunk
respective pins connected together on each module, forming a parallel
multi-drop bus.

- TRIGGER[0..3] signals **SHALL** be of CMOS levels supplied from VSYS rail.

**OBSERVATION**: using CMOS levels referred to VSYS rail allows TRIGGER
signals to be available to any module when the tree is supplied with 
VSYS; this simplifies the driver and receiver design in a system where
drivers may be active and receivers not Hi-Z from power supply.

- TRIGGER0 and **SHALL** be capable to wake-up any module in the system.

- TRIGGER sources **SHALL** be coordinated by the software to avoid bus
contention.

- TRIGGER signals **SHALL** be of maximum duration of 100ns.

- RECOMMENDATION: a relatively easy way to implement the rules above is 
to use the TXB0104, a bidirectional Voltage-level Translator With 
Automatic Direction Sensing; the local voltage **SHALL** be connected to 
VCCA and the VSYS connected to VCCB.

#### 5.3.2. GPIOA,B,C,D,E,F,G,H

**OBSERVATION**: The GPIO signals are intended to provide simple
unstructured signaling between a root and its branches.

- The root **SHALL** present up to 8 signals to the GPIO pins of the 
up-trunk connector.

**OBSERVATION**: the GPIO signals are point to point, with one point on the 
root and the other point one branch; a branch may consume one or more
GPIO signals; the GPIO signals may not be available to all branches
belonging to a root.

- If GPIO signals are used (consumed) by a branch, they **SHALL** form a
contiguous group starting with GPIOA pin from its down-trunk connector;
the unused signals **SHALL** be routed orderly to the GPIO pins on the 
up-trunk connector starting with GPIOA.

- A root or a branch **SHALL** NOT drive a GPIO high when the V3P3 rail is 
down.

- The logic levels for the GPIO signals **SHALL** be LVCMOS supplied from 
V3P3 rail.


- A root **MAY** use its GPIO pins on the down-trunk connector for testing
purposes


- A root **SHALL** follow all branch rules for the down-trunk signaling.


#### 5.3.3. I2C
 
**OBSERVATION**: I2CA and I2CB pins on the trunk connectors are intended to
provide two I2C independent buses between a root and its branches.

- Every branch **SHALL** connect down-trunk I2CA to up-trunk I2CB and 
down-trunk I2CB to up-trunk I2CA.

- Every branch **SHALL** connect half of its I2C devices to I2CA pins on 
down-trunk connector and the other half to I2CB on down-trunk connector; 
the remainder **SHALL** be connected to I2CA on down-trunk connector.

**OBSERVATION**: the two rules above support I2C traffic and loading
balancing.

- Every root **SHALL** master both I2C buses on its up-trunk connector.

- Every root **SHALL** follow the branch rules for the I2C interface with
the exception on the down-trunk to up-trunk connection (Hi-Z).

- Every root **SHALL** operate the down-trunk I2C from VDWN3P3.

- A root **MAY** master I2CA on the down-trunk connector.

- A branch **MAY** master any of the I2C buses.

- The two I2C buses **SHALL** run from V3P3 sourced by the root module.

**OBSERVATION**: if the root has its V3P3 powered down, then the I2C is
down.

**OBSERVATION**: the I2C pull-up resistors, capacitive loading and maximum
clock speed are correlated; the following rule is intended to optimize
the speed of the I2C bus.

- Every module **SHALL** have the I2C buses they use provided with pull-up
resistors equivalent to a parallel 200K resistor for each picofarad of
capacitive bus loading.

**OBSERVATION**: the capacitive loading can be determined by actual direct 
or indirect measurement or by adding the pin capacitance for each device
from their data sheet and the estimated PCB capacitance; the actual 
resistor value should be chosen obtained by rounding down to the nearest
E96 value.

- Every module **SHALL** provide the values of the pull-up resistors and 
parasitic capacitance in the the module's ID EEPROM and module's 
datasheet.

- The I2C operating speed **SHALL** be limited to 400kHz.

- A module **SHOULD** only use 400kHz capable I2C devices.

- Every module **SHALL** use only devices with I2C address bits A2,1,A0
available on their pinout and wired respectively to LADDR2,1,0 on the
down-trunk connector.

- Every module **SHALL** have one 256x8 I2C bit EEPROM written once
in production line, read only in normal operation, connected to I2CA on
down-trunk connector. This memory **SHALL** be of model 24LC02B
manufactured by Microchip or equivalent.

**OBSERVATION**: this memory is intended to contain module part number, 
version, serial number and hardware characteristics.

- Every module **SHOULD** have a second (4096x8 bit of higher) I2C EEPROM
for read/write normal operations. This memory **SHOULD** be of model 
24LC32A/24LC64/24LC128/24LC256/24LC512 manufactured by Microchip or
equivalent.

**OBSERVATION**: This memory is intended to store module variable operating 
parameters, firmware release, etc.




**Root Definition**: the hardware between down-trunk and up-trunk connector
that complies with the root related rules outlined by this 
specification.



- **Tree:** is a stack of one power module, one or more root modules and
one or more branch modules; herein the word tree is equivalent to 
system.

- **Power module:** adapts and stores external energy for tree to use;
it may include Real Time Clock, Ethernet, PoE and Test functions. 
There is one and only one power module in a tree and it always occupies
the first position in the stack.

- **Root:** is a module that controls the modules stacked above, 
inclusive to another root; there is at least one root in a tree, 
stacked on top of the power module; the root is the brain of the tree; 
if more brain power is needed, then multiple roots can be stacked 
together. A root behaves as a branch for the root below.

- **Branch:** is a module stacked above a root or another branch; 
its main functions are to connect the tree to the external world or to 
provide internal features to the gateway.

- **Module:** generic name given to an electronic assembly made of one
or more printed circuit assemblies; the types of modules in the Agathis
tree are power, root and branch.



