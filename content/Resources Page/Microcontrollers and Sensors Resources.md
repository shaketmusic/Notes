

# Arduino

## Getting Started

- [Arduino – Getting Started with Arduino](https://docs.arduino.cc/learn/starting-guide/getting-started-arduino/)
- [Mario’s Ideas – PullUp and PullDown Resistors](https://www.youtube.com/watch?v=87X5Duad8CU)

## Workshops

- [YouTube Playlist – Arduino Workshop for Beginners](https://www.youtube.com/playlist?list=PLPK2l9Knytg5s2dk8V09thBmNl2g5pRSr)

## Tutorials

- [Arduino – Digital Potentiometer Control](https://docs.arduino.cc/tutorials/communication/DigitalPotControl/)

## Reference

- [Arduino – Language Reference](https://www.arduino.cc/reference/en/)

# Arduino – Max Communication

## Cycling ‘74

- [Max Comm Tutorial 2: Serial Communication](https://docs.cycling74.com/max8/tutorials/communicationschapter02)

<aside>
⚠️

Occasionally, Max won’t successfully receive data from the Arduino board. Here are some things you can try (I recommend reviewing them in top-to-bottom order):

- Verify that your Arduino sketch is free of errors and that it has been successfully flashed to your Arduino board.
- Make sure that the Serial Monitor and the Serial Plotter in the Arduino IDE are closed. This is due to the Serial protocol being a one-to-one communication stream. If your Arduino board is talking to the Arduino IDE, it won’t be able to communicate with Max.
- With your board connected and your Serial port identified in Max, try pressing the physical Reset button on the Arduino board. This will reinitialize the Arduino board, restarting the sketch.
- Verify your Max patch. The image below shows a Max patch that utilizes a `dtr` message being fed into the `serial` object. The DTR (Data Terminal Ready) message was used in the past to let a device know that the receiver was ready to exchange information. In the current iteration of Arduino, the DTR message provides a way to “press” the Reset button digitally, meaning that it will reinitialize the board.
    
    ![MaxArduino_Troubleshooting.png](19cce77f-7c6b-47e7-956c-c196050b48d2.png)
    
- Try a different USB port.
</aside>

## Misc.

- [ASCII Table](https://www.asciitable.com/)

# Sensors

- Ultrasonic Sensor
    - [Last Minute Engineers – Ultrasonic Sensor](https://lastminuteengineers.com/arduino-sr04-ultrasonic-sensor-tutorial/)

# Teensy

## Teensy 4.0 Pinout

![Teensy4_Pinout_Front.png](Teensy4_Pinout_Front.png)

## Documentation

- [Using Digital I/O Pins](https://www.pjrc.com/teensy/td_digital.html)
- [Using the Teensy Loader in macOS](https://www.pjrc.com/teensy/loader_mac.html)
- [Using USB MIDI](https://www.pjrc.com/teensy/td_midi.html)

## Audio Shield Workshop

### Pins

![Teensy4_AudioShield_Pins.jpg](Teensy4_AudioShield_Pins.jpg)

### Advanced Microcontroller Audio Workshop

- [This](https://www.pjrc.com/store/audio_tutorial_kit.html) is the Kit used for the workshop.
- Here is the workshop documentation:
    
    [TeensyAudioWorkshop.pdf](TeensyAudioWorkshop.pdf)
    
- Here is the video walkthrough:
    
    [https://www.youtube.com/watch?v=wqt55OAabVs&ab_channel=PaulStoffregen](https://www.youtube.com/watch?v=wqt55OAabVs&ab_channel=PaulStoffregen)