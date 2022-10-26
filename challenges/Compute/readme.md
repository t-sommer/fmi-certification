# Synopsys Silver - Compute.fmu
## Setting tunable parameters example

- x_0, x_1, x_2 -> float inputs
- y_0, y_1, y_2 -> float outputs
- shift -> float tunable parameter

### Outputs update rule:
- y_0 = x_0 * x_1 + shift; updated each 10ms (time = 0 included)
- y_1 = x_0 + x_1; updated each 20ms (time = 0 included )
- y_2 = x_0 + x_1 + x_2; updated each 40ms (time = 0 included)

### Simulation example

#### Set initial values for inputs:
- x_0 = 5
- x_1 = 12
- x_2 = 25
#### Simulate the FMU.
#### The outputs should be:
- y_0 = 60
- y_1 = 17
- y_2 = 42
 
<img src="before_setting_tunable_parameter.png.png" alt="Results before setting shift tunable parameter" width="100%"/>

#### Set shift = 50
#### Simulate again the FMU.
#### The outputs should be now:
- y_0 = 110
- y_1 = 17
- y_2 = 42

<img src="after_setting_tunable_parameter.png.png" alt="Results after setting shift tunable parameter" width="100%"/> 
