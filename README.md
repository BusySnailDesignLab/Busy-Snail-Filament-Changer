# Busy Snail Filament Changer (BSFC)

![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/BSFC_spool_unit_animcut.gif)




## One More Filament Changer Design?

A filament changer supporting 5kg spools that uses large extruder gears to reliably pull filament from heavy spools didn't seem to exist when starting the project (or at least couldn't find an open source one).

Features that were targeted in the design process:

- Support for larger than 1kg spools up to 5kg
- Extruder and spool rewind function operated per spool unit by the same stepper motor
- NEMA17 stepper motors for power and speed
- Large extruder gears to maximize filament traction
- As modular system as possible where components are connected to each other by threaded rods
- Possibility to use only 1 spool unit as a loader/unloader/assisting extruder rather than a changer
- Keeping the BOM as light as possible with fairly easily accessible items

[YouTube playlist](https://www.youtube.com/playlist?list=PLjJb97KCYTC8oeRxWj5jBiS8WIRQJnpdh) of BSFC prototyping and testing videos.


<br/>

## Public Beta 2026.06

The Busy Snail Filament Changer is transitioning from closed testing to the wider community in June 2026. This public beta release represents what should be the final design. The core architecture is locked, though minor adjustments may still occur.

<br/>

## 3d-files and Printing

The files and info needed for the basic setup are available in this root directory, everything else can be found in the MODs folder.
Provided STL files are in their intended printing orientation, and bed adhesion helpers and supports are modeled in the files. Also, STEP files of assemblies are provided with and without modeled printing helpers to allow one to adjust or modify if wished.

Prototyping was done using PLA and PETG filaments. There are some areas in some of the parts with some fairly thin walls where using ABS might be challenging due to its generally poorer layer adhesion, resulting in parts too delicate.

As is usually the case with projects of this nature, the 3D printer and slicer print profiles must be properly calibrated. The clearances of the printed parts have been designed and tested based on this assumption.

[Ellis' Print Tuning Guide](https://ellis3dp.com) is naturally the place to go when things don't fit together.

<details>
<summary>Some print settings used in the design process</summary>



</details>

<br/>

## Technical Details and Build

This section with illustrations currently serves as a BSFC building manual. Each subsection contains also a link to the corresponding tutorial video on YouTube.

Slight differences may exist between the printed components shown in the illustrations or videos and the current STLs, as development continued during and after content creation.



<details>
<summary>Rewind clutch</summary>

<br/>

The rewind clutch is closely related to the traditional freecoaster rear hub used on BMX bicycles.
<br/>

When the stepper motor rotates in the feed/extrude direction, the clutch disengages; the clutch gear freewheels, allowing the spool rewind roller to rotate freely. In the rewind/retract direction, the clutch engages and the spool is rewound.
<br/>

The friction of the spring-loaded conical interface must be greater than the friction of the engager component's steep thread. The spring should not be adjusted too tight; however, an adjustment that is too loose will prevent the clutch from operating.
<br/>

For the clutch to function properly, a small amount of silicone grease must be applied to its contact surfaces.
<br/>

[Assembly video](https://youtu.be/TbNA-HyEh_M?si=HdrPlAlg6tBJTh0d) on YouTube.

<br/>

![bsfc_build_clutch_cut.jpg](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_clutch_cut.jpg)
![bsfc_build_clutch_cut.jpg](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_clutch_expl.jpg)

</details>




<details>
<summary>Spool controller</summary>

<br/>

Since the extruder and rewind gear train have a fixed gear ratio, the system is optimized for nearly empty spools to ensure sufficient rewind tension. Because of this, a fuller spool naturally has a higher peripheral velocity than an emptier one, meaning some slippage must occur between the roller and the spool. When the spool attempts to move faster than the retracted filament allows, it climbs against the spool controller and slips slightly, resulting in a constant "micro-jumping" effect.
<br/>

The chosen approach was to maximize the grip between the roller and the spool using a butyl rubber inner tube, then manage the necessary slippage through the spool controller. This method proved to be the only viable solution, as the grip of a 5kg spool on the roller is exceptionally strong.
<br/>

The height of the spool controller is adjusted by rotating the thumbwheel, which stays in position due to the worm gear construction. If the controller is set too low, the spool will slip excessively and fail to rewind properly. Conversely, if it is set too high, the jumping motion becomes too aggressive. Fortunately, the optimal adjustment has a fairly large tolerance for the rewind function to work reliably.
<br/>

[Assembly video](https://youtu.be/K6IZ9RyGhMk?si=yHqPg5wZYAanlQJ6) on YouTube.

<br/>

![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_spool_controller_cut.jpg)
![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_spool_controller_expl.jpg)

</details>




<details>
<summary>Drive unit</summary>

<br/>

The drive unit is in a way divided into two functional sections: motor/rewind and extruder section.
<br/>

[Assembly video](https://youtu.be/VoX7NNussHw?si=F9h9A9wVGLavogpF) on YouTube.

<br/>

Whole unit
![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_drive_unit_expl_1.jpg)
Motor/rewind section
![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_drive_unit_block_motor_expl_1.jpg)
![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_drive_unit_block_motor_expl_2.jpg)
![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_drive_unit_block_motor_expl_3.jpg)
Extruder section
![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_drive_unit_block_extruder_expl_1.jpg)
![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_drive_unit_block_extruder_expl_2.jpg)

</details>




<details>
<summary>Roller tray</summary>

<br/>

[Assembly video](https://youtu.be/v3EZafkdpoI?si=Pa8eA2tnM2RYGXaa) on YouTube.

<br/>
 
![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_roller_tray_expl_1.jpg)
![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_roller_tray_expl_2.jpg)

</details>




<details>
<summary>Hub-buffer</summary>

<br/>

[Assembly video](https://youtu.be/KklAEr8crc0?si=6_zTUBbSNkeF0NI5) on YouTube.

<br/>
 
![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_hub_buffer_cut.jpg)
![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_hub_buffer_expl_1.jpg)
![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_hub_buffer_expl_2.jpg)
![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_hub_buffer_expl_3.jpg)
![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_hub_buffer_expl_4.jpg)

</details>




<details>
<summary>Control board box</summary>
	
<br/>

The control board box currently supports Bigtreetech MMB CAN V1 and V2 boards. The box is sized to accommodate both board versions, with each having its own dedicated mounting bracket.
<br/>

[Assembly video](https://youtu.be/oLnCz8qqsjE?si=0IGYUk-QMdZsbvs8) on YouTube.

<br/>

![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_control_board_box_expl_1.jpg)
![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_control_board_box_expl_2.jpg)

</details>




<details>
<summary>General assembly</summary>
	
<br/>

The finished device consists of components connected by threaded rods.<br/>

<br/>

</details>

[YouTube playlist](https://www.youtube.com/playlist?list=PLjJb97KCYTC9PMECO4NPdOToGcQD9c51B) of current BSFC tutorial videos.

<br/>

## Software Configuration

Work in progress. <br/>
BSFC prototyping was done using [AFC-Klipper-Add-On](https://github.com/ArmoredTurtle/AFC-Klipper-Add-On) and using its [documentation](https://www.armoredturtle.xyz/docs/afc-klipper-add-on/index.html) to set things up. Compatibility with [Happy-Hare](https://github.com/moggieuk/Happy-Hare) has not yet been tested.

<details>
<summary>Some AFC-Klipper-Add-On config settings</summary>

<br/>

These settings instead of the default values were used in .cfg files when prototyping BSFC:

- rotation_distance: 24.84
- run_current: 1.7

<br/>

- long_moves_speed: 300
- long_moves_accel: 150
- short_moves_accel: 150
- global_print_current: 0.8

<br/>

Pin mappings for Bigtreetech mmb can v1.1 control board:

/config/AFC/mcu/MMB_1.1.cfg

```
[board_pins Busy_Snail]
mcu: Busy_Snail
aliases:
    M1_STEP=PB15   , M1_DIR=PB14   , M1_EN=PB8    , M1_UART=PA10   , # M1_DIAG=PA3   ,
    M2_STEP=PD2    , M2_DIR=PB13   , M2_EN=PD1    , M2_UART=PC7    , # M2_DIAG=PA4   ,
    M3_STEP=PD0    , M3_DIR=PD3    , M3_EN=PA15   , M3_UART=PC6    , # M3_DIAG=PB9   ,
    M4_STEP=PB6    , M4_DIR=PB7    , M4_EN=PB5    , M4_UART=PA9    , # M4_DIAG=PB8   ,

	HUB=PB11 		, 
	TRG1=PA3  		, TRG2=PA4  	, TRG3=PB9 		, TRG4=PA8		,
	EXT1=PC15 		, EXT2=PC13		, EXT3=PC14		, EXT4=PB12		,
    TN_ADV=PB10     , TN_TRL=PB2 ,
    
	# MOT1_RWD=PA0	, 
	# MOT2_RWD=PA1	, 
	# MOT3_RWD=PB10	, 
	# MOT4_RWD=PB2	, 
	
	RGB1=PA2		, 
```


</details>

<br/>

## Financial Aspects

When you do something as a hobby, it’s pure fun. The hours don’t matter because there are always too few—you know that feeling when you completely lose track of time? But what about the expenses? Well, who on earth would remember those... 

Yet somehow, in a strange way, those costs tend to add up when prototyping. If you’ve enjoyed or benefited from this project, I would be incredibly grateful for a small contribution to help cover some of the expenses involved.

<a href="https://www.buymeacoffee.com/busysnaildesignlab"><img src="https://img.buymeacoffee.com/button-api/?text=Filament_and_Bits_and_Bobs&slug=busysnaildesignlab&button_colour=FFDD00&font_colour=000000&font_family=Cookie&outline_colour=000000&coffee_colour=ffffff" /></a>


<br/>

## Bill of Materials Kits

[Mellow](https://3dmellow.com/products/) has expressed interest in offering a BSFC BOM kit. There is no date yet for when it will be available. When it is released, a link will be provided here.
