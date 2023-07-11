# Emulation of EcoLight+ on a Jetson Nano Developer Kit from a Simulation of Ecolight+ on Sumo

**Authors**

- Blasco Stanislas, Engineering School, ENSEA Cergy (France).

- Uljana Reinsalu.

- Sadok Ben Yahia, Department of Software Science, Tallinn University of Technology.


**Introduction**

This projetct proposes a emulation of a DDDQN reinforcement learning based intelligent traffic light control system : Ecolight+. This emulation is based on a jetson nano developer kit
This project proposes a DDDQN reinforcement learning based intelligent traffic light control system. Simply run the runexp.py to run the experiment. Please change the parameters in conf/ folder and runexp.py correspondingly if needed. Also, please specify the location of TraCI module in map_computor.py if necessary.

Before implementing on jetson nano you need to run it on your computer. Please follow the instruction from : https://github.com/doua-ounoughi/EcoLightPlus

Before running above codes, you may need to install following packages or environments:

- Python 3.6
- SUMO 0.32 with TraCI module. Please specify TraCI location correpsondingly in map_computor.py
- Keras 2.2.0 and Tensorflow 1.9.0


**Data**

To get the intersection environment files:

- Go under the installed SUMO folder `/usr/share/sumo/tools`
- Run: `python osmWebWizard.py` a webwizard map would open on a browser.
![WebWizard map](webwizard.png)
- Select the intersection on the map and the parameter on the right about the type of vehicles, roads, etc.


- Press `"Generate Scenario"`, a sumo GUI interface would pop-up to generate the traffic flow.
- Now go to your Home directory, and copy the created folder (named with the current time) under `/data/one_run/m`

The format of the noise prediction model inputs:

- Columns: `[Timestamp	TN_Noise_Level_DB	IW_Temp_C	IW_Air_Pressure_mmHg	IW_Air_Humidity_Percent	IW_Wind_Speed_MH	IW_Rain_MMH	TT_P1_Current_Speed_Kmh	TT_P1_Freeflow_Speed_Kmh	TT_P1_Speed_Diff_Kmh	TT_P1_Current_Travel_Time_Sec	TT_P1_Freeflow_Travel_Time_Sec	TT_P1_Travel_Time_Diff_Sec	Hour	Minute	Day_Of_Month	Day_Of_Week	IW_Wind_Direction_Mark	IW_Weather_Cloudiness_Class	IW_Sunrise_Hour	IW_Sunrise_Minute	IW_Sunset_Hour	IW_Sunset_Minute	TT_P1_Road_Type_Class	TT_P2_Road_Type_Class	TT_P1_Is_Road_Closed	TT_P2_Is_Road_Closed	car	motorbike	bus	truck]`

- Frequency: 1 minute


**Files in the folder**

The files are functioning like this:

- `EcoLight+.ipynb`

  The experiments notebook.

- `run.py`

  Load the experiment setting, and call traffic_light_agent.

- `traffic_light_dqn.py`

  Simulate the reinforcement learning agent. This file simulates the timeline, get current state from sumo_agent, get current state from sumo_agent and call the agent to make decision.

- `sumo_agent.py`

  Interact with map_computor to get state, reward from the map_computor, and convey action to map_computor.

- `map_computor.py`

  Read data from SUMO and operate SUMO.

- `agent.py`

  Abstract class of agent.

- `network_agent.py`

  Abstract class of neural network based agent.

- `dueling_agent.py`

  Class of our method.

- `conf/`

  Configuration files.

- `data/`

  Traffic flow files. The intersection is connected with four road segments of 300-meters long.

- `OHANA.py`

  The noise prediction model class file.







