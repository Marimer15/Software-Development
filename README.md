# Software-Development

#define LS 2 // Left sensor 
## Line 3 explanation: This line is for defining the left sensor will be on port 2.
#define RS 3 // Right sensor  
## Line 5 explanation: This line is for defining the right sensor will be on port 3.
#define LM1 5 // Left motor M1a
## Line 7 explanation: This line is for defining the left motor will be on port 5, for high pulse.
#define LM2 4 // Left motor M2b     	
## Line 9 explanation: This line is for defining the left motor will be on port 4, for low pulse.
#define RM1 7 // Right motor M1a 
## Line 11 explanation: This line is for defining the right motor will be on port 7, for high pulse.
#define RM2 6 // Right motor M2b	
## Line 13 explanation: This line is for defining the right motor will be on port 6, for low pulse.
void setup()
## Line 15 explanation: Function to start program.
{
## Line 17 explanation: Code starts to run here.
pinMode(LS, INPUT);
## Line 19 explanation: Left sensor is input.
pinMode(RS, INPUT);
## Line 21 explanation: Right sensor is input.
pinMode(LM1, OUTPUT);
## Line 23 explanation: Left motor on port 5 is output.
pinMode(LM2, OUTPUT);
## Line 25 explanation: Left motor on port 4 is output.
pinMode(RM1, OUTPUT);
## Line 27 explanation: Right motor on port 7 is output.
pinMode(RM2, OUTPUT);
## Line 29 explanation: Right motor on port 6 is output.
}
## Line 31 explanation: Closing this part of the code.
void loop()
## Line 33 explanation: Function to start program and repeat the code.
{
## Line 35 explanation: Code starts to run here.
if(digitalRead(LS) && digitalRead(RS)) // Not on the black line, robot moves forward
## Line 37 explanation: If statement, lets you make something happen or not, depending if a given condition is true or not. The digitalRead function reads whether the voltage is high or low. Two dash lines (//) means there’s a comment starting after them explain the function of that if statement. These symbols together (&&) mean that there is an AND statement.
{
## Line 39 explanation: Separation, here we start using digitalWrite function which tells the pin to be high or low.
digitalWrite(LM1, HIGH);
## Line 41 explanation: Here the left motor pin is on High.
digitalWrite(LM2, LOW);
## Line 43 explanation: Here the left motor pin is on Low.
digitalWrite(RM1, HIGH);
## Line 45 explanation: Here the right motor pin is on High.
digitalWrite(RM2, LOW);
## Line 47 explanation: Here the right motor pin is on Low.
}
## Line 49 explanation: Close, if statement.  
if(digitalRead(LS) && !(digitalRead(RS))) // Right sensor on black line, robot turns left by rotating the left motor forward and right motor back
## Line 51 explanation: If statement, lets you make something happen or not, depending if a given condition is true or not. The digitalRead function reads whether the voltage is high or low. Two dash lines (//) means there’s a comment starting after them explain the function of that if statement. When he exclamation point (!) symbol is next to a statement then that means that this part of the statement is not true. For example, in this case the digitalRead on the Right Sensor will be detecting the black line statement. These symbols together (&&) mean that there is an AND statement.
{
## Line 53 explanation: Separation, here we start using digitalWrite function which tells the pin to be high or low.
digitalWrite(LM1, HIGH);
## Line 55 explanation: Here the left motor pin is on High.
digitalWrite(LM2, LOW);
## Line 57 explanation: Here the left motor pin is on Low.
digitalWrite(RM1, LOW);
## Line 59 explanation: Here the right motor pin is on Low.
digitalWrite(RM2, HIGH);
## Line 61 explanation: Here the right motor pin is on High.
}
## Line 63 explanation: Close, if statement.
if(!(digitalRead(LS)) && digitalRead(RS)) // Left sensor on black line, robot turns right by rotating the right motor forward and left motor back
## Line 65 explanation:	If statement, lets you make something happen or not, depending if a given condition is true or not. The digitalRead function reads whether the voltage is high or low. Two dash lines (//) means there’s a comment starting after them explain the function of that if statement. When he exclamation point (!) symbol is next to a statement then that means that this part of statement is not true. For example, in this case the digitalRead on the Left Sensor will be detecting the black line statement. These symbols together (&&) mean that there is an AND statement.
{
## Line 67 explanation: Separation, here we start using digitalWrite function which tells the pin to be high or low.
digitalWrite(LM1, LOW);
## Line 69 explanation: Here the left motor pin is on Low.
digitalWrite(LM2, HIGH);
## Line 71 explanation: Here the left motor pin is on High.
digitalWrite(RM1, HIGH);
## Line 73 explanation: Here the right motor pin is on High.
digitalWrite(RM2, LOW);
## Line 75 explanation: Here the right motor pin is on Low.
}
## Line 77 explanation: Close, if statement.
if(!(digitalRead(LS)) && !(digitalRead(RS))) // Black line on both sensors, both motors stop
## Line 79 explanation: If statement, lets you make something happen or not, depending if a given condition is true or not.	The digitalRead function reads whether the voltage is high or low. Two dash lines (//) means there’s a comment starting after them explain the function of that if statement.	When he exclamation point (!) symbol is next to a statement then that means that this part of the statement is not true. For example, in this case the digitalRead on the Right and Left sensor will be detecting the black line.	These symbols together (&&) mean that there is an AND statement.
{
## Line 81 explanation: Separation, here we start using digitalWrite function which tells the pin to be high or low.
digitalWrite(LM1, LOW);
## Line 83 explanation: Here the left motor pin is on Low.
digitalWrite(LM2, LOW);
## Line 85 explanation: Here the left motor pin is on Low.
digitalWrite(RM1, LOW);
## Line 87 explanation: Here the right motor pin is on Low.
digitalWrite(RM2, LOW);
## Line 89 explanation: Here the right motor pin is on Low.
}
## Line 91 explanation: Close, if statement.
}
## Line 93 explanation: End code.
