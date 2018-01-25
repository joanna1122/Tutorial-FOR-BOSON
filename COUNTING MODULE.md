# COUNTING MODULE

------
    
The counting module is a 3-bit digital LED that can be used to display the voltage of the signal through the circuit, can also be used to count. We will explain how to use it below.

## COUNTING MODULE

（图1）
Two modes and four switch positions of the counting module.

**1. Count Mode**.  
Count Mode is at the left position of the switch, there are two levels: up and down. In this mode, when pressing RESET button, the number will be back to the initial value.

**2. Read mode**.  
Read mode is at the right position of the switch, there are two levels: value and volts.


## WHICH BOSON MODULE YOU NEED  

|   Module  | Quantity  |  Function  |
| -------- | -----:  | :----:  |
| Button      | 2（i2b、i2f） |   Press the button to record and clear the data     |
| Counting Module        |   1（f7）   |   Display with reading and counting functions  |
| Main Board        |    1（m2）    |  No programming, can be used directly after connected  |
| Rotation        |    1（i1）    |  In the circuit can continuously control the level of the output signal |

##COUNT MODE

**How to connect**

（图）
***

**There are two counting functions in Count mode:**
> * **Count-Up**
（GIF）
Connect as shown in the figure,connect the battery box, turn on the power.
And set the counting module to Count-Up, counting from 0. Each time you press the input button, the display number automatically +1, the maximum value can be 999. When you press the reset button, the display number returns to the initial value of 0.

> * **Count-Down**
（GIF）
Connect as shown in the figure,connect the battery box, turn on the power.
And set the counting module to Count-Down, counting from 999. Each time you press the input button, the number is displayed automatically -1, the minimum value can be 0. When you press the reset button, the number returns to the initial value of 999.

##READ MODE
**How to connect**
（图）



**There are two counting functions in Read mode:**
> * **Read-Value**

（GIF）
Connect as shown in the figure,connect the battery box, turn on the power.
And set the counting module to Read-Value(at the left position of the switch),the Rotation continuously controls the analog voltage outputs from 0 to 999.

> * **Read-Volts**

（GIF）
Connect as shown in the figure,connect the battery box,turn on the power.
And set the counting module to Read-Volts(at the right position of the switch),the Rotation continuously controls the voltage output from 0 to 5.5.

