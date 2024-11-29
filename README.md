# Efficient-Data-Stream-Anomaly-Detection
Efficient Data Stream Anomaly Detection using python 

####Objective: 
To develop a Python script capable of detecting anomalies in a continuous data stream. This stream, simulating real-time sequences of floating-point numbers, could represent various metrics such as financial transactions or system metrics. Your focus will be on identifying unusual patterns, such as exceptionally high values or deviations from the norm

#####Data Stream Simulation:
Rather than taking an external source, I am simulating the data.

data_stream_simulation(length=1000, anomaly_chance=0.01) to generate a data stream of -
Length: 1000
Anomaly Chance: On each data point, there's a 1% chance that the point will be an anomaly (a large spike).
