# Ghost Rider simulation

![Banner image](/readme-assets/promogr4-small.jpg?raw=true "Banner")

## Preprequisits

1. Install VSCode
2. Install UE4 Engine
3. Run UE4 Engine at least once

## Setup

1. download the latest version of the Ghostrider package
2. unzip the archive into a folder.
3. Open vscode
4. In a folder of your choosing pull the edison_ai repository into this folder. *git clone https://**[YOUR USERNAME]**@bitbucket.org/freemens/edison_ai.git*
5. Checkout to the ev_simulation branch.
6. Pull the repository.  

## Run the simulation

1. In VSCode go in the debug menu (small bug icon on the left)
2. Click on ther play button with the EDISON AI GR Option
3. Wait until you see the following :

|    | Conditions    | Name          | Type   | Unit   |   Value |
|----|---------------|---------------|--------|--------|---------|
|  0 |               | Cell in S     |        |        |  14     |
|  1 |               | Cell in P     |        |        |  10     |
|  2 |               | Modules in P  |        |        |   1     |
|  3 |               | Modules in S  |        |        |  14     |
|  4 |               | Stacks in P   |        |        |   1     |
|  5 |               | Stacks in S   |        |        |   1     |
|  6 | 25°C, C/2     | Capacity      | Nom.   | A.h    |  32     |
|  7 | 25°C, 50% SOC | Voltage       | Nom.   | V      |  51.8   |
|  8 | 25°C, 50% SOC | DC Resistance | Nom.   | Ohm    |   0.056 |
|  9 | 1C,50% SOC    | Power Loss    | Typ.   | W      |   0     |
| 10 | 500us,50% SOC | Short-Circuit | Typ.   | A      | 925.004 |
| 11 | Lithium cells | Specific Heat | Typ.   | J/K/kg | 800     |
| 12 | Lithium cells | Mass          | Typ.   | kg     |   8.4   |

>This table is displayed at the start of the simulation. 

## Run GhostRider

1. Go to the folder you used to unzip the archive
2. Go to  /WindowsNoEditor
3. Execute VehicleConf.exe

## Keybinding

### Move

- W: Move forward
- D: Move right
- A: Move left
- S: Move Back

### Interact

- E: Enter / Exit vehicle
- Numpad "+": Start the vehicle (ignition)
- C: Activate charger (only when near a charging station)

### Interface

- Numpad "-": Open / Close graphs and indicators
- Numpad ".": Open / close battery settings panel  

### Panic

- R: Resets the game to the start

>Please note that datas on graphs are managed by edison AI and will not be reseted. Use the reset if your vehicle is stuck or if you want to quicly reset the game to the hangar.

## HELP

### GhostRider recomendations

#### Clearing error

- To clear error you have to make sure that what was causing the issue is gone (under temperature is caused by too low temperature for example)
Then press the ignition key "Numpad +"

- If you have a **PDU Failure Error** you might need to rock the BMS's switch

- **In case it's not working you can reset the edison_ai program by clicking on the STOP button and PLAY button again**

- In case you have an authentication error you need to "Activate the BMS" via ION Lens

#### SoC

- Avoid going in SoC under 5% unless you want to showcase undervoltage error.

#### Deviation

- Nominal deviation is between 0.05 and 0.15
- Extreme deviation is between .016 and 0.5

#### Temperature

- Avoid ambient temperature below -15 and above +40 (unless the request arise)




### #TBS-Live Slack channel

This Slack channel is your go to place when you don't have answer. Ask them there for Technical consultant to answer.

#### Scheduling a meeting on Hangout

This channel can be used to schedule a meeting with someone. Event if you have someone specific in mind refrain from private messaging. Use the channel.

# Edison

## Setup

- Open Chrome
- Go to http://35.188.179.16/edison/web/app_dev.php/core/home
- Make sure you are using the DEMO account and no other.

## EV Telemetry

### Intra-day usage

This chart represent an intr day telemetry of the battery with the following parameters plotted:

- Current
- Temperature (of the battery)
- SoC

### SOH Counter

Current SoH (State of Health) of the battery

### Eq Cycles

Number of equivalent cycle to date

### Errors

Number of errors on the battery

### Last 1H - XXX profile

Last 1h evolution of the XXX parameter.

## Aging overview

### SoH Trend

