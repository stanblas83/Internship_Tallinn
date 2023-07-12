# EcoLight+: A DDDQN Approach for Intelligent Traffic Signal Control driven by A Data Fusion Urban Noise Prediction Technique


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

  Run the algorithm on your jetson nano 








