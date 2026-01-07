# Project NebulaX - Cloud-Enabled Intelligent Workplace Safety & Risk Monitoring System

## Introduction
This project demonstrates the integration of cloud processing and monitoring capabilities to manage sensor data effectively. It highlights a system designed to collect sensor data, process it through cloud infrastructure, and visualize the results via a web interface.

## Table of Contents
1. [Project Overview](#project-overview)
2. [System Overview](#system-overview)
3. [Flow Chart](#flow-chart)
4. [Hardware Components](#hardware-components)
5. [Technologies and Services](#technologies-and-services)
6. [Circuitry](circuitry)

## Project Overview

**Key Features:**
- **Cloud Integration:** Efficiently collects and transmits sensor data to the cloud for processing and storage.
- **Cloud Services Utilization:** Utilizes various cloud services for data processing and storage.
- **Visualization through Website Interface:** Showcases stored data visually via a website interface, enabling insights and informed decision-making.
- **Analytics Tools Integration:** Incorporates analytics tools for data analysis, providing deeper insights.
- **Raspberry Pi Control:** Demonstrates the system's capability to control the Raspberry Pi, triggering specific actions, highlighting its versatility and control over the IoT environment.

## System Overview
### Hardware/System
- **User Check-In:** Collects temperature data and evaluates user suitability.
- **Work Time:** Monitors environmental factors during work hours.
- **Off Work Turn On Security:** Activates sensors for security when off work.
- **Web Control:** Responds to MQTT messages to control system functions.
- **Turn Off System:** Closes all connections and terminates the program.

### Cloud Processing & Monitoring (AWS Services)

1. **AWS IoT Core**
   - Uses MQTT for sending/receiving messages.
   - IoT Rules direct data to specific services (Lambda, IoT Analytics).

2. **Lambda Function**
   - Processes IoT data, sends it to DynamoDB, and triggers events (AWS SNS).

3. **AWS Analytics**
   - Utilizes IoT Analytics Channel, Pipeline, and Data Store to store raw data in an S3 bucket.
   - SageMaker enables data analysis through a Jupyter Notebook instance.

### Website (PHP-based)

1. **Login and Sign-up Pages**
   - User authentication for system access.

2. **Main Page**
   - Displays processed data stored in DynamoDB.
   - Provides buttons for users to control work mode.

## Flow Chart:
![IOT Project](https://private-user-images.githubusercontent.com/56661548/290019767-1563438d-a8e9-49d6-bb72-3b534a14d887.png?jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3Njc3NzUzOTgsIm5iZiI6MTc2Nzc3NTA5OCwicGF0aCI6Ii81NjY2MTU0OC8yOTAwMTk3NjctMTU2MzQzOGQtYThlOS00OWQ2LWJiNzItM2I1MzRhMTRkODg3LnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNjAxMDclMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjYwMTA3VDA4MzgxOFomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPWQ4YjgyYzdlYTJkYWJkNWI4Mjk3MjU0OWQ0OWUyNDk1MzExZmIxNzEyYWQ1MjFjODEyZDgwZTYyYmQ5NTQ2ZjUmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0In0.xOM8fHAKQvr4q9CSPZHsgz7KdTePmlLxGQNP3kkHkX0)

## Hardware Components:

- **Raspberry Pi:** Microcontroller acting as the system's brain.

- **DHT11 Temperature / Humidity Sensor:** Detects surrounding temperature and humidity.

- **Flame Sensor:** Detects the presence of a flame in front of the sensor.

- **MQ-2 Gas Sensor:** Detects various gases like LPG, i-butane, propane, methane, alcohol, Hydrogen, and smoke in the surroundings.

- **Collision Sensor:** Detects collisions with the sensor.

- **LED:** Light emitting diode.

- **ADC (Analog to Digital Converter):** Converts analog signals to digital.

## Technologies and Services:

- **MQTT (MQ Telemetry Transport) Protocol:** Lightweight, publish-subscribe, machine-to-machine network protocol, primarily used in IoT.

- **AWS IoT Core:** Managed cloud service facilitating secure communication between IoT devices and the AWS Cloud through MQTT.

- **AWS IoT Analytics:** Processes and analyzes IoT data at scale, enabling data collection, storage, processing, querying, and integration with other AWS services for comprehensive analytics.

- **AWS DynamoDB:** Fully managed NoSQL database service providing seamless scalability, high availability, and low-latency data storage and retrieval.

- **AWS SageMaker:** Platform for building, training, and deploying machine learning models at scale.

- **Amazon S3 (Simple Storage Service):** Scalable, secure, highly available object storage service for storing and retrieving any amount of data.

- **AWS Lambda:** Serverless computing service allowing code execution without server management.

- **AWS SNS (Simple Notification Service):** Fully managed messaging service for publishing and delivering messages to endpoints or distributed systems.

- **IAM (Identity and Access Management) User:** Represents a person or application in the AWS environment, granting specific permissions based on policies assigned by an AWS account administrator.

- **User-end Website:** Monitors and allows admin users to view employee health and workplace conditions. Implements security features like Strong Password Rule, Hashing, and Session Control.

    - **Strong Password Rule:** Requires users to input a strong password with uppercase, numbers, and symbols for signup.

    - **Hashing:** Converts plaintext passwords into irreversible hashed values before saving in the database, enhancing security.

    - **Session Control:** Authenticates, authorizes users, manages session timeouts, implements secure protocols (like HTTPS), and monitors for suspicious activities or unauthorized access within user sessions.
 
## Circuitry:
![IMG_0087](https://private-user-images.githubusercontent.com/56661548/290021630-792e522f-2fb6-4552-9c81-e3d35ee0a6ed.JPG?jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3Njc3NzUzNjMsIm5iZiI6MTc2Nzc3NTA2MywicGF0aCI6Ii81NjY2MTU0OC8yOTAwMjE2MzAtNzkyZTUyMmYtMmZiNi00NTUyLTljODEtZTNkMzVlZTBhNmVkLkpQRz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNjAxMDclMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjYwMTA3VDA4Mzc0M1omWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTU1NmQ2ZjQyMGQ2NTJiOTUzMTc2N2UwZWY3N2Q3YmQ1MWZlMGZhMGRmNzY1MWEwZTkxODM1ODE4YWJlYWVmNjgmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0In0.sIbDX4A6OONSQlyWrAqtkiBmhScip7XDdArO96gm_x4)
