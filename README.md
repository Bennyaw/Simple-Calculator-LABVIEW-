# Simple Calculator using LABVIEW
This repository is about creating a simple calculator using LABVIEW. Operators that I did here is just simple add, subtract, multiply and divide and equal. The reason for me doing this calculator exercise is to get more familiar to LABVIEW.The code is available in PDF above.

![](https://github.com/Bennyaw/Simple-Calculator-LABVIEW-/blob/master/images/calculator%20interface.png)

### Using Queue for getting every inputs
There will be various approaches to complete this program. The appraoch I took here was using Queue. 
Using Queue's ***FIFO***(First-In-First-Out) property I can ensure that every button pressed is properly recoreded and transfers into processing loop. 

### Program states and concepts
<img src="https://github.com/Bennyaw/Simple-Calculator-LABVIEW-/blob/master/images/state%20diagram.png">
This calculator consists of 3 states, which is **Initialize**, **Display Value**, **Display Final Value**. 

- **Initialize**            - Clear all screen and empty all data arrays. If done action then move to next state, **Display Value**.

- **Display Value**         - Display digits to perform operation. Move to next state, **Display Final Value**, if equal button is pressed

- **Display Final Value**   - Take in the number array and operator array to perform math calculations and display on screen. Starts to store new digits for next calculation is number button is pressed. Here, the state goes back to **Display Value**, else if the OFF button is pressed, the state comes to end state. 

<img src="https://github.com/Bennyaw/Simple-Calculator-LABVIEW-/blob/master/images/math%20operation%20concept.png" width="500" height="250" />
The figure example above shows the operation of seperating the number and operators into respective array. Then, this 2 arrays will be passed into the `Calculated Result VI ` and perform the calculations in one shot.

## Result
This is the result of performing the math operation in the figure above.

<img src="https://github.com/Bennyaw/Simple-Calculator-LABVIEW-/blob/master/images/calculator%20result.png">

## Future upgrades
1. Replace the lastest the operator if the operator button is pressed in a row. Ex, '+' is pressed immediately after '-', then '+' is added into the array instead of '-'.
2. Add in a *Delete* button
3. Add in a *Clear All* button
4. Add in *sqr root*, *reciprocal*, *percent*, *+/-* functions

