## What is this?

My attempt at reverse engineering the CaiXianlin shocker.


Please Note: these schematics are accurate for the following board revisions:
* remote: H-880V-TX-V1.0
* shocker: H-880B-RX-V2.0

## Shock output current and voltage

these numbers most likely aren't spot on, but its what my multimeter told me, and its the best i've got atm.

intensity | VAC | current(microamps)
--- | --- | ---
1% | 17.07 | 1.8
5% | 19.45 | 1.9
10% | 23.4 | 2.2
25% | 40.62 | 2.6
50% | 69.2 | 3.4
75% | 80.6 | 3.6
100% | 82.3 | 3.6


#### graphs

![alt text](./images/volts_vs_intensity.png "VAC vs intensity")


![alt text](./images/current_vs_intensity.png "current vs intensity")



## Shock pwm captures

The transformer is switched at a fixed frequency of 666 hz.

It uses a pwm signal with a duty cycle between 3.94% and 29.99%.

The following images are screenshots of sigrok captures at various percentages of intensity.

Note: You can view the captures for yourself using PulseView, they are in the "sigrok captures" folder of this repo.

1% Capture

![alt text](./images/1.png "1% intensity")

5% Capture

![alt text](./images/5.png "5% intensity")

10% Capture

![alt text](./images/10.png "10% intensity")

25% Capture

![alt text](./images/25.png "25% intensity")

50% Capture

![alt text](./images/50.png "50% intensity")

75% Capture

![alt text](./images/75.png "75% intensity")

100% Capture

![alt text](./images/100.png "100% intensity")

