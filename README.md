# digital-building-twin
## Summary
<img src="/digitaltwinautodesk.png" style="float: left; margin-right: 20px; max-width: 200px;">

# Digital Building Twin Project

## Project Description

This project focuses on developing digital twins for visaulization of environmental conditions, energy usage within a physical building. The framework is demonstrated using a case study of Bishop-Favrao Hall, the home of the Department of Building Construction at Virginia Tech. This digital twin provides real-time visualization of environmental conditions, including temperature, humidity, lighting levels, air quality, within the building. 

## Video Demo

[![Watch the demo video](https://img.youtube.com/vi/unOPUtw5rmc/0.jpg)](https://youtu.be/unOPUtw5rmc)  
*Click on the image to view the video.*



### Technical Implementation
- **Environmental Data Collection**:  
   Environmental and energy data are collected using a network of sensors interfaced with a Raspberry Pi 4B single-board computer. Key sensors include:  
   - **DHT11 Humidity and Temperature Sensor**: Measures ambient temperature and relative humidity.  
   - **Light Intensity Sensor**: Monitors lighting levels to evaluate energy usage.  
   - **MQ-2 Gas Sensor**: Detects airborne pollutants and combustible gases to assess indoor air quality.  
   - **Groove Smart Plug**: Tracks energy consumption of key systems, such as HVAC and lighting.
- **Data Processing and Transmission**:  
   Sensor data is processed using Python libraries like `Adafruit_DHT` and `Rpi.GPIO`. Once processed, the data is transmitted to the digital twin platform via a REST API built with Flask, formatted in JSON.
- **Real-Time Integration**:  
   The Autodesk Platform Service’s Model Derivative API is utilized to overlay the collected environmental data onto the BIM model, enabling dynamic visualization within the digital twin environment.




## 🛠️ Detailed Setup Guide

### 1. Prepare the Revit Model

Create or export a Revit model of the building you want to digitize. This model will be used as the basis for visualization within Autodesk Platform Services (APS).

### 2. Set Up Autodesk Platform Services (APS) for IoT

Follow the official APS IoT integration guide to set up the cloud-based digital twin environment:
👉 [APS IoT Extensions Demo GitHub Repository](https://github.com/autodesk-platform-services/aps-iot-extensions-demo)

This will allow you to visualize sensor data on top of your BIM model.

### 3. Deploy Raspberry Pi Sensor Server

Use the provided `myserver.py` script in the `raspberrypi/` folder to host real-time sensor data.

#### Steps:
- Ensure your Raspberry Pi is connected to the following sensors:
  - DHT11 (Temperature & Humidity)
  - Light Sensor
  - MQ-2 Gas Sensor
- Run the server:
python3 myserver.py


This script will create a local web server (localhost) that serves JSON-formatted sensor data, updated every 5 seconds.

### 4. Connect Sensor Data to the Digital Twin
To feed live sensor data into your digital twin:

Open:
digital-building-twin/Digital twin_1_realtime data/public/dataview.js

Modify the file to include a GET request that pulls data from the Raspberry Pi REST API (e.g., http://<raspberry-pi-ip>:5000/data).

This integration allows live environmental data to be embedded and visualized in the Autodesk BIM model hosted on the APS platform.


