# Wemos D1-based HAN-module for Kamstrup Omnipower smart meter

__This will probably only work for Radius customers in the greater Copenhagen area__

Here's what we do:
- Connect to Wi-Fi and MQTT, 
- Read the output of Kamstrup Omnipower HAN-slot with a Wemos D1 Mini (ESP8266-based MCU), 
- Decrypt the incoming data using the two keys you got from Radius (Copenhagen-area DSO), 
- Publish the data to a MQTT broker of your choice.

__Note: You need to write to (kundesupport@radiuselnet.dk)[mailto:kundesupport@radiuselnet.dk] to get your decryption keys__

### Hookup guide:

1. Modify the code with your WiFi, MQTT, and Key information
2. Upload modified sketch to Wemos
2. Connect: Wemos Ground pin <-> Kamstrup HAN slot top left pin
2. Connect: Wemos D5 pin <-> Kamstrup HAN slot top middle pin
3. Power the Wemos through USB charger
4. Subscripe to your MQTT broker and do what ever you want with it


### History:
Adapted from [Claustn](https://github.com/Claustn/esp8266-kamstrup-mqtt) to use SoftwareSerial instead of a second UART, to make it work with my Wemos D1 Mini.
Claustn adapted his code from [Asbjoern](https://github.com/Asbjoern/Kamstrup-Radius-Interface/) whose repo has many more features than this little thing.

