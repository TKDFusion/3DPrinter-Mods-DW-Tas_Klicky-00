[![CC BY-NC-SA 4.0][cc-by-nc-sa-shield]][cc-by-nc-sa]

# Klicky-00: Zero X,Y offset probe (RC3)

Building on the amazing work of JosAr ([Klicky Probe](https://github.com/jlas1/Klicky-Probe)), whoppingpochard ([PCB Klicky](https://github.com/tanaes/whopping_Voron_mods/tree/main/pcb_klicky)), and Majarspeed ([Unklicky](https://github.com/majarspeed/Unklicky)) this mod moves the probe directly under the nozzle (X,Y 0,0) and also has the nozzle touching the probe so that you can reliably use it as your z endstop with consistent z-offset. All the usual caveats about clean nozzles during probing apply here too.

The goal of this probe is to give accurate, nozzle probe-like, repeatable Z-offset on a budget even when changing nozzles.

![render](images/Klicky-00_RC2_render.png)
<br/> <br/>
![alt text](images/Klicky-00.6.png)
<br/> <br/> <br/> <br/>
> [!NOTE]  
> You can help support the development of Klicky-00.<br/>
> Click on the Ko-Fi image below.<br/>

[![ko-fi](images/kofi_bg_tag_white.png)](https://ko-fi.com/O5O5OCC0K)

<br/> <br/> <br/>


#### Constraints:
* Low cost
* Easy access to required parts
* Simple add-on to existing ecosystems

### Currently in "release candidate (RC)" status
Versions have been community tested on Xol Toolhead, Archetype and Stealthburner. Many gremlins have been worked out already, but things are still being found as more and more people join the fun of Klicky-00.

### Discussion and development on the Armchair discord

[![Join us on Discord](https://discord.com/api/guilds/1029426383614648421/widget.png?style=banner2)](https://discord.gg/armchairengineeringsux)<br/>
Find the [Klicky-00 thread](https://discord.com/channels/1029426383614648421/1101496347540082799) under "user-projects"

#### RC3 - 01/01/2025
![Buckshot transparent](images/Klicky-00.9.png)
* Swingarm fixes for better location of probe under nozzle
* Changed Buckshot switches to use FHCS screws
* CAD fixes

#### RC2 - 05/05/2024
* Changed swingarm hinge screws to M3 (no more M2.5 screws needed)
* Increased strength around hinge points
* Moved D2F switch location to properly match 0,0 concept
* `New Switch Type` `Beta` Buckshot switch by ZaMarin <br/><br/>
  ![buckshot switch](images/buckshot_switch.png)

### Use 6mm x 3mm magnets
I have designed this around 6x3mm magnets and it will probably fail with the 6x2.7mm magnets that are also common. A mix of N52 and N35 magnets are most likely needed to help "tune" attraction and spring forces.

### Build Guide
Go to the [instructions](instructions.md)


### But why another probe?
Like many others, I installed Voron TAP and loved the consistency, repeatability and user experience, but I didn't like the extra complexity, weight and instability added to the toolhead.
I had previously used KlickyNG with auto-z calibration scripts and while that was good, I ALWAYS had to watch the first layer and make micro-adjustments to Z offset.

This probe takes the reliable docking hardware and software of the PCB Klicky and the high accuracy of the Unklicky BFP and puts them in contact with the probe for repatable z-offset and zero XY offset.

Initial testing in a Voron 2.4R2(300mm) with Xol-Toolhead looks promising.
probe_accuracy standard deviation results vary from 0.0005 to 0.0025 on my printer and that is similar to what I got with TAP.

Drift was also very low with bed temp at 118°C, nozzle 200°C and chamber ~57°C

![repeatability_test](images/20230415_1609_repeatability_test.png)
![drift_test](images/20230415_1609_drift_test.png)

### Credits:
* ZaMarin - For the Buckshot switch mechanism, and inspiring the linkage design that unlocked Klicky-00s potential and the continued help behind the scenes.


### References:
* [Klicky Klipper macros](https://github.com/jlas1/Klicky-Probe/tree/main/Klipper_macros)
* [Unklicky build guide](https://github.com/majarspeed/Unklicky/blob/main/Build%20Guide.md)
* [Voron Docs Klicky as Z-endstop](https://docs.vorondesign.com/community/howto/Takuya/Klicky_Probe_AutoZ_Alternative.html)

<br/><br/><br/><br/>
This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg
