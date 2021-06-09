EESchema Schematic File Version 4
EELAYER 30 0
EELAYER END
$Descr A4 11693 8268
encoding utf-8
Sheet 1 1
Title "Monostable 555 Switch Debouncer"
Date "2021-05-29"
Rev "1"
Comp ""
Comment1 ""
Comment2 ""
Comment3 ""
Comment4 ""
$EndDescr
$Comp
L chip_graphic:555_Timer U?
U 1 1 60B3E46D
P 2300 2175
F 0 "U?" H 2290 2255 50  0001 C CNN
F 1 "555_Timer" V 1750 2825 50  0001 R CNN
F 2 "" H 2300 2175 50  0001 C CNN
F 3 "" H 2300 2175 50  0001 C CNN
	1    2300 2175
	0    -1   -1   0   
$EndComp
$Comp
L power:VCC #PWR?
U 1 1 60B4C9D2
P 2425 1500
F 0 "#PWR?" H 2425 1350 50  0001 C CNN
F 1 "VCC" H 2440 1673 50  0000 C CNN
F 2 "" H 2425 1500 50  0001 C CNN
F 3 "" H 2425 1500 50  0001 C CNN
	1    2425 1500
	1    0    0    -1  
$EndComp
Wire Wire Line
	2425 2950 2425 3675
Wire Wire Line
	2725 2400 2725 2250
Wire Wire Line
	2575 2950 2575 3100
Wire Wire Line
	2575 3100 3125 3100
Wire Wire Line
	3125 2250 3125 3100
$Comp
L pspice:CAP C1
U 1 1 60B4DF5E
P 3125 3425
F 0 "C1" H 2947 3379 50  0000 R CNN
F 1 "80nF" H 2947 3470 50  0000 R CNN
F 2 "" H 3125 3425 50  0001 C CNN
F 3 "~" H 3125 3425 50  0001 C CNN
	1    3125 3425
	-1   0    0    1   
$EndComp
Connection ~ 3125 3100
Connection ~ 2425 3675
Wire Wire Line
	2425 3675 2425 3700
$Comp
L power:GND #PWR?
U 1 1 60B4CD04
P 2425 3700
F 0 "#PWR?" H 2425 3450 50  0001 C CNN
F 1 "GND" H 2430 3527 50  0000 C CNN
F 2 "" H 2425 3700 50  0001 C CNN
F 3 "" H 2425 3700 50  0001 C CNN
	1    2425 3700
	1    0    0    -1  
$EndComp
$Comp
L pspice:R R1
U 1 1 60B5037A
P 2725 1925
F 0 "R1" H 2775 1975 50  0000 L CNN
F 1 "1M" H 2775 1900 50  0000 L CNN
F 2 "" H 2725 1925 50  0001 C CNN
F 3 "~" H 2725 1925 50  0001 C CNN
	1    2725 1925
	1    0    0    -1  
$EndComp
Connection ~ 2725 2250
$Comp
L pspice:R R2
U 1 1 60B5128C
P 2950 1925
F 0 "R2" H 3000 1975 50  0000 L CNN
F 1 "1M" H 3000 1900 50  0000 L CNN
F 2 "" H 2950 1925 50  0001 C CNN
F 3 "~" H 2950 1925 50  0001 C CNN
	1    2950 1925
	1    0    0    -1  
$EndComp
Wire Wire Line
	2725 2950 2725 3025
Wire Wire Line
	2875 2400 2875 2325
Wire Wire Line
	2875 2325 3525 2325
$Comp
L pspice:CAP C2
U 1 1 60B56DA6
P 3525 2675
F 0 "C2" H 3347 2629 50  0000 R CNN
F 1 "10nF" H 3347 2720 50  0000 R CNN
F 2 "" H 3525 2675 50  0001 C CNN
F 3 "~" H 3525 2675 50  0001 C CNN
	1    3525 2675
	-1   0    0    1   
$EndComp
Wire Wire Line
	2725 3025 3700 3025
Wire Wire Line
	2425 1500 2425 1575
Wire Wire Line
	2725 2175 2725 2250
Wire Wire Line
	2725 2250 2950 2250
Wire Wire Line
	2950 2175 2950 2250
Connection ~ 2950 2250
Wire Wire Line
	2950 2250 3125 2250
Wire Wire Line
	2725 1675 2725 1575
Wire Wire Line
	2725 1575 2950 1575
Wire Wire Line
	2950 1575 2950 1675
Wire Wire Line
	2725 1575 2425 1575
Connection ~ 2725 1575
Connection ~ 2425 1575
Wire Wire Line
	2425 1575 2425 2400
Wire Wire Line
	2875 2950 2875 3175
Wire Wire Line
	2875 3175 2175 3175
Wire Wire Line
	2175 3175 2175 1575
Wire Wire Line
	2175 1575 2425 1575
Wire Wire Line
	2575 2400 2575 2250
NoConn ~ 2575 2250
Wire Wire Line
	3525 2325 3525 2425
Wire Wire Line
	3525 2925 3525 3675
$Comp
L Custom_Symbols_Library:SW_PUSH_BUTTON SW1
U 1 1 60B64A26
P 1900 3100
F 0 "SW1" H 1975 3275 50  0000 R CNN
F 1 "SW_PUSH_BUTTON" H 1900 3264 50  0001 C CNN
F 2 "" H 1900 3100 50  0000 C CNN
F 3 "" H 1900 3100 50  0000 C CNN
	1    1900 3100
	1    0    0    -1  
$EndComp
Wire Wire Line
	3125 3100 3125 3175
Wire Wire Line
	2425 3675 3125 3675
Connection ~ 3125 3675
Wire Wire Line
	3125 3675 3525 3675
Wire Wire Line
	1700 3100 1625 3100
Wire Wire Line
	2100 3100 2575 3100
Connection ~ 2575 3100
Wire Wire Line
	1625 3100 1625 3675
Wire Wire Line
	1625 3675 2425 3675
Text GLabel 3700 3025 2    50   Input ~ 0
Clock_Logic
$Comp
L power:VCC #PWR?
U 1 1 60B70F2F
P 1675 1800
F 0 "#PWR?" H 1675 1650 50  0001 C CNN
F 1 "VCC" H 1690 1973 50  0000 C CNN
F 2 "" H 1675 1800 50  0001 C CNN
F 3 "" H 1675 1800 50  0001 C CNN
	1    1675 1800
	1    0    0    -1  
$EndComp
$Comp
L power:GND #PWR?
U 1 1 60B717CD
P 1675 2450
F 0 "#PWR?" H 1675 2200 50  0001 C CNN
F 1 "GND" H 1675 2275 50  0000 C CNN
F 2 "" H 1675 2450 50  0001 C CNN
F 3 "" H 1675 2450 50  0001 C CNN
	1    1675 2450
	1    0    0    -1  
$EndComp
$Comp
L pspice:CAP C3
U 1 1 60B71FF1
P 1675 2125
F 0 "C3" H 1497 2079 50  0000 R CNN
F 1 "10nF" H 1497 2170 50  0000 R CNN
F 2 "" H 1675 2125 50  0001 C CNN
F 3 "~" H 1675 2125 50  0001 C CNN
	1    1675 2125
	-1   0    0    1   
$EndComp
Wire Wire Line
	1675 2375 1675 2450
Wire Wire Line
	1675 1875 1675 1800
Wire Notes Line
	2625 2200 3150 2200
Wire Notes Line
	3150 1525 2625 1525
Wire Notes Line
	2625 1525 2625 2200
Wire Notes Line
	3150 2200 3150 1525
Text Notes 2625 1500 0    50   ~ 0
R1 || R2 = 500k
Text Notes 1000 6100 0    50   ~ 0
Concept of Operation:\n\nWhen SW1 is open, C1 will charge through R1 and R2 which act in parallel to provide an equivalent resistance of 500kΩ. \nThe resistance of R1||R2, paired with the 80nF capacitance of C1, charges C1 to 66% of Vcc in about 40ms, at which point the threshold comparater \nwill trigger and the 555 output will be held in a low state (The values I chose for this RC circuit are based on the compnent values which come with the\n8-Bit Breadboard Computer kit, as well as what timing felt best in my own testing while maintaining good debounce properties. They are ultimately arbitrary, \nand I’d encourage you to experiment with values on your own).\n\nWhen SW1 is depressed, a direct path is created between C1 and GND causing C1 to discharge practically instantaneously, \ndropping the voltage on the TRIG pin below 33% of Vcc and latching the 555 output to a high state while SW1 remains held. \nIf the button contact is intermittent, the 555 output will not return to low unless the threshold voltage is allowed to return to 66% of Vcc \nwhich should only happen when SW1 is intentionally released and 40ms are allowed to pass with SW1 open.\n\nThe DISCH pin is not utilized in this circuit and should not be connected to anything.\n\nThe CONT pin’s purpose is to adjust the voltages at which the THRES and TRIG pins latch the 555’s internal SR latch. \nBecuase we do not want to use this feature, we place C2 between CONT and GROUND to resist voltage variations on this pin from outside interferences.\n\nThe RESET pin is tied to Vcc in order to avoid being accidentally triggered.\n\nC3 provides power smoothing to the Vcc and GND rails which results in much cleaner state transitions on the 555 output.
$EndSCHEMATC
