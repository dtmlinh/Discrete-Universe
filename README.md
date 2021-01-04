# Energy Conservation in Discrete Universe Simulation

## Project Description

This model is an agent-based universe in which each agent reacts to each other according to the Newton's law of universal gravitation. Everything is discrete, including time. 

The questions of interest are: 
- How does the initial velocity of one planet affect its trajectory around the sun? How about mass? Location?
- By calculating the gravitational potential (also known as Newtonian potential) energy and the kinetic energy, we will investigate whether the total energy can be conserved in a discrete universe. 

## Theoretical Framework

First, because of the complexity of simulating the entire solar system, only the sun and one planet are included in this model. The sun is set to be initially located at the origin. This origin position (x<sub>p</sub>, y<sub>p</sub>), the initial velocities (x<sub>v</sub>, y<sub>v</sub>), and the mass of the planet can be manipulated in the model. Each agent will interact with each other according to Newton's law of universal gravitation:

F = G * (m<sub>1</sub> * m<sub>2</sub>) / r<sup>2</sup> 

where:

F is the force between the masses,

G is the gravitational constant,

m<sub>1</sub> is the first mass,

m<sub>2</sub> is the second mass, and 

r is the distance between the centers of the masses.

In this equation, r is calculated as √((x<sub>p1</sub> - x<sub>p2</sub>)<sup>2</sup> + (y<sub>p1</sub> - y<sub>p2</sub>)<sup>2</sup>)

After that, we can apply the Newton's law of motion: F = m * a to derive the acceleration vector of each sun. Since we have the initial velocity (v<sub>t</sub>), we can obtain the velocity (v<sub>0</sub>) after each unit of time (potentially every second) using the equation v<sub>t</sub> = v<sub>0</sub> + a<sub>t</sub>. The suns will move accordingly to their velocity vectors (x<sub>v</sub>, y<sub>v</sub>) and arrive at new positions. Since our universe is discreet, we can only report the positions of all the suns discreetly at each given time.
At each given time and velocity, we can calculate the total energy of each sun using the gravitational potential energy formula and kinetic energy formula: 

U = -m * ∑ [G * (M / r)]

E<sub>k</sub> =  1/2 * m * v<sup>2</sup>

The total energy of the entire universe is then calculated and presented in a graph.

## Usage

By selecting the initial values for: location (distance of the planet from the sun), mass (in this simulation, we will assume the sun and the planet have equal masses), and velocity (initial velocity of the planet), we can look at how the planet would orbit around the sun. 

![](demo.gif)
