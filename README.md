# digital-building-twin
## Summary
<img src="/digitaltwinautodesk.png" style="float: left; margin-right: 20px; max-width: 200px;">

# Digital Building Twin Project: DAB-CPS Framework Implementation

## Project Description

This project focuses on the development and implementation of a dual digital twin system as part of the DAB-CPS (Decentralized Autonomous Building Cyber-Physical System) framework. The digital twins provide a comprehensive platform for monitoring and managing environmental conditions, energy usage, and space reservation within a physical building. The framework is demonstrated using a case study of Bishop-Favrao Hall, the home of the Department of Building Construction at Virginia Tech.

### Digital Twin Functionality

1. **Environmental and Energy Visualization**:  
   The first digital twin provides real-time visualization of environmental conditions, including temperature, humidity, lighting levels, air quality, and energy consumption within the building. 

2. **Space Reservation Monitoring**:  
   The second digital twin focuses on visualizing and managing the reservation status of the building's physical spaces, facilitating efficient utilization and management.

### Technical Implementation

- **Building Information Model (BIM)**:  
   The BIM model of Bishop-Favrao Hall was developed using Autodesk Revit 2024, serving as the foundation for integrating real-time sensor data.

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

### Visualization and Benefits

The developed digital twins allow DAO (Decentralized Autonomous Organization) members and facility managers to:
- Monitor real-time environmental conditions and energy usage.
- Gain insights into space utilization through the reservation status visualization.
- Make data-driven decisions for efficient building management and improved indoor environmental quality.

This project demonstrates the potential of integrating IoT, BIM, and real-time data visualization into digital twin frameworks, paving the way for smarter, more efficient building management systems.
