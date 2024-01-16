# Lab Report 1: Knowing Your Instruments 
Eli Barrow & Isaac Stevens      
Jan. 10, 2024


## Summary of Lab
The project goal of this lab was to become comfortable with the lab equipment that we will be using all semester, we experimented with a power supply, oscilloscope, a function generator, and a Fluke DMM. We began the lab by determining the expected, maximum, and minimum values of resistors using the Fluke DMM. We then did the same type of experimenting with Capacitors to find the expected, maximum, and minimum capacitance of each capacitor we were given. Next, we began to work with the o-scope, function generator, and power supply to run various tests. By the end of the lab, I am certain that Isaac and I are more comfortable using the lab equipment now than before beginning the lab.

## Lab Schematics and Procedure
The Oscillo
![A test image](https://github.com/Feffle/BAE305-SP24-Lab1/blob/main/Lab%201%20Image.jpg)


## Lab Assignment Specific Items
***Question 1:***   

*Resistor Measurements*
| Color Code | Expected Resistance k&Omega; | MAX | MIN | Measured | Range |
|:---|:---:|:---:|:---:|:---:|---:|
|   Red-Black-Red-Gold     | 2   |2.1 | 1.9 | 1.966 | In Range |
| Brown-Red-Yellow-Gold    | 120 |126 | 114 | 120.20| In Range |
| Brown-Black-Ornage-Gold  | 10  |10.5| 9.5 | 9.9   | In Range |
| Orange-Orange-Green-Gold |3300 |3465 |3135 | 3500 | Out of Range |

*a.) If you subtract this value from the previously measured, do the resistors fall within their tolerance?*   
Considering the expected, minimum, and maximum values for these resistors we can see that all of them are in the expected range except for the 3300 k&Omega; resistor.  
      


***Question 2:***   

*Capacitor Measurements*
| Color| Type | Expected Capacitance pF; | MAX | MIN | Measured pF| Range |
|:---|:---:|:---:|:---:|:---:|:---:|---:|
|   blue   | ceramic      |10000      | 10000.25 | 9999.75 | 10200         | In Range |
| yellow   | ceramic      |1000       | 1100     | 900     | 1300          | In Range |
| black    | electrolytic | 100000000 | ---      | ---     | 97900000      | In Range |
| blue     | electrolytic | 100000000 |---       | ---     | 106000000     | Out of Range |

*a.) Do the instruments agree with the expected value?*  
Yes, they agree with the values for the most part, the values are a little off but that is because the values are so small and our Fluke DMM may not be able to accurately measure at that precision.

*b.) Does the polarity affect the measurement of the electrolytic capacitor?*    
Yes, it does affect the measurements of the electrolytic capacitors but not enough to alter our values.


***Question 3:***   

*Measurements of Power Supply*
| Expected Voltage (V) |  Actual Voltage (V)| 
|:---|:---:|
|1.50    |1.478 |
|7       | 6.95 |
|12      | 11.94 |
|3.3     | 3.396 |
|5       | 5.171 |
|12      | 12.01 |

*Discussion Question 1: Do the instruments agree with each other? Why?*  
Yes, they agree with one another but there is a little bit of error/resistance in the wires that we are using the measure the values with.

***Question 4:***   

   
*Working with the O-scope*

|  |  Frequency (kHz)|  Voltage (V)|
|:---|:---:|:---:|
|1   |1.913 |8.25|
|2     | 1.826 |9.28|
|3     | 1.738 |9.12|
|4     | 1.73 |6.2|

*a.) Discussion Question 2: Do the instruments agree? Why?*   
They do not agree because the multimeter measures the voltage in RMS so the values are off a bit, but for the frequency, it is very close to the measured values.

*Change the frequency and amplitude of the generated sinusoidal and observe what happens in the o-scope and Fluke DMM. What happens?*   

When you change either the frequency or amplitude the o-scope and Fluke DMM change according to the new values that you have altered to on the function generator. The instruments will react accordingly to the changes you apply to the function generator.


***Note: All code above this line was written by Eli Barrow***



This report includes text and also figures that I linked from my repository.
Like this:
![A test image](https://github.com/cjarro-uky/BAE305-SP24-Lab1/blob/main/20240110_100436.jpg)

Or perhaps a nicer smaller, centered image like this (using HTML):

<p align="center">
  <img src=https://github.com/cjarro-uky/BAE305-SP24-Lab1/blob/main/20240110_100436.jpg width=50%>
</p>

Also I can include math functions like this:

$$V(V) = I(A)*R(&Omega;)$$

$$P = I^2*R$$

Also I have to include code like this:

```c++
void recvWithEndMarker() {
    static byte ndx = 0;
    char endMarker = '\n';
    char rc;
    
    while (mySerial.available() > 0 && newData == false) {
        rc = mySerial.read();

        if (rc != endMarker) {
            receivedChars[ndx] = rc;
            ndx++;
            if (ndx >= numChars) {
                ndx = numChars - 1;
            }
        }
        else {
            receivedChars[ndx] = '\0'; // terminate the string
            ndx = 0;
            newData = true;
        }
    }
}
```
Also, I can make **bold** and *emphatic* statements and add tables like this:

| Variable | Value |
|:---:|---|
|   V      | 5 V   |
| R        | 1 k&Omega; |
| I        | 5 mA  |

Check out these links:

[Link for images](https://docs.github.com/en/communities/documenting-your-project-with-wikis/editing-wiki-content)

[Link for code](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/creating-and-highlighting-code-blocks)

[Link for tables](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/organizing-information-with-tables)
