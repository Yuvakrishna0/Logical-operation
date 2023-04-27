# Logical Operation

## AIM:

To Perform logical operation ( Xor,AND, 4:1 multiplexer) using Arduino UNO Controller.

## Software required:

Arduino IDE </br>
Proteous 

## PROCEDURE:

### Arduino IDE
Step1:Open the Arduino IDE </br>
Step2: Go to file and select new file option</br>
Step3:Type the program</br>
Step4:Go to file and select save option to save the program</br>
Step5:Go to sketch and select verify or compile options</br>
Step6:If no error Hex file will be generated in the temporary folder</br>
### Proteus 
Step7:Open the Proteus software</br>
Step8:Go to file select new design and click ok button</br>
Step9:Select component mode and click pick devices from the library</br>
Step10:Type the component name in the keyword to select the components and click ok button</br>
Step11:Design the circuit as per the diagram</br>
Step12:Double click the Arduino controller and upload the hex file generated by Arduino IDE</br>
Step13:Click start button and check the output</br>

## THEORY:
```
Logical operators give you another element of control over the flow of your program. Also known as Boolean operators, they can be very powerful when used inside the condition of an if statement or while loop. In this article we will discuss the three most common logical operators – AND, OR, and NOT.

The AND logical operator evaluates two variables and returns a true value only when both variables are true. It’s written with two ampersands (&&).
The OR operator is written with two vertical bars (||).

The vertical bar key is usually found above the Enter key on most keyboards. With the OR operator, if any of the variables are true, the outcome will be true.
The NOT operator is written with an exclamation point (!).

The NOT operator makes a true statement false, and a false statement true:

!true = false
!false = true


```

## PROGRAM:
```
int bs0 = 0;         // variable for reading the pushbutton status
int bs1 = 0;
int bs2 = 0;         // variable for reading the pushbutton status
int bs3 = 0;
int bs4 = 0;         // variable for reading the pushbutton status
int bs5 = 0;
void setup() {
  pinMode(13, OUTPUT);
  pinMode(0, INPUT);
  pinMode(1, INPUT);
  pinMode(2, INPUT);
  pinMode(3, INPUT);
  pinMode(4, INPUT);
  pinMode(5, INPUT);
}
void loop() {

  bs0 = digitalRead(0);
  bs1 = digitalRead(1);
  bs2 = digitalRead(2);
  bs3 = digitalRead(3);
  bs4 = digitalRead(4);
  bs5 = digitalRead(5);

  if (bs4 == 0 && bs5 == 0) 
  {
      digitalWrite(13, bs0);
  } 
  else if (bs4 == 0 && bs5 == 1) 
  {
    
    digitalWrite(13, bs1);
  }
   else if (bs4 == 1 && bs5 == 0) 
  {
    
    digitalWrite(13, bs2);
  }
   else   if (bs4 == 1 && bs5 == 1) 
  {
      digitalWrite(13, bs3);
  } 
}
```

## CIRCUIT DIAGRAM:
![output](./LOcd.png)

## OUTPUT:
![output](./LOout.png)
## RESULT:

Thus the logical operation was performed by Arduino UNO controller
