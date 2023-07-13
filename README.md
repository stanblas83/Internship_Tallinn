# Emulation of EcoLight+ on a Jetson Nano Developer Kit from a Simulation of Ecolight+ on Sumo


**Authors**

- Blasco Stanislas, School of Engineering, ENSEA Cergy France.

- Uljana Reinsalu.

- Sadok Ben Yahia, Department of Software Science, Tallinn University of Technology.


**Introduction**


This project proposes a emulation on jetson nano developer kit for a DDDQN reinforcement larning based intelligent traffic light control system : Ecolight+. First step you need to run the algorithm on your computer by following this : https://github.com/doua-ounoughi/EcoLightPlus. Next, you simply run Record_data_from_sumo taking the folder data of your first simuation. Then you need to run Emulated_on_jetson on your device taking the folder sumo_record_data from Record_data_from_sumo.



Before running above codes, you may need to install following packages or environments on your jetson nao developer kit:

- Python 3.6
- Tensorflow 2.7.0
- Keras 2.6.0 


**Files in the folder**

The files are functioning like this:

- `Ecolight+`

  Run the algorithm on your computer.

- `Record_data_from_sumo`

  Record data from sumo to emulated from our jetson nano without launch sumo

- `Emulated_on_jetson`

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








