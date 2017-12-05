# Tutorial-FOR-BOSON
# Tracing car

---

Have you seen the delivery robot in the restaurant? They can serve customers along a fixed route. Robots reduce the work of service personnel, and can provide more efficient catering services. Do you want to have such a powerful robot?
Next, I will teach you to make a tracing car.

<div align=center>
<img src="https://github.com/joanna1122/Tutorial-FOR-BOSON/blob/master/image/tracing%20car/tracing%20car%203_%E7%9C%8B%E5%9B%BE%E7%8E%8B.jpg" height="450" width="500" >
</div>

> What kind of BOSON module do you need?

> What are the functions of these modules?

> How do these modules connect?

> How to achieve line inspection function?

> Car production process and testing

Let's work together to solve these problems!

---
## **What kind of BOSON module do you need?**

 - i10 Infrared Proximity Sensor  *2 
 - o9 Motor Module  *2
 - Motor  *2
 - micro：bit & expansion board for Boson  *1
 - cble  *4
 
## **What are the functions of these modules?**

**i10 Infrared Proximity Sensor**
<div align=center>
<img src="https://github.com/joanna1122/Tutorial-FOR-BOSON/blob/master/image/tracing%20car/Infrared%20Proximity%20Sensor%202.png" height="200" width="300" >
</div>
Infrared Proximity Sensor is an input module that can recognizes colors. It is a smart guy.Infrared Sensor can be used in distinguishing surfaces of black and white. However, colors of the surfaces need to be pre-recognized by the sensor upon first using. 

**o9 Motor Module & Motor**
<div align=center>
<img src="https://github.com/joanna1122/Tutorial-FOR-BOSON/blob/master/image/tracing%20car/motor%202.png" height="200" width="500" >
</div>
The motor and motor module are used together. They belong to the output module, can drive the wheel together to rotate. The motor module has four gears that can be selected by toggle switch.
## **How do these modules connect?**

Find the required BOSON module, connect the module according to the following connection diagram.
<div align=center>
<img src="https://github.com/joanna1122/Tutorial-FOR-BOSON/blob/master/image/tracing%20car/connection%202.png" height="400" width="700" >
</div>
## **How to achieve line inspection function?**

### **1.Set i10 Infrared Proximity Sensor**
The setup only need to be done once for the same combination of surfaces. Please follow the instruction below to setup the sensor. 

 1. Record the first color: 
  a)	Long press the bottom to enter recording mode (LED slowly blinks). 
b)	Face the sensor to the target surface and click the button to record the first color (LED turns off) 
 2. Record the second color:
 a)	Short press the bottom to enter recording mode again (LED fast blinks).
b)	Face the sensor to the target surface and click the button to record the second color (LED turns off) 
 3. To test if the colors are successfully recorded, face the sensor to
>first color: the sensor will send out a logic "1” signal, while the LED stays on;

>second color: the sensor will send out a logic "0” signal, while the LED stays off; 

### **2.Program and upload**

Please visit https://makecode.microbit.org，follow the procedure below to program.

<div align=center>
<img src="https://github.com/joanna1122/Tutorial-FOR-BOSON/blob/master/image/tracing%20car/makecode%E7%95%8C%E9%9D%A2.png" height="400" width="720" >
</div>

The final program as shown below.
<div align=center>
<img src="https://github.com/joanna1122/Tutorial-FOR-BOSON/blob/master/image/tracing%20car/%E5%AE%8C%E6%95%B4%E7%A8%8B%E5%BA%8F.png" height="400" width="750" >
</div>
 > **How to program?**

 1. Delete unnecessary modules, drag the module into the module area.
 <div align=center>
 <img src="https://github.com/joanna1122/Tutorial-FOR-BOSON/blob/master/image/tracing%20car/%E5%88%A0%E9%99%A4%E6%A8%A1%E5%9D%97.png" height="450" width="580" >
</div>
 2. Drag into the logic module
 <div align=center>
  <img src="https://github.com/joanna1122/Tutorial-FOR-BOSON/blob/master/image/tracing%20car/%E6%8B%96%E5%85%A5%E9%80%BB%E8%BE%91%E6%A8%A1%E5%9D%97.png" height="450" width="580" >
  </div>
 Logic module is editable. Click the Settings button, you can see there will be another dialog box appears.There will appear "else" and "else if" two modules, drag "else if" into the middle of "if" and "else", where you need to drag in two else ifs.
 <div align=center>
   <img src="https://github.com/joanna1122/Tutorial-FOR-BOSON/blob/master/image/tracing%20car/%E9%80%BB%E8%BE%91%E6%A8%A1%E5%9D%97%E7%BC%96%E8%BE%91.png" height="450" width="580" >
  </div> 
