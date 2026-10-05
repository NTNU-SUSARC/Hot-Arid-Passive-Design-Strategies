## Stack Ventilation with Air Flow Network

A passive ventilation system is a natural means of encouraging healthy airflow achieved without mechanical fans or electrical systems. It relies on natural wind and scientific principles such as temperature differentials and air pressure to move air through a space. 
The focus of this script is to test the role of The chimney effect as a ventilation concept that centers on the idea that warm, less dense air rises while heavier cool air remains lower to the ground. It’s also known as the stack effect, due to the idea that air of varying densities will sit on top of one another.
<img width="400" height="275" alt="solar_chimney_-_swl" src="https://github.com/user-attachments/assets/0c90410f-fa33-4e58-98b4-2399c592aa9a" />

[_Stack Ventilation_Image Source_](https://ad7eb.wordpress.com/2013/11/15/stack-venturi-and-bernoullis-effects-in-cooling-a-building/)



### Stack Ventilation Design Considerations
Openings located low and high, and on opposite sides of a space, create a ‘stack effect’ – warm indoor air rising out through high openings, drawing in cooler outdoor air through low openings.
Using the air’s buoyancy resulting from a difference in its temperature – climates with a minimum 1.7°C (3°F) difference between indoor and outdoor temperatures – the stack effect in a space, or within a ventilation shaft, will induce an air current that removes hot air from a space or building.

Guidelines for locating inlet and outlet openings:

Residential spaces – a minimum of 3 meters (10 feet) apart in height.

Commercial spaces – a minimum of 4.6 meters (15 feet) apart in height.

The greater the height between openings, the greater the air movement. Locate inlet openings below the height of an occupants’ upper body – 0.76 m to 1.37 m (2½ ft. to 4½ ft.) above finished floor.



### 1. Simulation Setup and Inputs

**1.1. Zone Geometry**


**1.2. Air Flow Network**

Compared to the default single-zone methods that Honeybee uses for infiltration and ventilation, the AFN represents air flow in a manner that is truer to the fluid dynamic behavior of real buildings. In particular, the AFN more accurately models the flow of air from one zone to another, accounting for the pressure changes induced by wind and air density differences. 

> [!CAUTION]
> Using the AFN means that the simulation will take considerably longer to run compared to the single zone option and the difference in simulation results is only likely to be significant when the Model contains operable windows or the building is extremely leaky.

[Read Ladybug Docs_AFN](https://docs.ladybug.tools/hb-energy-primer/components/3_loads/airflow_newtwork)


### 2. Simulation Outputs/Results




### Reference Readings
[https://www.mdpi.com/2076-3417/11/19/9185](https://www.mdpi.com/2076-3417/11/19/9185)

https://2030palette.org/stack-ventilation/




### Downloads (Released 04-10-2026)



