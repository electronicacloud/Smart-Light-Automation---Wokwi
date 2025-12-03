# Smart-Light-Automation - Wokwi simulation

This project simulates an automatic lighting system using an LDR (Light Dependent Resistor) module and an Arduino Uno.
The LED automatically turns ON in darkness and OFF in brightness.

Link to runthe simulation in Wokwi:

https://wokwi.com/projects/449302949419568129

<img width="584" height="439" alt="image" src="https://github.com/user-attachments/assets/cee89783-0389-42f6-9435-2450e35478f8" />

A 220 ohm resistor is used to limit the current drawn by the LED.

Aruduino output=5V

V_LED ≈ 2V (for red LED)

Desired safe current = ~10–15 mA 

R = V / I = 3V / 0.015A = 200Ω

A standard resistor value close to 200Ω is 220Ω


CODE USED:

int ldrvalue;

const int threshold=500;

int ldrpin=A0;

int ledpin=9;

void setup() {

  pinMode(ledpin, OUTPUT);
  
}

void loop() {

  ldrvalue=analogRead(ldrpin);

  if(ldrvalue>threshold){
  
    digitalWrite(ledpin,HIGH);}
    
    else{
    
    digitalWrite(ledpin, LOW);
    
  }
  
  delay(500);
  
}


The threshold value is based on the Photoresistor Sensor Reference Table provided in the Wokwi documentation.

According to the reference table:

Dark conditions produce high analog values 

Bright conditions produce low analog values 

PROJECT FILE:
Smart Light Automation.zip
