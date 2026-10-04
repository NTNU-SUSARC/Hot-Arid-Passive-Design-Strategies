# Evaporative Cooling Tower

A cooltower (which is sometimes referred to as a wind tower or a shower cooling tower) is a component that is intended to model a passive downdraught evaporative cooling (PDEC) that is designed to capture the wind at the top of a tower and cool the outside air using water evaporation before delivering it to a space. The air flow in these systems is natural as the evaporation process increases the density of the air causing it to fall through the tower and into the space without the aid of a fan. A cooltower typically consists of a water spray or an evaporative pad, a shaft, and a water tank or reservoir. Wind catchers to improve the wind-driven performance at the top of the tower are optional. Water is pumped over an evaporative device by water pump which is the only component consumed power for this system. This water cools and humidifies incoming air and then the cool, dense air naturally falls down through shaft and leaves through large openings at the bottom of cooltowers.


<img width="700" height="500" alt="image" src="https://github.com/user-attachments/assets/c325e4bb-1cf0-4038-a8da-b987b1ad13f8" />

_Concept: Passive down-draught evaporative cooling (PDEC)_ [_Image Source_](https://www.semanticscholar.org/paper/Simulation-of-passive-down-draught-evaporative-in-Kang-Strand/ac834a3993fb2bb16018c06f4f38f784f04557e2)



The shower cooling tower can be controlled by a schedule and the specification of maximum water flow rate and volume flow rate as well as minimum indoor temperature. The actual flow rate of water and air can be controlled as users specify the fractions of water loss and flow schedule. The required input fields include effective tower height and exit area to obtain the temperature and flow rate of the air exiting the tower. A schedule and rated power for the water pump are also required to determine the power consumed. The component typically has a stand alone water system that is not added to the water consumption from mains. However, users are required to specify the water source through an optional field, the name of water supply storage tank, in case any water comes from a water main. The model is described more fully in the Engineering Reference document.

This model requires weather information obtained from either design day or weather file specifications. The control is accomplished by either specifying the water flow rate or obtaining the velocity at the outlet with inputs and weather conditions when the water flow rate is unknown. As with infiltration, ventilation, and earth tubes, the component is treated in a similar fashion to “natural ventilation” in EnergyPlus.

[Refer to the _Energy Plus Object_ for 'ZoneCoolTower'](https://bigladdersoftware.com/epx/docs/8-0/input-output-reference/page-018.html#zonecooltowershower)



> [!NOTE]
> The script focuses primarily on showing the effects of Evaporative cooling in a hot & Arid climate. Hence, other parameters, like materiality, etc., are not explored fully in this example.

## 1. Simulation Inputs and Setup
To Run the simulation, some inputs are required to be set by the users, as shown below:

### 1.1 Extracting and analysing the weather data

The case example is simulated for the city of Aswan, Egypt. By extracting the Dry Bulb Temperature chart, as shown below, we see that the summer months can be overheated and dry, and can potentially benefit from the passive cooling strategy of Evaporative Cooling.

<img width="3220" height="1144" alt="DBT_Aswan" src="https://github.com/user-attachments/assets/98b5c0ee-f76b-4a31-9c57-8cb0eee09f17" />


### 1.2 Setting up the Energy Zone

<img width="1962" height="1386" alt="Geometry" src="https://github.com/user-attachments/assets/9743bcdf-e6d4-4149-bdd0-78496397cb7d" />


### 1.3 Additional string for the tower

Since there are no Grasshopper components in Honeybee to model these things, you will have to add them to the HB EnergyPlus model using the additionalStrings_ input on the Openstudio or EnergyPlus components.

<img width="8639" height="2205" alt="Script_tower" src="https://github.com/user-attachments/assets/dc060923-6d28-42e6-8b2d-105962d71799" />


### 1.4 Setting up the Seasonal Schedule for the Tower

It is important to find the overheated period for your weather, to make the most of the evaporative cooling effects, and avoid having an opposite effect on the total energy loads.

<img width="3938" height="1662" alt="Script_Scheduling" src="https://github.com/user-attachments/assets/835536ac-7b28-4301-b969-21486e08fc4c" />

### 1.5 Setting up the Simulation Setup for custom outputs

By referring to the the Energy Plus Object, specific outputs from the simulation can be demanded.

<img width="3208" height="1333" alt="simulation setup_ECT" src="https://github.com/user-attachments/assets/82953a69-d674-43ea-9e86-e0ac54aacf38" />



## 2. Simulation Outputs/Results

### 2.1 Reading the Custom Results

<img width="3079" height="881" alt="Zone Sensible Loss_ECT" src="https://github.com/user-attachments/assets/75928d87-fe7c-4ba5-97ce-354a8cc438e5" />

<img width="3503" height="969" alt="custom_results_ECT" src="https://github.com/user-attachments/assets/20ebd315-4db9-4ed8-99b4-87efc3525e0c" />



### 2.2 Energy Balance Chart comparison

To understand the effect of Evaporative cooling, two scenarios are simulated, i.e., with and without the Cooling tower.


**Scenario 1: _Without_ the Evaporative Cooling tower:**

<img width="2801" height="1002" alt="Without Evaporation_ECT png" src="https://github.com/user-attachments/assets/36eed6cf-ee46-4acc-b497-55c97b02a9b4" />




**Scenario 2: _With_ the Evaporative Cooling tower:**

The Storage component here shows the heat loss due to the cooling effect of evaporative tower. It reduced the Cooling load by almost 50 %, Although the heating load is increased by 20% in this sceanrio. 
Since this weather has a significant underheated period as well, some passive heating design techniques can also be employed to lower the heating load.

<img width="2775" height="993" alt="With Evaporation_ECT" src="https://github.com/user-attachments/assets/2a8a3f35-5667-4891-a537-0460550540d8" />



## Downloads (released_03-10-2026)

***The files are created in Rhino 7 and use the Ladybug 1.10 version.***

[Download the Rhino File here](https://github.com/ntnu-susarc-cbf/GH-Scripts-2026/blob/b4835dd071a91f7e8b08557ce84773b7ba5ad4c6/Working%20Files/03_10_2026_Evaporative%20Cooling%20tower.3dm)

[Download the Grasshopper file here](https://github.com/ntnu-susarc-cbf/GH-Scripts-2026/blob/b4835dd071a91f7e8b08557ce84773b7ba5ad4c6/Working%20Files/03_10_2026_Evaporative%20Cooling%20tower.gh)
