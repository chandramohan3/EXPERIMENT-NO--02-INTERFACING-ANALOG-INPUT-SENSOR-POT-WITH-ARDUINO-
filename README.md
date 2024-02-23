 ###  DATE: 23/02/2024

###  NAME: CHANDRAMOHAN S
###  ROLL NO : 212221223002
###  DEPARTMENT: INFORMATION TECHNOLOGY

**AIM**:  To interface a Analog  input (angular displacement sensor POT) and scale the values up on change in the input.


**COMPONENTS REQUIRED:**
1.	10 KΩPOT
2.	1 KΩ resistor 
3.	Arduino Uno 
4.	USB Interfacing cable 
5.	Connecting wires 
6.	LED of choice 
**


**THEORY**: 

**Analog signals:**

Analog signals – directly measurable quantities in terms of some other quantity.
Examples:
1. Thermometer – mercury height rises as temperature rises
2. Car Speedometer – Needle moves farther right as you accelerate
3. Stereo – Volume increases as you turn the knob
Reason for conversion of analog to digital quantity is that as the controller or any microprocessor works with digital signals in the form of 0 and 1s, in order to make the signal compatible  most of the analog signals are converted into its equivalent digital level signals using an analog to digital converter .
Quantizing - breaking down analog value is a set of finite states
Encoding - assigning a digital word or number to each state and matching it to the input signal
 There are two ways to best improve accuracy of A/D conversion:
Increasing the resolution which improves the accuracy in measuring the amplitude of the analog signal.
Increasing the sampling rate which increases the maximum frequency that can be measured.
General specifications of analog sensor
	1. Range
	2. Accuracy
	3.Linearity
	4.Compatiblity
	5. signal conversion capability

**Potentiometer**
A potentiometer, informally a pot, is a three-terminal resistor with a sliding or rotating contact that forms an adjustable voltage divider. If only two terminals are used, one end and the wiper, it acts as a variable resistor or rheostat.
Potentiometers are commonly used to control electrical devices such as volume controls on audio equipment. Potentiometers operated by a mechanism can be used as position transducers, for example, in a joystick. Potentiometers are rarely used to directly control significant power (more than a watt), since the power dissipated in the potentiometer would be comparable to the power in the controlled load


CIRCUIT DIAGRAM

figure 1:
![Screenshot 2024-02-23 154854](https://github.com/vasanthkumarch/EXPERIMENT-NO--02-INTERFACING-ANALOG-INPUT-SENSOR-POT-WITH-ARDUINO-/assets/142579775/64fec311-6031-4172-84af-14a6c26336b6)

**FIGURE -01
**

**PROCEDURE:**

1.	Connect the circuit as per the circuit diagram 
2.	Connect the board to your computer via the USB cable.
3.	If needed, install the drivers.
4.	Launch the Arduino IDE.
5.	Select your board (If you the board is arduino uno, select accordingly).
6.	Select your serial port, accordingly ( E.g. COM5 )
7.	Open the file of the program  and verify the error , clear if any errors that are existing 
8.	Upload the program and check for the physical working. 
9.	Ensure safety before powering up the device 



**PROGRAM** 
``` C++
int pot;
int led=7;

void setup()
{
  pinMode(led,OUTPUT);
  Serial.begin(9600);
}

void loop()
{
  pot=analogRead(A0);
  //rial.print("Values=");
  Serial.println(pot);
  if (pot>900)
  {  
 
  digitalWrite(led, HIGH);
  delay(500);
  digitalWrite(led, LOW);
  delay(500); 
  }
  else
  {
    digitalWrite(led,LOW);
    delay(500);
  }
}
```
 









**
**Simulation output:** 

![Screenshot 2024-02-23 154555](https://github.com/vasanthkumarch/EXPERIMENT-NO--02-INTERFACING-ANALOG-INPUT-SENSOR-POT-WITH-ARDUINO-/assets/142579775/60274823-affa-4241-9f91-d9ba80fff774)

**

BEFORE STIMULATION

![Screenshot 2024-02-23 160217](https://github.com/vasanthkumarch/EXPERIMENT-NO--02-INTERFACING-ANALOG-INPUT-SENSOR-POT-WITH-ARDUINO-/assets/142579775/7c1425c5-eb21-4970-a533-3a7111373073)

AFTER STIMULATION

![Screenshot 2024-02-23 160229](https://github.com/vasanthkumarch/EXPERIMENT-NO--02-INTERFACING-ANALOG-INPUT-SENSOR-POT-WITH-ARDUINO-/assets/142579775/338badf8-8028-4c8e-866e-51dac4962a9a)










**RESULT: ** Arduino uno analog input functioning is learned and interfaced with digital input switch .
