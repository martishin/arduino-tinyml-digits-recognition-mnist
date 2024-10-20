# Arduino TinyML Digits Recognition
Arduino TinyML project that uses a ML model to recognize digits, the model was trained using the MNIST dataset, [link to the project](https://studio.edgeimpulse.com/studio/537816).

## Tested Devices

The project has been tested on the following devices:
- [Arduino Nano 33 BLE Sense](https://store.arduino.cc/usa/nano-33-ble-sense-with-headers) with [OV7675 camera](https://store.arduino.cc/en-de/products/arducam-camera-module)

## How to Run
Add the project to [Arduino IDE](https://www.arduino.cc/en/software/) using `Sketch -> Include Library -> Add .ZIP Library...`.  
Once the library has been added, go to `File -> Examples`. You should see an entry within the list named `martishin-mnist_inferencing`. Select it and click `nano_ble33_sense -> nano_ble33_sense_camera` to load the project.

Use the Arduino IDE to build and upload the project. Once it is running, you can see inference results using `Serial Monitor`:

```
Starting inferencing in 2 seconds...
Taking photo...
Predictions (DSP: 15 ms., Classification: 744 ms., Anomaly: 0 ms.): 
Predictions:
  0: 0.03906
  1: 0.03125
  2: 0.00391
  3: 0.00000
  4: 0.03125
  5: 0.02344
  6: 0.02734
  7: 0.83594
  8: 0.00391
  9: 0.00391
```

In this case, digit 7 was shown on the phone to the connected camera, the number after each digit is its score (confidence).
