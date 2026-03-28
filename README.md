# Busy Snail Filament Changer (BSFC)

![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/BSFC_spool_unit_animcut.gif)




## One more filament changer design?
A filament changer supporting 5kg spools that uses large extruder gears to reliably pull filament from heavy spools didn't seem to exist when starting the project (or at least couldn't find an open source one).

Features that were targeted in the design process:

- Support for larger than 1kg spools up to 5kg
- Extruder and spool rewind function operated per spool unit by the same stepper motor
- NEMA17 stepper motors for power and speed
- Large extruder gears to maximize filament traction
- As modular system as possible
- Possibility to use only 1 spool unit as a loader/unloader/assisting extruder rather than a changer
- Keep the BOM as light as possible with fairly easily accessible items




<br/>

## From proto to closed beta
Prototyping has been done and everything is working nice. It's time to move to closed beta testing to ensure that STLs, BOM and wiring are all spot on before the public release.
The completed STEP files will be available at the time of the public release of BSFC. This ensures that possible upcoming user mods are based on the actual final released version.
<br/><br/>
Welcome to the Busy Snail Filament Changer private closed beta repository! <br/><br/>
<ins>***By downloading closed beta files from here, you agree to not share them anywhere.***</ins> Since minor changes are still possible, we don't want pre-release files floating around the internet.




<br/>

## Technical details and build

This section with illustrations currently serves also as a BSFC building manual.




<details>
<summary>Rewind clutch</summary>

<br/>
Rewind clutch is closely related to the traditional freecoaster rear hub of a BMX bicycle. <br/>
When the stepper motor rotates in the filament feed/extrude direction, the clutch is disengaged and clutch gear freewheels and spool roller also rotates freely.
In the rewind/retract direction, the clutch is engaged and the spool is rewound. 
<br/> <br/>
Spring-loaded conical interface's friction must be greater than the sparse thread’s friction of the engager component.
It is not beneficial for the spring to be adjusted too tight, but too loose an adjustment will prevent the clutch from operating. <br/>
For the clutch to function properly, a small amount of silicone grease must be applied to its contact surfaces.
<br/><br/>
 
![bsfc_build_clutch_cut.jpg](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_clutch_cut.jpg)
![bsfc_build_clutch_cut.jpg](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_clutch_expl.jpg)

</details>




<details>
<summary>Spool controller</summary>

<br/>
Since the extruder and rewind gear train have a fixed gear ratio, it has to be optimized for almost empty spools to achieve acceptable rewind tightness (angular vs. peripheral velocities).
Fuller spool has then higher peripheral velocity than emptier spool and some slipping must exist between the roller and the spool.
When spool tries to have higher peripheral velocity than rewinded filament from extruder allows it climbs to the spool controller and slips a bit (does this micro jumping constantly).
<br/> <br/>
The chosen approach was to get the best possible grip between the roller and spool using a butyl rubber inner tube and then control the slippage with this spool controller. The grip of the 5kg spool on the roller is so strong that this particular solution seemed like the only viable method.
<br/> <br/>
Spool controller height is adjusted by rotating the thumbwheel and it stays in position due to worm geared construction.
If spool controller is too low/ touching the spool it slips too much and doesn’t rewind properly.
If spool controller is too high/ far away jumping gets aggressive. The optimal gap has a fairly large tolerance though to rewinding function properly.
<br/><br/>

![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_spool_controller_cut.jpg)
![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_spool_controller_expl.jpg)

</details>




<details>
<summary>Drive unit</summary>

<br/>
The drive unit is in a way divided into two functional sections: motor/rewind and extruder section.
<br/><br/>

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
 
![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_roller_tray_expl_1.jpg)
![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_roller_tray_expl_2.jpg)

</details>




<details>
<summary>Hub-buffer</summary>
 
![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_hub_buffer_cut.jpg)
![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_hub_buffer_expl_1.jpg)
![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_hub_buffer_expl_2.jpg)
![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_hub_buffer_expl_3.jpg)
![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_hub_buffer_expl_4.jpg)

</details>




<details>
<summary>Control board box</summary>
 
![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_control_board_box_expl_1.jpg)
![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_control_board_box_expl_2.jpg)

</details>

[YouTube playlist](https://www.youtube.com/playlist?list=PLjJb97KCYTC9PMECO4NPdOToGcQD9c51B) of current BSFC tutorial videos.

<br/>

## Software configuration

Work in progress. <br/>
BSFC prototyping was done using [AFC-Klipper-Add-On](https://github.com/ArmoredTurtle/AFC-Klipper-Add-On) and using its [documentation](https://www.armoredturtle.xyz/docs/afc-klipper-add-on/index.html) to set things up. Compatibility with [Happy-Hare](https://github.com/moggieuk/Happy-Hare) has not yet been tested.

<details>
<summary>Some Afc-Klipper-Add-On config settings</summary>

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
