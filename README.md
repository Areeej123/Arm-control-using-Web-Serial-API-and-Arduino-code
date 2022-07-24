# Arm-control-using-Web-Serial-API-and-Arduino-code


## What is the Web Serial API?
The Web Serial API provides a way for websites to read from and write to a serial device with JavaScript. 
Serial devices are connected either through a serial port on the user's system or through removable USB and Bluetooth devices that emulate a serial port.

## What does this repository contain?
I included in this repository the JavaScript code that contains Web Serial API for Open a serial port and Write to a serial port to control the robot arm to the right and to the left by converting the speech on the site to text and sending it to the Arduino code, and thus when we say right It moves to 0 degrees, and when we say left, it moves to 180 degrees

## How can you try this code:
- First you have to open the html file in Chrome browser.
- Open the Arduino code in the Arduino IDE.
- Then you have to connect the servo to the Arduino and connect the Arduino piece to the USB wire of your device.
- After that, press the connect button "اتصال" on the page to connect to the Serial Port
### Simplified explanation of the code :
Calling requestPort() prompts the user to select a device and returns a SerialPort object. Once you have a SerialPort object, calling port.open() with the desired baud rate will open the serial port. The baudRate dictionary member specifies how fast data is sent over a serial line. It is expressed in units of bits-per-second (bps). Check your device's documentation for the correct value as all the data you send and receive will be gibberish if this is specified incorrectly. For some USB and Bluetooth devices that emulate a serial port this value may be safely set to any value as it is ignored by the emulation.
```js
// Prompt user to select any serial port.
const port = await navigator.serial.requestPort();

// Wait for the serial port to open.
await port.open({ baudRate: 9600 });
```
- After that, he has to click in the box designated to speak (you can say “يمين” to move to 0 degrees) or (you can say “يسار” to move to 180 degrees)
