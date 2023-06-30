# EcoLight+: A DDDQN Approach for Intelligent Traffic Signal Control driven by A Data Fusion Urban Noise Prediction Technique


**Introduction**


This project proposes a DDDQN reinforcement learning based intelligent traffic light control system. Simply run the runexp.py to run the experiment. Please change the parameters in conf/ folder and runexp.py correspondingly if needed. Also, please specify the location of TraCI module in map_computor.py if necessary.


Before running above codes, you may need to install following packages or environments:

- Python 3.6
- SUMO 0.32 with TraCI module. Please specify TraCI location correpsondingly in map_computor.py
- Keras 2.2.0 and Tensorflow 1.9.0





**Files in the folder**

The files are functioning like this:

- EcoLight+.ipynb

  The experiments notebook.

- run.py

  Load the experiment setting, and call traffic_light_agent.

- traffic_light_dqn.py

  Simulate the reinforcement learning agent. This file simulates the timeline, get current state from sumo_agent, get current state from sumo_agent and call the agent to make decision.

- sumo_agent.py

  Interact with map_computor to get state, reward from the map_computor, and convey action to map_computor.

- map_computor.py

  Read data from SUMO and operate SUMO.

- agent.py

  Abstract class of agent.

- network_agent.py

  Abstract class of neural network based agent.

- dueling_agent.py

  Class of our method.

- conf/

  Configuration files.

- data/

  Traffic flow files. The intersection is connected with four road segments of 300-meters long.

- OHANA.py

  The noise prediction model class file.


 

If you are new to SUMO, hope these slides can help you with a good start (http://personal.psu.edu/hzw77/posts.html#sumo-introduction).




