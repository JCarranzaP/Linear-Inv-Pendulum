<p align="center">Controls Final Project</p>
<p align="center">Translational Inverted Pendulum</p>
<p align="center">MECA 482 Controls Theory and Design</p>
<p align="center">California State University, Chico</p>

<p align="center"><img src="CSUCHICO-Seal-Color.png" width="250" />
<br/>

<p align="center">Ahmad Alherz</p>
<p align="center">Jorge Carranza Perez</p>
<p align="center">Luis Hernandez</p>
<p align="center">Cristian Rodriguez</p>

<br/>
<br/>

<p align="center">December 25, 2019</p>

<br/>
<br/>

<p align="center">Introduction</p>

The goal of the control theory in this project is to describe and predict the underactuated and non-linear motion of a pendulum, and control it to balance upright. What can be expected from this project is a mathematical representation of the physical model that can be run on a computer software system such as matlab or simulink in order to virtually test the systems response to varying conditions. Finally, we will be adding a PID controller in order to balance the pendulum in an upright position. This step will be facilitated through the use of the matlab function “pid”.
<br/>

<p align="center"><img src="model.jpg" width="250" />
<p align="center">Figure 1. Simplified model of Inverted Pendulum</p>

<br/>

The first step in deriving the mathematical equations of motion is to draw out the free body diagram. Assuming the rod is massless, we can neglect its Inertial effects from the system and thus from the free body diagram.

<br/>

<p align="center"><img src="fbd.jpg" width="250" />
<p align="center">Figure 2. (a) Free body diagram of isolated pendulum (b) Free body diagram of sliding cart attached to pendulum.</p>

<br/>

The approach taken in this paper used to derive the motions of equations is that of kinematics. A more elegant approach, according to research on the topic would have been to use a Lagrange method, which uses the kinetic energy and internal energy of the system components to reduce the mechanical system to a mathematical representation. This approach, however more elegant, is more involved mathematically and the group decided to use a more familiar method. 

<br/>

Starting the interpretation of the free body diagrams from Figure 2, Newton’s second law is applied in order to balance the forces.

<p align="center"><img src="1.jpg" width="250" />
<p align="center"><img src="2.jpg" width="250" />
<p align="center"><img src="3.jpg" width="250" />
<p align="center"><img src="4.jpg" width="250" />
<p align="center"><img src="5.jpg" width="250" />
<p align="center"><img src="6.jpg" width="250" />
<p align="center"><img src="7.jpg" width="250" />  
<p align="center"><img src="8.jpg" width="250" />
<p align="center"><img src="9.jpg" width="250" /> 
<p align="center"><img src="10.jpg" width="250" />
<p align="center"><img src="11.jpg" width="250" />
<p align="center"><img src="12.jpg" width="250" />
<p align="center"><img src="13.jpg" width="250" />
<p align="center"><img src="14.jpg" width="250" />
<p align="center"><img src="15.jpg" width="250" />
<p align="center"><img src="16.jpg" width="250" />  
  
  
  
  
  
  
  
  
  
  
<p align="center">Modeling</p>

<p align="center">Controller Design and Simulation</p>

<p align="center">



























