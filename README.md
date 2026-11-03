# Hot-Arid-Passive-Design-Strategies
# Hot-Arid Passive Design Strategies

Hot-arid climates combine intense solar radiation, very hot days, low
humidity and a large swing between day and night temperatures. These
conditions make passive design especially effective: the building can
block the sun, store and release heat at the right time, and use dry air
for cooling.

This repository collects Grasshopper workflows (using Ladybug and
Honeybee) that let you test these strategies on your own building
geometry and weather file, and see how each one changes thermal
performance. Each strategy has its own page with an explanation of the
principle, a step-by-step walkthrough of the script, and example results.

## Strategies covered

| Strategy | What it explores |
|---|---|
| [Designing Shading Devices](Designing%20Shading%20Devices.md) | How shading geometry reduces solar gains |
| [Effect of Thermal Mass](Effect%20of%20Thermal%20Mass.md) | How storing heat buffers day-night temperature swings |
| [Evaporative Cooling Tower](Evaporative%20Cooling%20Tower.md) | Using the dry air to cool incoming air passively |
| [Stack Ventilation – AirFlowNetwork](Stack%20Ventilation-AirFlowNetwork.md) | Buoyancy-driven ventilation, modelled with the EnergyPlus AirFlowNetwork |

## Who this is for
Architecture students, researchers and practitioners who want to
test passive strategies in early design. Basic familiarity with Rhino
and Grasshopper is helpful; no prior Ladybug Tools experience is needed.

## Getting started
1. Download the repository (green **Code** button, then **Download ZIP**).
2. Open the script for the strategy you are interested in from from the "Downloads (released_'date')" at the end of each strategy page.
3. Load your own EPW weather file and adjust the inputs described on the strategy page.

## Requirements
Rhino / Grasshopper, Ladybug Tools (Ladybug, Honeybee). Tested versions: [add versions].

## Licence and citation
Released under the MIT licence. If you use this material in teaching or
research, please cite: [add citation / DOI].

Part of the NTNU SUSARC collection of climate-specific passive design resources.
