# Evaporative Cooling Tower
A cooltower (which is sometimes referred to as a wind tower or a shower cooling tower) is a component that is intended to model a passive downdraught evaporative cooling (PDEC) that is designed to capture the wind at the top of a tower and cool the outside air using water evaporation before delivering it to a space. The air flow in these systems is natural as the evaporation process increases the density of the air causing it to fall through the tower and into the space without the aid of a fan. A cooltower typically consists of a water spray or an evaporative pad, a shaft, and a water tank or reservoir. Wind catchers to improve the wind-driven performance at the top of the tower are optional. Water is pumped over an evaporative device by water pump which is the only component consumed power for this system. This water cools and humidifies incoming air and then the cool, dense air naturally falls down through shaft and leaves through large openings at the bottom of cooltowers.

The shower cooling tower can be controlled by a schedule and the specification of maximum water flow rate and volume flow rate as well as minimum indoor temperature. The actual flow rate of water and air can be controlled as users specify the fractions of water loss and flow schedule. The required input fields include effective tower height and exit area to obtain the temperature and flow rate of the air exiting the tower. A schedule and rated power for the water pump are also required to determine the power consumed. The component typically has a stand alone water system that is not added to the water consumption from mains. However, users are required to specify the water source through an optional field, the name of water supply storage tank, in case any water comes from a water main. The model is described more fully in the Engineering Reference document.

This model requires weather information obtained from either design day or weather file specifications. The control is accomplished by either specifying the water flow rate or obtaining the velocity at the outlet with inputs and weather conditions when the water flow rate is unknown. As with infiltration, ventilation, and earth tubes, the component is treated in a similar fashion to “natural ventilation” in EnergyPlus.

> [!NOTE]
> The script focuses primarily on showing the effects of Evaporative cooling in a hot & Arid climate. Hence, other parameter, like materiality, etc., are not explored fully in this example.

## 1. Simulation Inputs and Setup
To Run the simulation, some inputs are required to be set by the users, as shown below:

### 1.1 Extracting and analysing the weather data

The case example is simulated for the city of Aswan, Egypt. By extracting the Dry Bulb Temperature chart, as shown below, we see that the summer months can be overheated and dry, and can potentially benefit from the passive cooling strategy of Evaporative Cooling.
![Hourly Dry Bulb Temperature_Aswan_Egypt](https://github.com/ntnu-susarc-cbf/GH-Scripts-2026/blob/a64fa2c539c52175742e0c354329a12b7c22b957/GH%20Images/DBT_Aswan.PNG)

### 1.2 Setting up the Energy Zone
![Zone Modelling](https://github.com/ntnu-susarc-cbf/GH-Scripts-2026/blob/a64fa2c539c52175742e0c354329a12b7c22b957/GH%20Images/Geometry.PNG)

### 1.3 Setting up the Tower Geometry
![Tower Geometry](https://github.com/ntnu-susarc-cbf/GH-Scripts-2026/blob/a64fa2c539c52175742e0c354329a12b7c22b957/GH%20Images/Script_tower.png)

### 1.4 Setting up the Seasonal Schedule for the Tower

It is important to find the overheated period for your weather, to make the most of the evaporative cooling effects, and avoid having an opposite effect on the total energy loads.

![Seasonal and Weekly Scheduling for the tower operation](https://github.com/ntnu-susarc-cbf/GH-Scripts-2026/blob/a64fa2c539c52175742e0c354329a12b7c22b957/GH%20Images/Script_Scheduling.png)

### 4.0 Setting up the Simulation Setup for custom outputs
![Simulation Setup](https://github.com/ntnu-susarc-cbf/GH-Scripts-2026/blob/a64fa2c539c52175742e0c354329a12b7c22b957/GH%20Images/simulation%20setup_ECT.png)


## 2. Simulation Outputs/Results

### 2.1 Reading the Custom Results
![Custom Results reading](https://github.com/ntnu-susarc-cbf/GH-Scripts-2026/blob/a64fa2c539c52175742e0c354329a12b7c22b957/GH%20Images/custom_results_ECT.png)

![Zone Sensible Heat Energy Loss](https://github.com/ntnu-susarc-cbf/GH-Scripts-2026/blob/a60900103b8d67f5e932cd24a26844bb656e3347/GH%20Images/Zone%20Sensible%20Loss_ECT.png)


### 2.2 Energy Balance Chart comparison
![Energy Balance CHart_Without Evaporation Tower](https://github.com/ntnu-susarc-cbf/GH-Scripts-2026/blob/a60900103b8d67f5e932cd24a26844bb656e3347/GH%20Images/Without%20Evaporation_ECT.png.png)

![Energy Balance Chart_With Evaporation Tower](https://github.com/ntnu-susarc-cbf/GH-Scripts-2026/blob/a60900103b8d67f5e932cd24a26844bb656e3347/GH%20Images/With%20Evaporation_ECT.png)



## Downloads_Realease_03-10-2026

***The files are created in Rhino 7 and use the Ladybug 1.10 version.***

[Download the Rhino File here](https://github.com/ntnu-susarc-cbf/GH-Scripts-2026/blob/b4835dd071a91f7e8b08557ce84773b7ba5ad4c6/Working%20Files/03_10_2026_Evaporative%20Cooling%20tower.3dm)

[Download the Grasshopper file here](https://github.com/ntnu-susarc-cbf/GH-Scripts-2026/blob/b4835dd071a91f7e8b08557ce84773b7ba5ad4c6/Working%20Files/03_10_2026_Evaporative%20Cooling%20tower.gh)
