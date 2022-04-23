# Robot-Project
## Teamwork and Collaboration
This project was worked on by me, Mohammed Barakat, and Marwan Gadara.
Marwan mainly worked on making the user inputs and sensor parts of the code, while i worked on the rest. We worked together on the Robot moving towards the goal while avoiding obstacles together.

## User inputs and Expected outputs
For this program to function, a user input is required to define the starting coordinates of the robot and the goal coordinates. Also the amount of randomly postioned obstacles are required. We use `int(input))` in the code to allow the user to input said data
The expected output would be a graphic of a 20x20 grid showing the Robot png, goal marker and the randomly generated obstacles.

## Software Versiona and Dependencies
To run the code, 
- It is required to have installed Python3.6 or any previous version of Python
- To install RoboticsToolBox via [Peter Corke's RoboticsToolBox Repisotory](https://github.com/petercorke/robotics-toolbox-python)
It is important that the imports in the existing code to be correctly written or copied to ensure the code functions

## Code Explaination
After the appropriate imports have been written, we use `int(input))` to allow the user the input the data required such as the coordinates and the number of obstacles. After it we use `def` to create the code necessory to make the robot move. This function is used to tidy up the code and make the final while loop easier to read. Another `def` function is used to create the code necessory for the object manuavering, again this is to tidy up the code and make the final loop easier to read. After it we give the robot its form using the Robot.png as an icon and giving it a scale. We then define its animation, control and starting position under `veh`.
![Robot.png](/Robot.png)

We then use LandmarkMap to generate the randomly positioned followed by the RangeBearingSensor that mesures the distance and angle of every obstacle to the robot.
Finally, we make a `while(run)` loop, initiallizing the code by a `run=True` to make sure the while loop will always function at the begining. Inside the while loop we call in the def functions we previously wrote and making it so the loop will stop once the first functions returns a False.
Finally we have `plt.pause(1000)` delay so the simulation can be watched and not close immediatly.
To simplify what the code does, here is a flowchartof the code.

![flowchart](/flowchart.png).

## Results
Once the code has compiled and has ran, a window will open showing the robot, obstacles and goal.

![Simulation](/Simulation.png). 

The robot will start moving towards the goal,avoiding all obstacles in the way, until it reaches the goal and stops moving.
.
![Simulation Done](/Simulation Complete.png)


## Limitations and Future Work
Some of the issues we encoutered were mainly due to the obstacle maneuvering:
- Robot would spin around an obstacle until it eventually leaves it and continues to the goal
- If a random obstacle happened to be placed right next to the robot's initial position
In the future we hope to iron out these issues and work on a significantly more robust obstacle maneuvering using Python and RoboticsToolBox

