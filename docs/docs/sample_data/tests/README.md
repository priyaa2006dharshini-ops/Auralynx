# Auralynx — Test Cases

## 1. Purpose

This document describes the planned tests for evaluating Auralynx's wearable sensing, communication, reminders, and notification functions.

## 2. Test Cases

| Test ID | Function                | Test Procedure                                          | Expected Result                                                         |
| ------- | ----------------------- | ------------------------------------------------------- | ----------------------------------------------------------------------- |
| TC01    | Sensor data             | Supply valid sample motion readings                     | Readings are parsed correctly                                           |
| TC02    | Data validation         | Supply missing or invalid readings                      | Invalid data is handled safely                                          |
| TC03    | Movement processing     | Supply sample movement measurements                     | Processing produces the expected output                                 |
| TC04    | Event detection         | Supply test data representing a predefined safety event | Detection logic responds according to its configured rules              |
| TC05    | Bluetooth communication | Connect the wearable to a compatible phone              | Connection status is reported correctly                                 |
| TC06    | Connection loss         | Disconnect the paired phone                             | The system detects the disconnection where supported                    |
| TC07    | Reminders               | Configure a daily reminder in the application           | The reminder appears at the scheduled time                              |
| TC08    | Caregiver notification  | Trigger a simulated safety event                        | The configured notification pathway is exercised                        |
| TC09    | Missing connectivity    | Disable network access                                  | The system handles unavailable remote notifications appropriately       |
| TC10    | Data privacy            | Review stored data and application permissions          | Only necessary data is collected and access is appropriately restricted |

## 3. Testing Notes

* These are planned test cases, not completed test results.
* Simulated data can be used during initial software testing.
* Hardware tests must be conducted after the relevant components are integrated.
* Fall-detection performance must be evaluated under controlled conditions.
* No test should put a person at risk.
* Remote notification delivery depends on the implemented communication service and network availability.

## 4. Current Status

Testing will be performed progressively as the firmware, wearable hardware, and mobile application are developed.

Actual results, including failures and limitations, should be recorded after each test is conducted.
