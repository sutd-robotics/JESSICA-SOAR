# JESSICA-SOAR
SOAR to the floor

Documentation for incoming team, taking over the JESSICA robot arm.

JESSICA is a robot arm that can automatically serve coffee upon activation. 
We plan to add a manual function, where users can control JESSICA with an EMG myosensor armband.



## Simple communication from Arduino Uno to Raspberry Pi:
### Code in Arduino
```
void setup(){
  Serial.begin(9600);
}

void loop(){
  Serial.println("Hello World!");   
  delay(2000);
}
```
### Python code in RPi:
```
ser = serial.Serial('/dev/ttyUSB0', 9600)
while 1: 
    if(ser.in_waiting >0):
        line = ser.readline()
        print(line)
```


### Useful guides:

Connecting RPi and Uno:
https://www.instructables.com/id/Connect-Your-Raspberry-Pi-and-Arduino-Uno/
https://classes.engineering.wustl.edu/ese205/core/index.php?title=Serial_Communication_between_Raspberry_Pi_%26_Arduino

Myosensor explained:
https://medium.com/@leex5202/an-unofficial-introductory-tutorial-to-myoware-muscle-sensor-development-kit-e2169948e63