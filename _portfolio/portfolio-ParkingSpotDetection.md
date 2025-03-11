---
title: "App-based Empty Parking Spot Detection"
excerpt: "The project was aimed to detect empty vehicle spots in parking by mobile based application with the help of sensors implemented using an Arduino board. Wrote the Arduino code to help detect cars using UV sensors and to change the color of LEDs.  The data was visualized on mobile app using Bluetooth.<br/>
[![Parking Mini](https://navoditamathur.github.io/files/1..png)](https://navoditamathur.github.io/portfolio/portfolio-ParkingSpotDetection/)"
collection: portfolio
tags: 
  - IoT
---

Objective:
------
To design and implement an intelligent parking system that detects and displays the availability of parking spots in real-time. The system aims to simplify the parking process for users by providing accurate and immediate information on parking space occupancy through a mobile application and various display components.

Introduction:
------
This project aims to enhance parking efficiency through an intelligent car parking system. By leveraging infrared technology and Arduino sensors, the system provides real-time data on parking slot availability, simplifying the parking process and improving user experience.

Key Components:
------
- Infrared Transmitters and Receivers: Positioned in each parking lane, these components are critical for detecting the presence or absence of vehicles, ensuring accurate monitoring of slot occupancy.
- LED Indicators: Each parking slot features an LED that changes color to indicate whether the spot is occupied or available.
- LCD Display: Installed at the parking entrance, the LCD display provides an overview of parking slot status across all lanes.
- Mobile Application: Data from the sensors is visualized on a mobile app via Bluetooth, allowing users to view real-time parking information.
  
System Workflow:
------
- Sensor Detection: Infrared transmitters and receivers detect vehicle presence in each parking spot.
- LED Indicators: LEDs in each lane signal the availability of parking spots by changing color (e.g., green for available, red for occupied).
- Entrance Gate LCD Display: An LCD display at the entrance gate offers a visual summary of the parking area, showing the status of all lanes.
- Real-Time Monitoring: The system continuously monitors parking slot occupancy, providing immediate updates to users.<br/>
  ![Parking Mini](https://navoditamathur.github.io/files/MiniParking.png)
- Mobile App Visualization: Real-time data is transmitted via Bluetooth to a mobile app, allowing users to check parking availability remotely.<br/>
  ![Parking Mini](https://navoditamathur.github.io/files/MiniParking_app.png)
- Read more [here](https://navoditamathur.github.io/files/ParkingMiniProject.pdf)
  
Benefits:
------
- Efficient Parking Navigation: Helps drivers quickly locate available parking spots, reducing time spent searching for a space.
- Reduced Congestion: Minimizes traffic congestion by streamlining the parking process and reducing the time spent in search of parking.
- User-Friendly Interface: Offers an intuitive interface through LED and LCD displays, as well as a mobile app, enhancing user accessibility and experience.
- Optimized Space Utilization: Improves the management of parking spaces, preventing blockages and ensuring better use of available spots.

Deliverables:
------
- Functional Parking Detection System: A complete setup with infrared transmitters, receivers, LEDs, and LCD displays for real-time monitoring of parking spaces.
- Arduino Code: Custom code written for Arduino to detect vehicles using UV sensors and control LED indicators based on parking slot occupancy.
- Mobile Application: A Bluetooth-enabled mobile app that displays real-time parking availability and status.
