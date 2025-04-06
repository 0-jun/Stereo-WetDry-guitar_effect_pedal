Stereo Wet/Dry pedal
=======================
The effect pedal has the following functions.
* Dry_In : Split dry signal to sum into each channel of the stereo wet signal
* Dry_Buffered_Bypass (DBD) : Output buffered dry signal for using input of another pedal
* Wet_Right_In (WR In), Wet_Left_In (WL In) : Stereo input for signals such as delay, reverb, chorus, etc
* WRD_Out, WLD_Out : Output stereo of wet+dry signal (or you can use it as a mono using only one channel)
* Four volume knob : Set the volume of two dry signals and two wet signals by knob

## PCB
I divided the pcb into three to put all parts in the pedal case.
1. power part
![PCB-power part](https://github.com/0-jun/Stereo-WetDry-guitar_effect_pedal/blob/main/image/PCB-power%20part.jpg)
![Artwork-power part](https://github.com/0-jun/Stereo-WetDry-guitar_effect_pedal/blob/main/image/Artwork-power%20PCB.png)
2. register for half vdd inputa
![PCB-half vdd for input part](https://github.com/0-jun/Stereo-WetDry-guitar_effect_pedal/blob/main/image/PCB-half%20vdd%20for%20input.jpg)
![Artwork-half vdd for input part](https://github.com/0-jun/Stereo-WetDry-guitar_effect_pedal/blob/main/image/Artwork-half%20vdd%20for%20input.png)
3. main part (opamp)
![PCB-main part](https://github.com/0-jun/Stereo-WetDry-guitar_effect_pedal/blob/main/image/PCB-main%20part%20.jpg)
![Artwork-main part](https://github.com/0-jun/Stereo-WetDry-guitar_effect_pedal/blob/main/image/Artwork-main%20part.png)

## Verify signal
1.Verify Dry_In (triangle wave) signal and Dry_Buffered_Bypass
 * blue signal : Dry_In (STM32 DAC out (triangle wave))
 * yellow signal : Dry_Buffered_Bypass
![Dry_In and Dry_Buffered_Bypass](https://github.com/0-jun/Stereo-WetDry-guitar_effect_pedal/blob/main/image/01_Dry_In_and_Dry_Buffered_Bypass.png)
2. Verify Dry_In signal (triangle wave) and WRD_Out signal (guitar signal) combined
 * blue signal : Dry_In (STM32 DAC out (triangle wave))
 * yellow signal : WRD_Out (blue signal + guitar signal)
![Combined signal](https://github.com/0-jun/Stereo-WetDry-guitar_effect_pedal/blob/main/image/02_Dry_In_and_WRD_Out.png)

## Conclusion
It was confirmed that the dry signal and the wet signal were combined when connected in the following configuration.\

### configuration
* config1
![config1](https://github.com/0-jun/Stereo-WetDry-guitar_effect_pedal/blob/main/image/config%201.png)
* config2
![config2](https://github.com/0-jun/Stereo-WetDry-guitar_effect_pedal/blob/main/image/config%202.png)
* config3
![config3](https://github.com/0-jun/Stereo-WetDry-guitar_effect_pedal/blob/main/image/config%203.png)

