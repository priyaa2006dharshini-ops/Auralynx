# Auralynx — Hardware Components

## 1. Overview

Auralynx is a proposed wearable assistive system designed to support personal safety and daily living activities for neurodivergent individuals.

The following components are candidates for the initial prototype. The final selection will depend on the system requirements and hardware testing.

## 2. Proposed Components

### 2.1 ESP32 Microcontroller

**Purpose:** Main processing unit.

* Reads data from connected sensors.
* Processes sensor measurements.
* Implements the configured event-detection logic.
* Supports wireless communication with a compatible smartphone.

### 2.2 MPU6050 Accelerometer and Gyroscope

**Purpose:** Motion sensing.

* Measures acceleration along three axes.
* Measures angular velocity along three axes.
* Provides movement data that can be evaluated for potential fall detection.

The sensor cannot independently confirm that a fall has occurred. Detection logic must be developed and tested.

### 2.3 Battery and Power Management

**Purpose:** Power supply for the wearable.

* Provides portable power to the electronic components.
* Requires suitable voltage regulation and charging protection.
* Must be selected according to the final circuit's voltage and current requirements.

The battery type and capacity are yet to be finalized.

### 2.4 Bluetooth Low Energy (BLE)

**Purpose:** Wireless communication.

* Transfers relevant event information between the wearable and a compatible smartphone.
* Supports communication over a limited wireless range.
* Does not independently provide internet connectivity or deliver remote caregiver notifications.

### 2.5 Smartphone

**Purpose:** User interface and communication gateway.

* Receives information from the wearable.
* Displays configured safety notifications.
* Runs the proposed companion application.
* Supports reminders, schedules, and caregiver notifications when the required services are available.

## 3. Proposed Hardware Architecture

Motion Sensor
↓
ESP32 Microcontroller
↓
Event Detection
↓
Bluetooth Low Energy
↓
Smartphone Application
↓
Caregiver Notification Service

## 4. Component Selection Considerations

The final components should be selected based on:

* Cost and availability.
* Power consumption.
* Wearable size and comfort.
* Sensor performance.
* Communication reliability.
* Ease of programming and integration.
* Safety and suitability for the intended use.

## 5. Current Status

The components listed above are proposed candidates, not a declaration of a completed hardware prototype.

Final component selection, circuit design, pin assignments, power requirements, and integration testing will be documented as development progresses.
