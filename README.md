# Time series from IoT devices: anomaly detection and forecast 

A young couple wants to buy a house with connected devices and solar panels. The owner has collected and shared data from IoT devices. 
They would like me to analyze those, check eventual power consumption anomalies and have tips to optimize the installation. As a bonus they asked if I could predict future consumption using AI. This would help to decide whether to buy it or not, and to estimate the cost of eventual improvements.

![main](dom.jpg)

Those were my conclusions after EDA and application of anomaly detection and forecast algorithms:

- Consumption is high during the night, and increases significantly during hot months in the summer. This is likely due to air conditioning, house insulation may be improved.

- Almost no solar energy produced in the morning: panels orientation must be checked.

Application of CUSUM method for anomaly detection showed that there were some consumption spikes, correlated to the weather but no points of steady increase. Home appliances work well, no evident faults.

Models built with LightGBM can predict future energy consumption when weather information was added to the simple time information. 

Data for this study can be downloaded here: https://www.kaggle.com/datasets/taranvee/smart-home-dataset-with-weather-information


