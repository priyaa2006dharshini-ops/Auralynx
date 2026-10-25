# Auralynx — System Architecture

## 1. Overview

Auralynx is a proposed IoT-based assistive system designed to support neurodivergent individuals with personal safety, daily routines, and caregiver connectivity.

The system consists of a wearable device and a companion mobile application.

## 2. Main Components

### A. Wearable Device

* Collects movement data using a motion sensor.
* Uses a microcontroller to process sensor readings.
* Identifies potential safety events using configured detection logic.
* Communicates with a paired smartphone.

### B. Embedded Controller

The proposed ESP32 microcontroller will read sensor data, process the readings, and communicate detected events to the smartphone.

### C. Bluetooth Communication

Bluetooth Low Energy (BLE) is a proposed communication method between the wearable and a compatible smartphone.

### D. Mobile Application

The application is intended to:

* Display wearable status and notifications.
* Manage daily reminders and schedules.
* Receive safety events from the wearable.
* Support caregiver notifications through an appropriate communication service.

## 3. System Data Flow

1. The motion sensor collects movement measurements.
2. The microcontroller processes the sensor readings.
3. The detection logic evaluates whether a potential safety event has occurred.
4. The wearable sends relevant event information to the paired smartphone over Bluetooth.
5. The application displays a notification.
6. If configured and connectivity is available, the application forwards an alert to the designated caregiver.

The application also manages reminders and schedules independently of the wearable's event-detection process.

## 4. Architecture Diagram

```text
+--------------------------+
|     Wearable Device      |
|                          |
|  Motion Sensor           |
|         |                |
|         v                |
|  ESP32 Microcontroller   |
|         |                |
|  Event Detection Logic   |
+------------+-------------+
             |
             | Bluetooth Low Energy
             v
+--------------------------+
|    Mobile Application    |
|                          |
|  Safety Notifications    |
|  Daily Reminders         |
|  Scheduling              |
+------------+-------------+
             |
             | Internet / Notification Service
             v
+--------------------------+
|   Caregiver's Device     |
|                          |
|  Configured Alert        |
+--------------------------+
```

## 5. Proposed Technology

* Microcontroller: ESP32
* Motion sensor: To be finalized; MPU6050 is a candidate.
* Communication: Bluetooth Low Energy
* Firmware: Embedded C/C++
* Mobile application: Framework to be selected

## 6. Safety and Reliability Considerations

* Motion-based detection may produce false alerts or miss events.
* Bluetooth communication requires a compatible, paired device.
* Remote caregiver notifications depend on the phone, network availability, and notification service.
* Local functionality should be considered when connectivity is unavailable.
* Personal information should be protected and limited to what is necessary.

## 7. Current Status

This document describes the proposed architecture. Hardware selection, firmware development, mobile application integration, and system testing are pending or in progress and must be updated as implementation advances.

## 8. Future Improvements

Potential future developments include personalized detection settings, additional daily organization features, improved notification reliability, and usability evaluation.
