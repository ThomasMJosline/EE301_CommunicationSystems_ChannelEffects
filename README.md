# EE301_CommunicationSystems_ChannelEffects
Demonstrating the effect of channel on transmission of pulse signals


Group members:
Thomas M Josline
Anshul Mandhar

Here we are using an Arduino Uno to generate pulse signal. The pulse signal generated here is the UART signal generated by the Arduino.
The code used for generating the signal:

```cpp

void setup() {
  // Initialize the serial communication at a baud rate of 9600
  Serial.begin(9600);
}

void loop() {
  // Send the character 'o' over UART
  Serial.write('o');
  delay(1000); // Wait for 1 second before sending the next 'o'
}
```

Here the UART signal corresponding to letter 'o' is generated. The bit stream correspoding to letter 'o' is:
```
01001111
```

The bits are sent in a serial manner with a '0' at the start indicating the start of the bit stream contunued with the least significant bit being sent first and move towards the most significant bit.

The signal come out through the Tx pin of the arduino.

The setup used was:

![setup](https://github.com/ThomasMJosline/EE301_CommunicationSystems_ChannelEffects/assets/84652232/1e2ecb31-1780-4857-a6c7-58d8962ae21d)


The channel used in the transmission is the red spool of wire in the image. 


The resultant signal is analysed in an oscilloscope.

![results](https://github.com/ThomasMJosline/EE301_CommunicationSystems_ChannelEffects/assets/84652232/34e81e53-090f-4299-b7dc-2e4cbe8625f6)

The purple waveform is of the signal which is being directly taken from the arduino. The yellow waveform shows the output from the channel, ie. the spool of red wire.
Here we are able to observe the effect of channel on the pusle signal.
