[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/rXX1_Uiw)
## Project 00
### NeXTCS
### Period: 09
## Name0: Mia Shi
## Name1: Isabel Zheng
---

This project will be completed in phases. The first phase will be to work on this document. Use github-flavoured markdown. (For more markdown help [click here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) or [here](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) )

All projects will require the following:
- Researching new forces to implement.
- Method for each new force, returning a `PVector`  -- similar to `getGravity` and `getSpring` (using whatever parameters are necessary).
- A distinct demonstration for each individual force (including gravity and the spring force).
- A visual menu at the top providing information about which simulation is currently active and indicating whether movement is on or off.
- The ability to toggle movement on/off
- The ability to toggle bouncing on/off
- The user should be able to switch _between_ simluations using the number keys as follows:
  - `1`: Gravity
  - `2`: Spring Force
  - `3`: Drag
  - `4`: Frictional Force
  - `5`: Combination


## Phase 0: Force Selection, Analysis & Plan
---------- 

#### Custom Force: Frictional Force

### Forumla
What is the formula for your force? Including descriptions/definitions for the symbols. (You may include a picture of the formula if it is not easily typed.)

![alt text](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcShVEKU0hPyU1Ogn7_5JpGfjqgNOYr8B1FIMQ&s)

### Custom Force
- What information that is already present in the `Orb` or `OrbNode` classes does this force use?
  - N/A

- Does this force require any new constants, if so what are they and what values will you try initially?
  - μ: Coefficient of friction (kinetic & static)
- Does this force require any new information to be added to the `Orb` class? If so, what is it and what data type will you use?
  - N: Normal Force (mgcos(theta))

- Does this force interact with other `Orbs`, or is it applied based on the environment?
  - Yes (collision)

- In order to calculate this force, do you need to perform extra intermediary calculations? If so, what?
  - nawh

--- 

### Simulation 1: Gravity
Describe how you will attempt to simulate orbital motion.
![alt text](https://i.ytimg.com/vi/N__3zLT8zU0/maxresdefault.jpg)

With a fixed orb in the center acting as the Earth, we can simulate orbital motion with the F = G(m1)(m2)/(r^2) equation. If necessary, we can also 
simulate centripetal force as shown above. The orbs will move in a "circular" shape around the center orb and based on the size and distance from the center, 
it will move differently. 
--- 

### Simulation 2: Spring
Describe what your spring simulation will look like. Explain how it will be setup, and how it should behave while running.

The spring simulation would look similar to our work from previous labs. Using the F = kx (AB hat) formula, we can model the spring forces between moving orbs. 
For the setup, there will be a couple orbs on screen, each moving, and the lines between the centers of orbs will stretch. 

--- 

### Simulation 3: Drag
Describe what your drag simulation will look like. Explain how it will be setup, and how it should behave while running.

Similar to the Spring simulation, this section will also reference our labs. We will use borders to represent distance and compare the speed of certain orbs. 
Using the drag formula coded previously, we can also control the drag coefficient. Our setup consists of a couple orbs, falling down the bottom of the screen 
in a predefined speed. Additionally, we will color-code the background to help compare the distance each orb has traveled. 

--- 

### Simulation 4: Custom force
Describe what your Custom force simulation will look like. Explain how it will be setup, and how it should behave while running.

****We are hoping to simulate frictional force. Frictional force requires the usage of mg and possibly, cos(theta). Moving alongside the surfaces of the wall, the frictional
force would be forced to act against the smooth flow of movement, pushing back. For this, we may need to create a wall in the background to control the cordinates. ****
--- 

### Simulation 5: Combination (grav-ing)
Describe what your combination simulation will look like. Explain how it will be setup, and how it should behave while running.

Using the previous functions, we hope to find a way to merge spring force and gravity. When there is a perfect no acceleration position, gravity (mg) may be equal to kx.