*Click the Settings button and the dialog will disappear.*

 3. Drag into another logical module "And".
 <div align=center>
 <img src="https://github.com/joanna1122/Tutorial-FOR-BOSON/blob/master/image/tracing%20car/%E6%8B%96%E5%85%A5and%E6%A8%A1%E5%9D%97.png" height="450" width="580" >
 </div>
 The shape of "AND" module can be changed.Right-click the module, you can switch the shape of the module,inline or external.
 <div align=center>
 <img src="https://github.com/joanna1122/Tutorial-FOR-BOSON/blob/master/image/tracing%20car/and%E6%A8%A1%E5%9D%97%E7%BC%96%E8%BE%91.png" height="450" width="580" >
 </div>

 4. Drag into the other two logic blocks "=",on both ports of the logic block "AND".
 <div align=center>
 <img src="https://github.com/joanna1122/Tutorial-FOR-BOSON/blob/master/image/tracing%20car/%E6%8B%96%E5%85%A5%E5%88%A4%E6%96%AD%E6%A8%A1%E5%9D%97.png" height="450" width="700" >
 </div>
 5. Find "Pins" in the "Advance" pull-down menu and drag the "digital read pin P0" on the corresponding location.
 <div align=center>
 <img src="https://github.com/joanna1122/Tutorial-FOR-BOSON/blob/master/image/tracing%20car/%E6%8B%96%E5%85%A5%E5%BC%95%E8%84%9A%E6%A8%A1%E5%9D%97.png" height="450" width="700" >
 </div>
 "P0" is the default pin number, you need to modify according to the actual use whitch pin Infrared Proximity Sensor connect.
In this project, we use two pins, P0 and P1.You need to change one of the pins to P1.
<div align=center>
 <img src="https://github.com/joanna1122/Tutorial-FOR-BOSON/blob/master/image/tracing%20car/%E4%BF%AE%E6%94%B9%E5%BC%95%E8%84%9A.png" height="380" width="500" >
</div>
The state of P1 and P0 exist 1 and 0 state, corresponding to the setting of Infrared Proximity Sensor. Click the number to make the change.
<div align=center>
 <img src="https://github.com/joanna1122/Tutorial-FOR-BOSON/blob/master/image/tracing%20car/%E4%BF%AE%E6%94%B91%E5%92%8C0.png" height="380" width="500" >
</div>

 6. When an action is independent, we can create a function that makes it easy to call throughout the big program. We need to define the way the car turns to the left. Click on fuctinon, in the dialog box, enter "Left".
 <div align=center>
 <img src="https://github.com/joanna1122/Tutorial-FOR-BOSON/blob/master/image/tracing%20car/%E8%87%AA%E5%AE%9A%E4%B9%89function.png" height="400" width="580" >
 <img src="https://github.com/joanna1122/Tutorial-FOR-BOSON/blob/master/image/tracing%20car/left.png" height="200" width="580" >
 </div>
 There are two modules that we need.
 Drag the two modules to the corresponding locations.
 <div align=center>
  <img src="https://github.com/joanna1122/Tutorial-FOR-BOSON/blob/master/image/tracing%20car/%E5%BB%BA%E7%AB%8Bleft%E4%B9%8B%E5%90%8E.png" height="500" width="650" >
</div>
 7. Define how car to turn left. Drag the module to the corresponding location and modify the pins and numbers.
 <div align=center>
   <img src="https://github.com/joanna1122/Tutorial-FOR-BOSON/blob/master/image/tracing%20car/%E5%90%91%E5%B7%A6%E8%BF%90%E5%8A%A8.png" height="500" width="650" >
 </div>
 *Note： "P8" controls the right wheel.When the right wheel and the left wheel does not turn ,the car turn left. "500" control speed, it can be adjusted according to the actual situation.If the angle to the left is too large, please speed down.*

 8. Repeat STEP 3 ~ STEP 7, complete the program.

 9. Download the code to your computer.
 <div align=center>
    <img src="https://github.com/joanna1122/Tutorial-FOR-BOSON/blob/master/image/tracing%20car/%E7%A8%8B%E5%BA%8F%E4%B8%8B%E8%BD%BD.png" height="80" width="600" >
 </div>
 Find the code, dragged into the micro: bit disk.
 <div align=center>
  <img src="https://github.com/joanna1122/Tutorial-FOR-BOSON/blob/master/image/tracing%20car/%E7%A8%8B%E5%BA%8F%E6%8B%96%E5%85%A5.png" height="250" width="650" >
 </div>
*Note: The micro: bit disk will appear only if the cable is properly connected to the micro: bit and the computer's USB port.*

## **Car production process and testing**
Congratulations, you have completed the program section.Let's make a car.

 1.Find a piece of cardboard or plastic plate, as the car's chassis. Fix the module on this board.
 <div align=center>
   <img src="https://github.com/joanna1122/Tutorial-FOR-BOSON/blob/master/image/tracing%20car/tracing%20car%202.jpg" height="600" width="580" >
 </div>
 *Note:*
 
 - Place two Infrared Proximity Sensors on the left and right of the front.
 - Battery power will affect the speed of the car.
 
2.Make the body with the material in our life.
<div align=center>
   <img src="https://github.com/joanna1122/Tutorial-FOR-BOSON/blob/master/image/tracing%20car/tracing%20car%203.jpg" height="600" width="580" >
</div>
<div align=center>
**The tracing car is finished！**
 </div>
