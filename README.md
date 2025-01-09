# ASCOM-Pololu-Tic-Focuser
ASCOM USB Motor focuser based on a Pololu Tic Motorcontroller. 

First install USB device driver from Pololu as well as the Tic Control Center.
These can be found at www.pololu.com/product/3135/resources for the Pololu Tic T 500.

Second use the ASCOM driver installer provided here.

This project provides an ASCOM driver for the Pololu Tic T500 Motor Controller, 
enabling precise control of a stepper motor for astrophotography and telescope focusing. 

The Tic T500 features:
- USB control without COM ports
- Voltage range: 4.5–35 V
- Microstepping options: Full, 1/2, 1/4, 1/8
- Current control: Up to 1.5 A (no cooling required)
- Adjustable speed and acceleration settings	

Setup: 
- Direct USB control: No need for additional microcontrollers (Arduino, etc.)
- Easy setup: Connect the stepper motor (4 phases) and power supply

Driver (v 0.1):
- compliant ASCOM focuser
- on startup it sets position to 25.000 setups of a total range of 50.000 steps (steps are not stored in controller when power cycle)
- driver implemented a monitoring task, constantly checking state of connection and power supply
- Step Size, speed, acceleration to be set in Tic Control Center for the moment

Planned driver enhancements:
- Support for additional Pololu Tic models
- Advanced setup options in ASCOM Setup Dialog (microstepping modes, current adjustments, etc.)

Requirements
- Pololu USB driver and Tic Controller software for initial configuration
- Compatible with tools like Deepsky Geek's Virtual Focuser for temperature compensation feature.

The driver currently supports the Tic T500 but can be adapted for other models.

