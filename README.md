# Busy Snail Filament Changer (BSFC)

<br/>

## From proto to closed beta
Prototyping has been done and everything is working nice. It's time to move to closed beta testing to ensure that STLs, BOM and wiring are all spot on before the public release.
<br/><br/>
Welcome to the Busy Snail Filament Changer private closed beta repository! By downloading files from here, you agree to not share them anywhere. Since minor changes are still possible, we don't want pre-release files floating around the internet.

<br/>

## One more filament changer design?
A filament changer supporting 5kg spools that uses large extruder gears to reliably pull filament from heavy spools didn't exist when starting the project (or at least couldn't find an open source one).

Features that were targeted in the design process:

- Support for larger than 1kg spools up to 5kg
- Extruder and spool rewind function operated per spool unit by the same stepper motor
- NEMA17 stepper motors for power and speed
- Large extruder gears to maximize traction
- As modular system as possible
- Possibility to use only 1 spool unit as a loader/unloader rather than a changer

<br/>








## Technical details
This technical details section with illustrations also currently serves as a BSFC building manual.

### Rewind clutch
Rewind clutch is closely related to the traditional freecoaster rear hub of a BMX bicycle. <br/>
When the stepper motor rotates in the filament feed/extrude direction, the clutch is disengaged and clutch gear freewheels and spool roller also rotates freely.
In the rewind/retract direction, the clutch is engaged and the spool is rewound. <br/> <br/>
Spring-loaded conical interface's friction must be greater than the sparse thread’s friction of the engager component.
It is not beneficial for the spring to be adjusted too tight, but too loose an adjustment will prevent the clutch from operating. <br/>
For the clutch to function properly, a small amount of silicone grease must be applied to its internal contact surfaces.

![bsfc_build_clutch_cut.jpg](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_clutch_cut.jpg)
![bsfc_build_clutch_cut.jpg](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_clutch_expl.jpg)

<br/>

### Spool controller

![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_spool_controller_cut.jpg)
![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_spool_controller_expl.jpg)


<br/>

### Hub/buffer

![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_hub_buffer_cut.jpg)
![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_hub_buffer_expl_1.jpg)
![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_hub_buffer_expl_2.jpg)
![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_hub_buffer_expl_3.jpg)
![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_hub_buffer_expl_4.jpg)



<br/>

### Control board box

![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_controller_box_expl_f.jpg)
![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_controller_box_expl_b.jpg)
