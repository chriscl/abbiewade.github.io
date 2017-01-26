# Building a Smart Alarm Clock

You can use the [editor on GitHub](https://github.com/abbiewade/abbiewade.github.io/edit/master/smartalarmclock.md) to maintain and preview the content for your website in Markdown files. You can see the webpage [here](https://abbiewade.github.io/smartalarmclock). 

This tutorial makes the assumption that you have played around with the Arduino, Understand the basics of the program structure and have at a minimum used LEDs and buttons. 

## Just Your Basic Alarm Clock

To get started, we are going to build a simple alarm clock that is not connected to the internet. The code developed in this section will act as part of the framework for building an alarm clock connected to the internet further down. 

### Displaying Digits
The first part of the challenge of building a clock is to learn how to display numbers using a four digit 7-segment dispay. 

Describe how the 7-segment display works
Show the lettering of the display

To start off we are going to wire this display as you can see in the image below and make each of the four digits display the same number. 

First off we need to define our pin values in the code. The large advantage of doing so is to allow us to reuse our code later on. If we decide later to use a different set of pins to control this display, all we have to do is change one value rather than multiple throughout our code. 

```c++
#define A 11
#define B 7
#define C 4
#define D 2
#define E 1
#define F 10
#define G 5
#define DP 3

#define firstDigit 12
#define secondDigit 9 
#define thirdDigit 8 
#define fourthDigit 6 
```
Now that we have defined all our pins, we need to set them up so the Arduino knows that they are all output pins...

```c++
void setup() {
    pinMode(A, OUTPUT);
    pinMode(B, OUTPUT);
    pinMode(C, OUTPUT);
    pinMode(D, OUTPUT);
    pinMode(E, OUTPUT);
    pinMode(F, OUTPUT);
    pinMode(G, OUTPUT);
    pinMode(DP, OUTPUT);

    pinMode(firstDigit, OUTPUT);
    pinMode(secondDigit, OUTPUT);
    pinMode(thirdDigit, OUTPUT);
    pinMode(fourthDigit, OUTPUT);

    digitalWrite(firstDigit, HIGH);
    digitalWrite(secondDigit, HIGH);
    digitalWrite(thirdDigit, HIGH);
    digitalWrite(fourthDigit, HIGH);
}
```


```c++
void displayZero(){
    digitalWrite(A, LOW);
    digitalWrite(B, LOW);
    digitalWrite(C, LOW);
    digitalWrite(D, LOW);
    digitalWrite(E, LOW);
    digitalWrite(F, LOW);
    digitalWrite(G, HIGH);
    digitalWrite(DP, HIGH);
}
```

### Shift Registers 

```c++
put code here
```

### Real Time Clock Module

### Measuring Temperature

### Additional Functionalities
- timer
- alarm
- setting time manually 
- ...