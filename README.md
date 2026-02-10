# Busy Snail Filament Changer (BSFC)

![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/BSFC_spool_unit_animcut.gif)

## From proto to closed beta
Prototyping has been done and everything is working nice. It's time to move to closed beta testing to ensure that STLs, BOM and wiring are all spot on before the public release.
<br/><br/>
Welcome to the Busy Snail Filament Changer private closed beta repository! <ins>***By downloading files from here, you agree to not share them anywhere.***</ins> Since minor changes are still possible, we don't want pre-release files floating around the internet.

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

[Rewind clutch](#rewind-clutch) -
[Spool controller](#spool-controller) -
[Drive unit](#drive-unit) -
[Roller tray](#roller-tray) -
[Hub-buffer](#hub-buffer) -
[Control board box](#control-board-box)

This section with illustrations currently serves also as a BSFC building manual.

<br/>
<br/>
<br/>

### Rewind clutch
[To section top](#technical-details) <br/>

Rewind clutch is closely related to the traditional freecoaster rear hub of a BMX bicycle. <br/>
When the stepper motor rotates in the filament feed/extrude direction, the clutch is disengaged and clutch gear freewheels and spool roller also rotates freely.
In the rewind/retract direction, the clutch is engaged and the spool is rewound. 
<br/> <br/>
Spring-loaded conical interface's friction must be greater than the sparse thread’s friction of the engager component.
It is not beneficial for the spring to be adjusted too tight, but too loose an adjustment will prevent the clutch from operating. <br/>
For the clutch to function properly, a small amount of silicone grease must be applied to its internal contact surfaces.

![bsfc_build_clutch_cut.jpg](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_clutch_cut.jpg)
![bsfc_build_clutch_cut.jpg](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_clutch_expl.jpg)



<br/>
<br/>
<br/>

### Spool controller
[To section top](#technical-details) <br/>

Since the extruder and rewind gear train have a fixed gear ratio, it has to be optimized for almost empty spools to achieve acceptable rewind tightness (angular vs. peripheral velocities).
Fuller spool has then higher peripheral velocity than emptier spool and some slipping must exist between the roller and the spool.
When spool tries to have higher peripheral velocity than rewinded filament from extruder allows it climbs to the spool controller and slips a bit (does this micro jumping constantly).
<br/> <br/>
Spool controller height is adjusted by rotating the thumbwheel and it stays in position due to worm geared construction.<br/>
If spool controller is too low/ touching the spool it slips too much and doesn’t rewind properly.<br/>
If spool controller is too high/ far away jumping gets aggressive.<br/>
The optimal gap has a fairly large tolerance though to rewinding function properly.

![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_spool_controller_cut.jpg)
![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_spool_controller_expl.jpg)



<br/>
<br/>
<br/>

### Drive unit
[To section top](#technical-details) <br/>

![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_drive_unit_expl_1.jpg)
![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_drive_unit_block_motor_expl_1.jpg)
![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_drive_unit_block_motor_expl_2.jpg)
![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_drive_unit_block_motor_expl_3.jpg)





<br/>
<br/>
<br/>

### Roller tray
[To section top](#technical-details) <br/>

![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_roller_tray_expl_1.jpg)
![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_roller_tray_expl_2.jpg)



<br/>
<br/>
<br/>

### Hub-buffer
[To section top](#technical-details) <br/>

![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_hub_buffer_cut.jpg)
![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_hub_buffer_expl_1.jpg)
![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_hub_buffer_expl_2.jpg)
![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_hub_buffer_expl_3.jpg)
![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_hub_buffer_expl_4.jpg)



<br/>
<br/>
<br/>

### Control board box
[To section top](#technical-details) <br/>

![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_control_board_box_expl_1.jpg)
![IMG](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_build_control_board_box_expl_2.jpg)
