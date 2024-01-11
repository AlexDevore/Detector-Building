# Water Quality Monitoring System with Arduino

This project used an Arduino to measure and display multiple readings such as temperature, voltage, and concentration of salt in water (PPM) when the probe is placed in water. The data is presented on a 16x2 LCD screen. The reason for creating this project was to compete in a competition called the Science Olympiad, where I was assigned a topic called detector building. I later modified the code, adding the temperature sensor for a science fair competition, where I won first place. The temperature sensor still needs to be fully fixed. To measure the data, I made a probe that was constructed by hot-gluing four Jumper wires onto a BIC pen.

# Some of the Components Used
  Arduino UNO R3 
  16x2 LCD with I2C interface (0x27 address)
  Many different types of resistors
  Numerous Jumper cables
  Breadboard
  Red LED
  Green LED
  Blue LED
  Diodes
  
  # Libraries
  LiquidCrystal_I2C: Used for interfacing with the I2C-enabled LCD.

  # Code Overview
  B: B value of the thermistor
  R0: Reference resistance of the thermistor
  pinTempSensor: Pin connected to the Grove Temperature Sensor
  sensorPin: Pin connected to the analog voltage sensor
  RED, GREEN, BLUE: Pins for RGB LED output
  flipFlop: Boolean variable to control LED alternation
  tw: Time for LED alternation (milliseconds)
  tm: Time for measurements (milliseconds)
  Temp, sensorInput, PPM: Variables for temperature, sensor input, and salt concentration
  lcd: LiquidCrystal_I2C object for controlling the LCD

  # Loop
  Alternating LED states to indicate the system is active.
  Performing measurements every 2 seconds.
  Calculating temperature, voltage, and PPM.
  Displaying the results on the LCD.
  Changing the color of an RGB LED based on voltage level.

  # Works Cited
https://theiotprojects.com/digital-voltmeter-using-arduino-16x2-lcd/
https://www.instructables.com/Measuring-salt-concentration-with-AC/
https://www.teachengineering.org/activities/view/nyu_probe_activity1

![Capture](https://github.com/AlexDevore/Detector-Building/assets/97128910/54a42a11-ca4b-47b0-bbf7-611e52cc37af)
![image](https://github.com/AlexDevore/Detector-Building/assets/97128910/1ee50b7b-433e-4de5-aa74-351ac918d6b0)

