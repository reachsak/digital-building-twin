# digital-building-twin
## Summary
<img src="/digitaltwinautodesk.png" style="float: left; margin-right: 20px; max-width: 200px;">

# Digital Building Twin Project

## Project Description

This project focuses on developing digital twins for visaulization of environmental conditions, energy usage within a physical building. The framework is demonstrated using a case study of Bishop-Favrao Hall, the home of the Department of Building Construction at Virginia Tech. This digital twin provides real-time visualization of environmental conditions, including temperature, humidity, lighting levels, air quality, within the building. 

## Video Demo

[![Watch the demo video](https://img.youtu.be/unOPUtw5rmc/0.jpg)](https://youtu.be/unOPUtw5rmc)  
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

### Requirements
- Open-source Large language model (e.g., LLaMA)
- Generative AI inference tool. llama.cpp
- Python 3.10
- Raspberry Pi and IoT sensors

## Detailed setup guide
Coming soon.....

## License
This project is licensed under the MIT License.
