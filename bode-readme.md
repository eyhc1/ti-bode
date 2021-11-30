# Bode Plotter 1.0.0
The TI program for plotting magnitude and phase plot with given transfer function H(s)

## Programs
Bode - Main program
GetTransferVal - Sub additional program

### Bode
First enter your numerator and denominator of H(S) separately, in terms of S.
**You have to enter your transfer function in terms of S, or it will give
error**. For example, for the transfer function H(S) = S/(S+1), enter S first, 
press `enter`, then S+1 (as shown)  
![Initial entry](img/Capture%201.png)  
then press `enter` again to go to the menu  
![menu](img/Capture%2011.png)    

You can plot your transfer function from here by selecting `4:Plot magnitude`
for magnitude plot or `5:Plot Phase` for phase plot, either of them will
calculate magnitude or phase then show the plot. You will need to press `enter`
after finishing inspecting the plot. Note that the last plot the program shown
will be preserved and can be seen again from the graphing option in the
calculator after exiting the program

#### Modify transfer function
In the menu you may change numerator or denominator of H(S) by selecting either
`1:Change Numerator` or `2:Change Denominator`, respectively.

#### Change bounds
you may adjust the x-axis (frequency bounds) by selecting `4: Set Frequency 
Bound` option, where it will ask for the low and upper bounds and steps.
For each of value it will be a power of 10. So if you want to have frequencies
from 10 to 10^6 just enter 0 for lower and 6 for upper bounds.  
![set bounds](img/Capture%208.png)  
Step is how much values the program will calculate for each decade. The larger
value it is given the more data it will calculate, making the plot finer but
takes more time to calculate, and less value will be faster but less date.
If you do not wish to enter any of the lower/upper bounds or steps, simply
enter 0 then press `enter` to set it default values, which is 10 to 10^4 with
step of 10  
![set step](img/Capture%207.png)  

#### Access plot data after quitting the program
After done with program, you can plot either the magnitude or the phase of H(S)
by turning on `stat plot` in the calculator, with Plot 1 being the magnitude
plot and Plot 2 being the phase plot. All the data used in the plot are saved
in three lists L3, L4, and L5. L3 is the frequencies (in Hz) in power of 10. L4
is the data for magnitude plots in decibels. L5 is the data for phase plot in
degrees

### GetTransferVal
This helper program is named `HVAL` in the calculator. It will calculate any
H(jw) **after** you have saved H(S) by running the main `BODE` program. simply
enter a value for w and will give you the log magnitude and phase of it. If you
wish to access the values again they are saved in list L6, where first entry is
value of jw, second entry is H(jw) decibel value, and the third entry is the
phase of H(jw) in degrees. Note that ignore the +0i in the magnitude and phase
entries in the list. and only taking the real values of them (since all values
were stored as complex)
