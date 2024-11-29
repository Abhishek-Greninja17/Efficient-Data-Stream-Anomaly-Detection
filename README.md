# Efficient-Data-Stream-Anomaly-Detection
Efficient Data Stream Anomaly Detection using python 

### Objective: 
To develop a Python script capable of detecting anomalies in a continuous data stream. This stream, simulating real-time sequences of floating-point numbers, could represent various metrics such as financial transactions or system metrics. Your focus will be on identifying unusual patterns, such as exceptionally high values or deviations from the norm

### Data Stream Simulation:
Rather than taking an external source, I am simulating the data.

data_stream_simulation(length=1000, anomaly_chance=0.01) to generate a data stream of -
Length: 1000
Anomaly Chance: On each data point, there's a 1% chance that the point will be an anomaly (a large spike).

### Algorithm: Exponential moving average (EMA)
Use: To smooth the data and detect anomalies as deviations from the smoothed value. EMA allows adaptation to concept drift
EMA formula at time 't'
EMA(t) = a.X(t) + (1 - a).EMA(t-1)
where,
a = smoothing factor : controls how much weight is given to the current data point versus the previous EMA
a = 2/(N-1) where N = no. of periods or window size
X(t) = the current data point at time 't'
EMA(t-1) = EMA from the previous time step t-1

### Anomaly Detection:
A Z-score based on the difference between the current value and the EMA. A high absolute Z-score indicates an anomaly

### Stream Anomaly Detection and Real-Time Plotting
Simulate Real-Time Data Handling: By using a sliding window, it processes incoming data points one at a time and performs computations only when the window is full.
Compute Anomalies: It calculates the EMA and detects anomalies using Z-scores based on the data in the window.
Visualize Data and Anomalies: It updates the plot in real-time to reflect the current data stream, EMA, and detected anomalies.
Efficient Plot Updates: Only updates the plot every few data points to reduce overhead.

