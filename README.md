<p>Controls Final Project</p>
## Translational Inverted Pendulum
## MECA 482 Controls Theory and Design
## California State University, Chico


<br/>

Ahmad Alherz
Jorge Carranza Perez
Luis Hernandez
Cristian Rodriguez

<p align="center">
  

<br/>
<br/>

### Project Description



<br/>
<br/>
<br/>
<p align="center">
Testing setup
<br/>
The power supplies were used to power the Peltiers(x3) and the 80mm x 80mm Fans (x2)
<br/>
MATLAB and an Arduino were used to supply PWM signal to Fans for Fan Speed
<img src="Full_Setup.jpg" width="800" />

<br/>
<br/>
<p align="center">
Device Under Test (DUT)
</p>
<p align="center">
<img src="ClamShell.jpg" width="35%" />

<br/>
<br/>
<p align="center">
Parts list (not capturing clam shell)
</p>
<p align="center">
<img src="Parts.png" width="50%" />

<br/>
<br/>
<p align="center">
Performing Test
</p>
<p align="center">
<img src="Testing.jpg" width="50%" />

<br/>
<br/>
<p align="center">
DMM with K-Type Thermocouple Displaying Temperature
</p>
<p align="center">
<img src="Temperature.jpg" width="50%" />

<br/>
<br/>
<p align="center">
<br/>
The input step command can be ignored on this plot, because this was not a closed loop test
<br/>
Test initial Temperature was 24 degrees Centigrade - it took ~2 minutes to achieve 4 degrees Centigrade
<br/>
Sampling was performed using a stopwatch at 10 second intervals
</p>
<p align="center">
<img src="TEC_Testing.png" width="800" />
<p align="center">
Results Plotted with exponential curve fit
<p align="center">

<br/>
<br/>
<br/>
<br/>
<br/>

<p align="center">
The trend line equation was then taken from above collected data and converted to s domain
</p>
<p align="center">
<img src="Equations.png" width="50%" />
<p align="center">

<br/>
<br/>


### MATLAB Script used to analyze Transfer Function Response
```

%MECA 482 - Thermal Response
%12/4/2019

clc; close all; clear all;

%% raw data from testing, sampled at .1Hz
temp = [22.2 21.7 20.2 17.9 15.4 13.2 11.1 8.9 7.2 6 4.5 3.2 2.7];

time = [10 20 30 40 50 60 70 80 90 100 110 120 130];

%% Transfer Function and step response
s = tf('s');
%init temperature from exp trend line at t = 0
t = 0;
To = 34.701*exp(-.018*t);
K = -34.701;            % DC gain
tau = .018^-1;
TF = K/(tau*s+1);        % model transfer function
[y,t] = step(TF,130);    % model step response

%% plot generation
plot(time,temp,'rx',t,y+To,'b')
xlabel('time (sec)')
ylabel('temperature (degrees C)')
title('SLAC Reservoir Clamshell Temperature Step Response')
legend('experimental data','model','Location','NorthEast')

```

<br/>
<br/>
<br/>

<p align="center">
The results from the above MATLAB script plotted
</p>
<p align="center">
<img src="MATLAB_Script_Results.jpg" width="75%" />
<p align="center">








<!--
```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

```
- this is a test
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/MechaEngBryan/MECA482-Temp_Control_Project/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
-->
