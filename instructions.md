# Build Instructions

> [!WARNING]
> You need to have a good understanding of Klicky (+macro settings), probes, offsets and Klipper.

It is highly recommended to have a working PCB Klicky or standard Klicky already installed on your toolhead and configured. Follow the instructions from Josar on the Klicky-Probe Github:
[klipper configuration](https://github.com/jlas1/Klicky-Probe/tree/main/Printers/Voron/v1.8_v2.4_Legacy_Trident#step-5-klipper-configuration) `<br/>`
Make sure to include the steps for [Klicky Probe as Endstop with constant Z-Offset](https://github.com/T4KUUY4/Voron-Stuff/tree/main/KlickyProbeZoffset).

> [!IMPORTANT]
> Klicky-00 is a Loooong probe. It doesn't fit behind the print bed of a standard Voron 2.4 or Trident build without a dock that retracts the probe. See "Bump dock" instructions below.
> `Should be OK with StealthBurner version as the probe is ~5.5mm shorter`

> [!WARNING]
> You need at least 5mm travel on Y past the back of your build plate for this to work.

## Klicky-00 Probe

The probe is built from components of other projects. The original concept of this project is putting the probe under the nozzle in a repeatable/automatable way.

## BOM

The first two tables are specific to the mount type you use. The third table has extra BOM depending on switch type.

### PCB Klicky Version (needed for all switch types)

`[Assumes you already have the PCB Klicky upper mount on your toolhead]`

| Qty | Item                   | Note                                                                                                    |
| --- | ---------------------- | ------------------------------------------------------------------------------------------------------- |
| 1   | PCB Klicky Lower kit   | Lower PCB with switch removed, magnets, screws and heatset inserts that came with the kit or equivalent |
| 5   | 6x3mm Disc Magnets     | Probably a mix of N52 and N35 strength for adjustability                                                |
| 4   | M3 x 20mm SHCS or BHCS | Swing arm hinges                                                                                        |
| 2   | Lengths of wire        | Less than 2mm sheathing diameter, approx 100mm                                                          |

### Standard Klicky Version (needed for all switch types)

`[Assumes you already have the Klicky mount on your toolhead]`

| Qty | Item                   | Note                                                     |
| --- | ---------------------- | -------------------------------------------------------- |
| 8   | 6x3mm Disc Magnets     | Probably a mix of N52 and N35 strength for adjustability |
| 4   | M3 x 20mm SHCS or BHCS | Swing arm hinges                                         |
| 2   | Lengths of wire        | Less than 2mm sheathing diameter, approx 100mm           |

### Extra parts by switch type

| Switch Type | Qty | Item                                                                             | Note                                                                                       |
| :---------- | --- | -------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------ |
| Buckshot    | 3   | M3 x 8 FHCS `M3 x 6 FHCS will work`                                              | Brass version from Ali Express (https://www.aliexpress.com/item/1005004957093547.html)     |
| Buckshot    | 1   | 5.5m Ball Bearing                                                                | Known good source from Ali Express (https://www.aliexpress.com/item/1005005046697375.html) |
| Buckshot    | 1   | Spring: <br/>* Length: 10mm<br/>* Wire Diameter: 0.4mm<br/>* Outer Diameter: 4mm | Known good source from Ali Express (https://www.aliexpress.com/item/1005007100755870.html) |
| Unklicky    | 1   | M3 x 12mm SHCS                                                                   | Unklicky probe stylus retention screw                                                      |
| D2F         | 1   | D2F switch                                                                       | No lever                                                                                   |
| D2F         | 2   | M2 x 10mm self tapping countersunk screws                                        |                                                                                            |

## Printed Parts
Pick your toolhead, switch type and mount type from the tables below to find the correct file to print

#### A4T or Xol-Toolhead
|          | Klicky PCB                                                         | Klicky Standard                                                          |
| -------- | ------------------------------------------------------------------ | ------------------------------------------------------------------------ |
| Buckshot | [A4T-Xol - Buckshot - PCB.stl](<STL/A4T-Xol - Buckshot - PCB.stl>) | [A4T-Xol - Buckshot - Klicky.stl](<STL/A4T-Xol - Buckshot - Klicky.stl>) |
| Unklicky | [A4T-Xol - Unklicky - PCB.stl](<STL/A4T-Xol - Unklicky - PCB.stl>) | [A4T-Xol - Unklicky - Klicky.stl](<STL/A4T-Xol - Unklicky - Klicky.stl>) |
| D2F      | [A4T-Xol - D2F - PCB.stl](<STL/A4T-Xol - D2F - PCB.stl>)           | [A4T-Xol - D2F - Klicky.stl](<STL/A4T-Xol - D2F - Klicky.stl>)           |
#### Archetype
|          | Klicky PCB                                                             | Klicky Standard                                                              |
| -------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| Buckshot | [Archetype - Buckshot - PCB.stl](<STL/Archetype - Buckshot - PCB.stl>) | [Archetype - Buckshot - Klicky.stl](<STL/Archetype - Buckshot - Klicky.stl>) |
| Unklicky | [Archetype - Unklicky - PCB.stl](<STL/Archetype - Unklicky - PCB.stl>) | [Archetype - Unklicky - Klicky.stl](<STL/Archetype - Unklicky - Klicky.stl>) |
| D2F      | [Archetype - D2F - PCB.stl](<STL/Archetype - D2F - PCB.stl>)           | [Archetype - D2F - Klicky.stl](<STL/Archetype - D2F - Klicky.stl>)           |
#### StealthBurner
|          | Klicky PCB                                                                     | Klicky Standard                                                                      |
| -------- | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| Buckshot | [StealthBurner - Buckshot - PCB.stl](<STL/StealthBurner - Buckshot - PCB.stl>) | [StealthBurner - Buckshot - Klicky.stl](<STL/StealthBurner - Buckshot - Klicky.stl>) |
| Unklicky | [StealthBurner - Unklicky - PCB.stl](<STL/StealthBurner - Unklicky - PCB.stl>) | [StealthBurner - Unklicky - Klicky.stl](<STL/StealthBurner - Unklicky - Klicky.stl>) |
| D2F      | [StealthBurner - D2F - PCB.stl](<STL/StealthBurner - D2F - PCB.stl>)           | [StealthBurner - D2F - Klicky.stl](<STL/StealthBurner - D2F - Klicky.stl>)           |
#### Extras
| File                                                                                                                      | Description                                                                                                         |
| ------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| [StealthBurner - Klicky_Toolhead_Mount.stl](<STL/StealthBurner - Klicky_Toolhead_Mount.stl>)                              | Klicky mount to use with standard StealthBurner carriage when using the "standard Klicky" mount type with Klicky-00 |
| [Klicky-00_SLM_Nozzle_Plate.stl](<STL/SLM Nozzle Plate/Klicky-00_SLM_Nozzle_Plate.stl>)                                   | SLM Strike plate version for A4T or Xol-Toolhead                                                                    |
| [Klicky-00_A4T-Xol_Buckshot_Front-Strike_SLM.stl](<STL/SLM Nozzle Plate/Klicky-00_A4T-Xol_Buckshot_Front-Strike_SLM.stl>) | SLM Strike plate version for A4T or Xol-Toolhead                                                                    |

## Instructions (PCB_Klicky Version with Unklcy switch)
| Note                                                                                                                                                                                                                                                                                                                      | Picture                                         |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------- |
| Remove the built in support                                                                                                                                                                                                                                                                                               | ![Alt text](images/probe_remove_support.png)      |
| Install the M2 heatset inserts                                                                                                                                                                                                                                                                                            | ![Alt text](images/probe_install_heatsets.png)    |
| If an M3 screw placed through the swing arms doesn't move freely with low friction, drill out the swing arm holes with M3 drill bit.<br/>`Don't over do it! If the screws have too much room the probe will end up wobbly and not be as accurate.`                                                                           | ![Alt text](images/probe_drill_arms.png)          |
| Prepare the probe stylus. Sand it down so it moves smoothly inside the probe front body `Unklicky Version`                                                                                                                                                                                                              | ![Alt text](images/probe_prepare_stylus.png)      |
| Install the stylus as per UnKlickyBFP. Wire wraps around top of stylus, Magnets are opposing<br/>`*TIP: Make sure that the top magnet repells the furthest back magnet on the toolhead. This will make sure that Klicky-00 is pushed down as the toolhead moves over it to attach the probe.`                                | ![Alt text](images/probe_install_stylus.png)      |
| Put the screw in most of the way. Leave room for the second wire to wrap around                                                                                                                                                                                                                                           | ![Alt text](images/probe_install_stylus2.png)     |
| Put the left side wire in place, wrapped around the screw and tighten the screw                                                                                                                                                                                                                                           | ![Alt text](images/probe_wire_left.png)           |
| Install the front two swing arm screw hinges                                                                                                                                                                                                                                                                              | ![Alt text](images/probe_attach_arms1.png)        |
| Install a magnet in the back of the lower swing arm                                                                                                                                                                                                                                                                       | ![Alt text](images/probe_lower_arm_magnet.png)    |
| Install the other two swing arm screws                                                                                                                                                                                                                                                                                    | ![Alt text](images/probe_attach_arms2.png)        |
| Solder the probe wires to the bottom of the PCB Klicky lower PCB. One in the front, one at the back. Middle hole stays empty                                                                                                                                                                                              | ![Alt text](images/probe_solder_wires.png)        |
| Install the magnets that live under the PCB. The rear one should attract to the dock, the other should repel the lower swing arm. You may need to swap between N35 and N52 magnets to get just enough spring force to activate the swing arm. Too much won't let the arm move and will push the klicky PCB magnets apart. | ![Alt text](images/probe_rear_body_magnets.png)   |
| Install the Klicky PCB magnets with the counter sunk screws. Get your polarity right.                                                                                                                                                                                                                                     | ![Alt text](images/probe_install_pcb_magnets.png) |

## Instructions (Stanrad Klicky Version)

[Todo (sorry)]

# Bump dock

![Alt text](images/bump_dock.png)
In the spirit of Unklikcy, this atrocity is put together out of things that hopefully you have laying around as spare parts.

Like the rest of Klicky-00, magnets are used as "springs" because they're magic.

## BOM

| Qty     | Item              | Note                                                                  |
| ------- | ----------------- | --------------------------------------------------------------------- |
| 2       | M5 x 16 BHCS      | Attaching to gantry                                                   |
| 2       | M5 T-Nuts         | Attaching to gantry                                                   |
| 1       | M3 Heatset Insert | Standard Voron spec. In the height adjuster-a-thingy                  |
| 1       | M3 x 30 SHCS      | Height adjustment screw                                               |
| 2       | M3 Heatset Insert | Standard Voron spec. In the front of the klicky dock hoder            |
| 2       | 36mm PTFE Tube    | 2mm ID / 4mm OD PTFE Tube: lower hinges                               |
| 3       | 40mm PTFE Tube    | 2mm ID / 4mm OD PTFE Tube: Middle hinges + Bump slide                 |
| 2       | 30mm PTFE Tube    | 2mm ID / 4mm OD PTFE Tube: Upper hinges                               |
| 5 or 10 | 6x3mm Magnets     | Depending on how strong the magnets are: the "Springs" for the bumber |
| 2       | M3x20 SHCS        | Klicky dock to bump dock                                              |
| 1       | 6x3mm Magnet      | Behind Klicky dock                                                    |

## Instructions

| Note                                                                                                                                                                                                                                                                                                      | Picture                                                                                           |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| Install heatset inserts:<br/> * Lower arm and height adjuster                                                                                                                                                                                                                                                | ![Alt text](images/bump_dock_heatsets.png)   <br/>  ![Alt text](images/bump_dock_height_adj_heatset.png) |
| Put the dock arms together with the PTFE tube in the upper and lower hinges. Don't forget the other PTFE tube on the front of the bumper!                                                                                                                                                                 | ![Alt text](images/bump_dock_assemble_arms.png)                                                     |
| Slide the arms into place in the body and put the two middle hinge PTFE tubes in place                                                                                                                                                                                                                    | ![Alt text](images/bump_dock_assemble_dock.png)                                                     |
| Thread the height adjustment screw into the height adjuster and clip it into place                                                                                                                                                                                                                        | ![Alt text](images/bump_dock_height_adj.png)                                                        |
| Attach the Klicky dock to the bump dock. Don't forget the magnet and it's polarity if you have existing probes                                                                                                                                                                                            | ![Alt text](images/bump_dock_klicky-dock.png)                                                       |
| Install Magnets to be the "springs" and "latch"<br/> Depending on how strong your magnets are, and how well everything moves, you may only need these magnets on one side. The top three magnets are setup to push the upper arm forward and the lower two magnets attract to pull the lower part backwards. | ![Alt text](images/bump_dock_springs.png)                                                           |
| Time to install it into the printer.                                                                                                                                                                                                                                                                      | ![Alt text](images/bump_dock_into_printer.png)                                                      |
