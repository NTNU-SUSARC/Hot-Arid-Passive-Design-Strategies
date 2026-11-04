## Stack Ventilation with Air Flow Network

A passive ventilation system is a natural means of encouraging healthy airflow achieved without mechanical fans or electrical systems. It relies on natural wind and scientific principles such as temperature differentials and air pressure to move air through a space. 
The focus of this script is to test the role of The chimney effect as a ventilation concept that centers on the idea that warm, less dense air rises while heavier cool air remains lower to the ground. It’s also known as the stack effect, due to the idea that air of varying densities will sit on top of one another.
<img width="400" height="275" alt="solar_chimney_-_swl" src="https://github.com/user-attachments/assets/0c90410f-fa33-4e58-98b4-2399c592aa9a" />

[_Stack Ventilation_Image Source_](https://ad7eb.wordpress.com/2013/11/15/stack-venturi-and-bernoullis-effects-in-cooling-a-building/)



### Stack Ventilation Design Considerations
Openings located low and high, and on opposite sides of a space, create a ‘stack effect’ – warm indoor air rising out through high openings, drawing in cooler outdoor air through low openings.
Using the air’s buoyancy resulting from a difference in its temperature – climates with a minimum 1.7°C (3°F) difference between indoor and outdoor temperatures – the stack effect in a space, or within a ventilation shaft, will induce an air current that removes hot air from a space or building.

**Guidelines for locating inlet and outlet openings:**

Residential spaces – a minimum of 3 meters (10 feet) apart in height.

Commercial spaces – a minimum of 4.6 meters (15 feet) apart in height.

The greater the height between openings, the greater the air movement. Locate inlet openings below the height of an occupants’ upper body – 0.76 m to 1.37 m (2½ ft. to 4½ ft.) above finished floor.



### 1. Simulation Setup and Inputs

**1.1. INPUT_Zone Geometry**

**TEST CASE 1_No Chimney**
The simulated energy zone is an 8m X 8m X 3m room. To showcase the effects of stack ventilation, there is a primary inlet aperture, with a window shade object, constructed in the middle of its face towards the prevailing wind direction. Along with it, a smaller outlet aperature is constructed at a higher sill level on the ooposite face to enable cross ventilation.

<img width="500" height="500" alt="Screenshot (856)" src="https://github.com/user-attachments/assets/5e8c3c15-9135-4d8a-97ea-9ed16ca2a07b" />



<img width="2144" height="1497" alt="INPUR-GEO" src="https://github.com/user-attachments/assets/5e080d94-93de-4160-847f-a7a383b20386" />


For a naturally ventilated building, as in this test case, we do not need the mechanical ventilation systems. It can be turned off like this:

<img width="1228" height="979" alt="NO MECH VENT" src="https://github.com/user-attachments/assets/e41613ca-048f-43e2-8418-b2c606f8ee83" />


**1.1. INPUT_Chimney Geometry**


**TEST CASE 2_With Chimney**

An outlet chimney with apertures is provided on top of the energy zone, on the opposite side as that of the inlet aperture.
The greater the height difference and temperature difference, the stronger the effect. 
<img width="3158" height="1151" alt="INPUR-chi" src="https://github.com/user-attachments/assets/26d9810d-bfcc-47e4-a93f-d6a7f5b0ba5a" />

Due to high diurnal differences in temperatures, the chimney apertures are given a constant schedule where they are only operable between the cooler hours, as found in the particular weather file, from 1AM to 4AM. This enables night coolth.
<img width="1822" height="1983" alt="SCHEDULE CHIM" src="https://github.com/user-attachments/assets/5437354a-df3e-4a42-a967-2e1a2cb546ec" />


**1.1. INPUT_Weather file and Analysis Period**

Stack ventilation (the stack or chimney effect) requires a minimum temperature difference (Δ T) of 1.7°C (3°F) between the interior and exterior air to generate sufficient buoyancy and drive natural airflow. Source: [Architecture2030 palette](https://2030palette.org/stack-ventilation/).
Therefore, to get the best out of the chimney, it should be operable on days when outdoor air is cooler than indoor air, bringing cooler outdoor air indoors to reduce the cooling load.

<img width="1727" height="1272" alt="INPUR-WEA" src="https://github.com/user-attachments/assets/7cdf9f74-eea7-4b95-99dd-55cc5d991bb2" />


<img width="724" height="790" alt="Screenshot (851)" src="https://github.com/user-attachments/assets/26bf298d-ddb2-4a4c-aa50-7370f06aa4c3" />


**1.2. Air Flow Network**

Compared to the default single-zone methods that Honeybee uses for infiltration and ventilation, the AFN represents air flow in a manner that is truer to the fluid dynamic behavior of real buildings. In particular, the AFN more accurately models the flow of air from one zone to another, accounting for the pressure changes induced by wind and air density differences. 

<img width="2068" height="2137" alt="CASES" src="https://github.com/user-attachments/assets/d0f40d0a-37ee-45e7-96f1-f4f80bc32adc" />

<img width="2401" height="1176" alt="AFN RESULTS" src="https://github.com/user-attachments/assets/bbddcdb2-5f80-458e-a448-19b40d3a579b" />


> [!CAUTION]
> Using the AFN means that the simulation will take considerably longer to run compared to the single zone option and the difference in simulation results is only likely to be significant when the Model contains operable windows or the building is extremely leaky.

[Read Ladybug Docs_AFN](https://docs.ladybug.tools/hb-energy-primer/components/3_loads/airflow_newtwork)


### 2. Simulation Outputs/Results

<img width="993" height="813" alt="Screenshot (848)" src="https://github.com/user-attachments/assets/59b7a2d4-5fe2-428c-92f1-03890165f876" />

<img width="3967" height="754" alt="COMFORT RESULT" src="https://github.com/user-attachments/assets/354dcf86-d0b2-4c57-bec8-7f6609f1c2f3" />


<img width="1000" height="810" alt="Screenshot (850)" src="https://github.com/user-attachments/assets/099056f9-1481-4653-a563-7a5437f40ecd" />


<img width="828" height="812" alt="Screenshot (856)" src="https://github.com/user-attachments/assets/6928abb1-3a0c-4212-a905-ea69e6709390" />


<img width="2401" height="1176" alt="AFN RESULTS" src="https://github.com/user-attachments/assets/295c5f66-0107-468c-b67c-8d118dd0899e" />

<img width="769" height="827" alt="Screenshot (855)" src="https://github.com/user-attachments/assets/e92a5a97-1868-47ba-ae7b-0682c67cba7d" />

<img width="755" height="835" alt="Screenshot (854)" src="https://github.com/user-attachments/assets/eae79ef6-a946-428f-b02c-6f0f37d275ce" />


### Reference Readings
[https://www.mdpi.com/2076-3417/11/19/9185](https://www.mdpi.com/2076-3417/11/19/9185)

https://2030palette.org/stack-ventilation/


### Downloads (Released 03-11-2026)

***The files are created in Rhino 7 and use the Ladybug 1.10 version.***

[Download the Grasshopper File here](https://github.com/NTNU-SUSARC/Hot-Arid-Passive-Design-Strategies/blob/78088de6bf3d66187db30f12045e9a7a6ee9ed39/Files-Scripts/03_11_2026_Stack%20Ventilation_AFN.gh)



