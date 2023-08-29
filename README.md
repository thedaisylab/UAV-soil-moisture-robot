# Aerial-robot-field-trial-original-data-and-programs-used
This repository contains the original data from the field trial and the programs used to get the data and operate the robot.
The gyro data folder contains the accelerometer and height sensor data, the soil moisture data consists of .txt files per replicate, and the lift data contains the linear potentiometer data during sensor insertion.
A simplified overview of the project is a soil moisture payload was developed and mounted on a UAV. The payload should measure soil moisture at three locations upon landing and inform the UAV to fly to the next location autonomously. MyRIO was used for controlling the movements of linear motor sliders and saving the measured data in its internal memory. MyRIO was also used to power the Arduino Mega using the USB connection. The system architecture design is shown in the below figure.
![image](https://github.com/hemanthd95/Aerial-robot-field-trial-original-data-and-programs-used/assets/97570253/a2405d50-13e9-4b80-a4c8-7da4a68d6b63)

The LabVIEW program contains the state machine logic that was used to control the sensor insertion, move the sensor, and record soil moisture data. The logic workflow in LabVIEW is explained in detail in the below figure.
![image](https://github.com/hemanthd95/Aerial-robot-field-trial-original-data-and-programs-used/assets/97570253/d824edba-b7a5-45af-bfb2-3f44966eb114)

The Arduino program was used to measure soil moisture, send it to myRIO, and upload new flight plans so that the UAV could fly to the next location.
         SDI-12 library was used to get soil moisture data and TDR waveform data. The sensor address was 3. The power data pin was connected to the Arduino Mega Digital pin (11). The UART 1 ports were connected to myRIO UART ports to establish the novel two-way communication. The waveform data was obtained from 1995 to 6000 picoseconds.
The R program was used to post-process the data and get tabulated forms of soil moisture data with the respective GPS coordinates.
