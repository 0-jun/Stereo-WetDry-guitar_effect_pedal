Stereo Wet/Dry pedal
=======================
The effect pedal has the following functions.
* Dry_In : Split dry signal to sum into each channel of the stereo wet signal
* Dry_Buffered_Bypass : Output buffered dry signal for using input of another pedal
* Wet_Right_In, Wet_Left_In : Stereo input for signals such as delay, reverb, chorus, etc
* WRD_Out, WLD_Out : Output stereo of wet+dry signal (or you can use it as a mono using only one channel)
* Four volume knob : Set the volume of two dry signals and two wet signals by knob

## Verify signal
I connected a signal with a constant period and amplitude to the dry-in port to check that the signals were combined.

1.Verify dry-in signal and buffered dry-out signal
 * blue signal : Dry_In (STM32 DAC out (triangle wave))
 * yellow signal : Dry_Buffered_Bypass
![Dry_In and Dry_Buffered_Bypass](./image/01_Dry in signal, Buffered Dry out signal.png)
2. Verify combined dry signal and wet signal
 * blue signal : Dry_In (STM32 DAC out (triangle wave))
 * yellow signal : WDR out (blue signal + guitar signal)
![Combined signal](./image/02_Dry in signal, Sum Wet and Dry signal.png)

## Result
It was confirmed that the dry signal and the wet signal were combined when connected in the following configuration.\
You can check the sound in the link below.

## Additional
It can be used in the following configurations.
* wet/dry
 - Dry_In : input dry signal
 - Dry_Buffered_Bypass : connect to another pedal
 - Wet_Right_In : NC
 - Wet_Left_In : delay, reverb, chorus, etc
 - WRD_Out : only dry-out
 - WLD_Out : wet + dry signal
* wet/dry stereo
 - Dry_in : input dry signal
 - Dry_Buffered_Bypass : connect to another pedal
 - Wet_Right_In : delay (or right of stereo delay)
 - Wet_Left_In : chorus (or left of stereo delay)
 - WRD_Out : wet right + dry signal
 - WLD_Out : wet left + dry signal


