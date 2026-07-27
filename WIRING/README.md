# Busy Snail Filament Changer (BSFC) Wiring

These wiring instructions currently support two control boards: Bigtreetech MMB CAN V1.1 and V2. The internal wiring of the drive units and hub/buffer is universal. The LED, stepper motor, and hub/buffer intermediate wiring is the same for both boards. The wiring between the filament switches of the drive unit and the control board is board-specific.

For the internal wiring of the drive unit and hub/buffer, it is recommended to use UL1332 AWG26 FEP wire (outer diameter 1.1mm) because 3D printed components have some tight spots in the wire channels. The insulation thickness and outer diameter of PVC insulated wire is usually larger, which may cause challenges.

For wiring between the control board and the drive unit and hub/buffer, the thickness of the wire is not critical. For stepper motor wiring, a typical ribbon wire is a good choice to keep the bundles neater.

<br/>

## Wiring Diagrams

![bsfc_wiring_diagrams](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_wiring_diagrams.jpg)

<br/>

## Control Board Connections

<details>
<summary>Control Board Connections and Corresponding Pin Mappings for AFC-Klipper-Add-On</summary>

## Bigtreetech mmb can v1.1
![BSFC_wiring_board_btt_mmb_can_v1.1](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/BSFC_wiring_board_btt_mmb_can_v1.1.jpg)

Pin mappings for Bigtreetech mmb can v1.1 control board:

/config/AFC/mcu/MMB_1.1.cfg

```
[board_pins Your_Unit_Name]
mcu: Your_Mcu_Name
aliases:
    M1_STEP=PB15   , M1_DIR=PB14   , M1_EN=PB8    , M1_UART=PA10   ,
    M2_STEP=PD2    , M2_DIR=PB13   , M2_EN=PD1    , M2_UART=PC7    ,
    M3_STEP=PD0    , M3_DIR=PD3    , M3_EN=PA15   , M3_UART=PC6    ,
    M4_STEP=PB6    , M4_DIR=PB7    , M4_EN=PB5    , M4_UART=PA9    ,

	HUB=PB11 		, 
	TRG1=PA3  		, TRG2=PA4  	, TRG3=PB9 		, TRG4=PA8		,
	EXT1=PC15 		, EXT2=PC13		, EXT3=PC14		, EXT4=PB12		,
    TN_ADV=PB10     , TN_TRL=PB2 ,
	RGB1=PA2		, 
```

<br/>
<br/>


## Bigtreetech mmb can v2.0
![BSFC_wiring_board_btt_mmb_can_v2.0](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/BSFC_wiring_board_btt_mmb_can_v2.0.jpg)

Pin mappings for Bigtreetech mmb can v2.0 control board:

/config/AFC/mcu/MMB_2.0.cfg

```
[board_pins Your_Unit_Name]
mcu: Your_Mcu_Name
aliases:
    M1_STEP=PD4    , M1_DIR=PD3    , M1_EN=PD5    , M1_UART=PB5    ,
    M2_STEP=PC9    , M2_DIR=PC8    , M2_EN=PD2    , M2_UART=PB4    ,
    M3_STEP=PC15   , M3_DIR=PC11   , M3_EN=PC10   , M3_UART=PB3    ,
    M4_STEP=PC13   , M4_DIR=PC12   , M4_EN=PC14   , M4_UART=PD6    ,

	HUB=PA15 		, 
	TRG1=PC5  		, TRG2=PB1  	, TRG3=PB10		, TRG4=PB12 	,
	EXT1=PC4  		, EXT2=PB0 		, EXT3=PB2 		, EXT4=PB11		,
    TN_ADV=PA10     , TN_TRL=PD9 ,
	RGB1=PC3		, 
```


</details>

<br/>

## Sample Pictures of Prototype Wire Assemblies

Some example pictures from the prototype phase showing soldered and crimped wire assemblies. The pictures are presented in the same order as they appear in the wiring diagram above.

<details>
<summary>Prototype Wire Assemblies</summary>
	
<br/>

Drive unit internal: filament presence switches
![bsfc_wiring_sample_du_switch](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_wiring_sample_du_switch.jpg)

Drive unit internal: LED
![bsfc_wiring_sample_du_led](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_wiring_sample_du_led.jpg)

Drive unit internal: stepper motor <br/>
(JST PH2.0-4 connector populated after wires are routed through 3d printed part's channel)
![bsfc_wiring_sample_du_motor](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_wiring_sample_du_motor.jpg)

Hub/buffer internal: micro switches
![bsfc_wiring_sample_hb_switch](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_wiring_sample_hb_switch.jpg)

Control board RGB to 1st drive unit RGBIN
![bsfc_wiring_sample_cb_led](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_wiring_sample_cb_led.jpg)

LED daisy chain between drive units 1->2, 2->3, 3->4 (RGBOU -> RGBIN)
![bsfc_wiring_sample_ga_led_daisy_chain](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_wiring_sample_ga_led_daisy_chain.jpg)

Control board stepper driver to drive unit stepper MOTOR in (Sample: 1st unit 300mm)
![bsfc_wiring_sample_cb_motor](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_wiring_sample_cb_motor.jpg)

Control board STOPx to Hub/Buffer
![bsfc_wiring_sample_cb_hub_buffer](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_wiring_sample_cb_hub_buffer.jpg)

Control board STOPx to drive unit SWTCH (Sample: Btt Mmb Can V2)
![bsfc_wiring_sample_cb_switch](https://github.com/BusySnailDesignLab/Busy-Snail-Filament-Changer/blob/main/IMG/bsfc_wiring_sample_cb_switch.jpg)

</details>

