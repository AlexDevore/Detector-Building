# Water Quality Monitoring System with Arduino

## Monitor Water Quality with Arduino

Welcome to the Water Quality Monitoring System project! This Arduino-based application measures and displays multiple readings such as temperature, voltage, and concentration of salt in water (PPM) on a 16x2 LCD screen.

## Introduction

This project uses an Arduino to measure various water quality parameters when a probe is placed in water. The data is presented on a 16x2 LCD screen. The project was initially created for the Science Olympiad competition under the detector building category and later modified for a science fair competition, where it won first place. The current version includes a temperature sensor that needs further calibration. The probe was made by hot-gluing four jumper wires onto a BIC pen.

## Components Used

- Arduino UNO R3
- 16x2 LCD with I2C interface (0x27 address)
- Various resistors
- Numerous jumper cables
- Breadboard
- Red, Green, and Blue LEDs
- Diodes
- Voltage Detection Module DC 0~25V Voltage Sensor for Arduino

## Libraries

- **LiquidCrystal_I2C**: Used for interfacing with the I2C-enabled LCD.

## Installation and Usage Instructions

### Prerequisites

To compile and run this application, you need to have the Arduino IDE installed on your machine.

### Setup

1. Connect the components as described in the components list.
2. Download the `LiquidCrystal_I2C` library from the Arduino Library Manager.
3. Upload the code to the Arduino.

### Usage

1. Power on the Arduino.
2. Place the probe in the water to start measuring.
3. The readings for temperature, voltage, and salt concentration (PPM) will be displayed on the LCD screen.

### Example Output

The system will display readings like:
```
Temp: 25.00C
Voltage: 5.00V
Salt: 500PPM
```

## Code Overview

The code includes variables and functions to manage the sensor readings, display data on the LCD, and control the RGB LED based on voltage levels.

### Key Variables

- **B**: B value of the thermistor
- **R0**: Reference resistance of the thermistor
- **pinTempSensor**: Pin connected to the temperature sensor
- **sensorPin**: Pin connected to the analog voltage sensor
- **RED, GREEN, BLUE**: Pins for RGB LED output
- **flipFlop**: Boolean variable to control LED alternation
- **tw, tm**: Timing variables for LED alternation and measurements
- **Temp, sensorInput, PPM**: Variables for temperature, sensor input, and salt concentration
- **lcd**: `LiquidCrystal_I2C` object for controlling the LCD

### Main Loop

- Alternates LED states to indicate the system is active.
- Performs measurements every 2 seconds.
- Calculates temperature, voltage, and PPM.
- Displays the results on the LCD.
- Changes the color of the RGB LED based on voltage level.

## Contributor Expectations

If you'd like to contribute to this project, please follow these guidelines:

1. **Fork the repository**: Create a personal copy of the repository on your GitHub account.
2. **Create a new branch**: Use `git checkout -b branch-name` to create a new branch for your feature or bugfix.
3. **Commit your changes**: Use descriptive commit messages to explain your changes.
4. **Push to the branch**: Push your changes to your forked repository using `git push origin branch-name`.
5. **Create a pull request**: Submit a pull request to the original repository with a detailed description of your changes.

## Known Issues

- The temperature sensor needs further calibration.
- The system might show incorrect readings if the probe is not properly constructed or placed.

## My Own Data

![Capture](https://github.com/AlexDevore/Detector-Building/assets/97128910/54a42a11-ca4b-47b0-bbf7-611e52cc37af)
![image](https://github.com/AlexDevore/Detector-Building/assets/97128910/1ee50b7b-433e-4de5-aa74-351ac918d6b0)

## Works Cited

- [Digital Voltmeter using Arduino & 16x2 LCD](https://theiotprojects.com/digital-voltmeter-using-arduino-16x2-lcd/)
- [Measuring Salt Concentration with AC](https://www.instructables.com/Measuring-salt-concentration-with-AC/)
- [Probe Activity](https://www.teachengineering.org/activities/view/nyu_probe_activity1)
- [Interface DC Voltage Sensor with Arduino](https://theiotprojects.com/interface-dc-voltage-sensor-with-arduino/)
- [Detector Building Project Repository](https://github.com/Haadi-Khan/Detector-Building)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgements

- [Arduino Documentation](https://www.arduino.cc/reference/en/)
- [LiquidCrystal_I2C Library](https://github.com/johnrickman/LiquidCrystal_I2C)

Feel free to reach out with any questions or suggestions!
