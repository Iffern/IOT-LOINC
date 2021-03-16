# Personal Compliant Smart Medical Devices with the LOINC standard - simulation of renting medical devices for clinic patients

### Description

The project presents backend for medical devices management.

Program consists of four main parts:
- Doctor Manager - part responsible for communication with doctor, it enables pairing medical devices with patients and shows patient's medical data
- Devices Manager - part responisble for devices management, it adds LOINC info to database, saves patient's measurements in database and handles devices disconnection
- Device - device mock
- Database Manager - part responsible for communication with database

The doctor can pair device with patient, and then when patient will make measure with that device, the information from the device should be save in database. Doctor can have access to patient's measurement any time, as the data is immediately stored in cloud.

### Technology

Devices' mocks were designed to meet LOINC (https://loinc.org/) and IEEE 11073 standard (https://loinc.org/collaboration/ieee/). 

All parts of the program communicate with MQTT.

Devices are connected on AWS IoT Core, where their state is also being stored.

To store the patients' data and other important information about system, AWS Cloud Relational Database with PostgreSQL is used.
