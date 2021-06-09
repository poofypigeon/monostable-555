# Monostable 555 Tactile Switch Decounce Circuit

> Designed as an alternative to the monostable 555 timer circuit used in Ben Eater's 8-bit breadboard computer. 

## The Problem
An issue I encountered with the single step debounce circuit used in Ben Eater's 8-bit computer kit
is that it had only a fixed period of time for which it maintained a high clock state, regardless of whether
the button remained depressed or not. This meant that if you held the button down for longer than this time period, 
the debounce characteristics of the switch would cease and the button could produce another clock pulse, even though
the switch was never released.

One can attempt to resolve this problem by using larger resistances and/or capacitances to lengthen the debounced
time frame; however, this introduces its own annoyances when trying to send multiple controlled clock pulses in quick 
succession because the user must wait for the debounce period of one pulse to finish before another pulse can be sent.
It is very difficult to find a good timing balance for this configuration, especially if one is to limit the selection
of component values to those included in the kit.

## The Solution
The circuit presented here provides more reliable debounce characteristics, and puts the user in control of the timing
by maintaining a high clock state as long as the tactile switch remains depressed, only attempting to discharge the 
voltage holding the **555 Timer** in its _unstable_ state when the switch is released. 

### Trigger Behaviour
By default, the **555 Timer** has a _threshold_ voltage of `> 2/3 VCC` and a _trigger_ voltage of `< 1/3 VCC`; however, 
in this circuit the trigger voltage has negligible timing signifigance. This is due to **SW1** shorting **C1** to **GND** 
when pressed such that there can be no voltage difference between **C1** and **GND**. Applying the equation `I = C d/dt V`, 
consideringthat `d/dt V` can be approximated as infinity, we determine that current must also be approximated as infinity. 
Thus when **SW1** is pressed, **C1** will discharge practically instantaneously, dropping the voltage on the _trigger_ pin 
below `1/3 VCC`, and latching the **555 Timer**'s output to its _unstable_ high state.

### Threshold Behaviour

The recommended component values in the schematic give the following RC time constant:
```
R   =   R1   || R2
    =   1 MΩ || 1 MΩ
    =   500 KΩ
    
C   =   C1
    =   100 nF

RC  =   500 KΩ * 100 nF
    =   50 ms
```

An RC charging table can now be used to determine approximately how long it will take for the voltage of **C1** to return to 
`> 2/3 VCC` when **SW1** is released so that the **555 Timer**'s output will return to its _stable_ low state.

| Time in RC Constants | % VCC |
|----------------------|-------|
| 1RC                  | 63.2% |
| 2RC                  | 87.5% |
| 3RC                  | 95.0% |
| 4RC                  | 98.2% |
| 5RC                  | 99.3% |

From this table we determine that it takes about 1RC (50 ms) of **SW1** remaining as an open circuit for the **555 Timer**'s output 
to return to a low state.
> Note that based on the behaviour described above in _trigger behaviour_, if **SW1** reinitiates the path from **C1** to **GND**, 
> even momemtarily, **C1** will dump all of it's charge and return to `0V`, resetting the charging 'timer'. It is this property that 
> gives this circuit its excellent debounce characteristics because 50 ms is a long period of time with respect to any intermittent 
> contact on **SW1** which may cause unwanted clock pulses; however, from a user's perspective, 50 ms is not a long enough interval 
> to interrupt consecutive button presses.
