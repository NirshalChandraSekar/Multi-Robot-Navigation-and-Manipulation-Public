THIS REPO IS PART OF A PROJECT FOR THE COURSE CSCI5551 - INTRODUCTION TO INTELLIGENT ROBOTICS SYSTEMS, AT THE UNIVERSITY OF MINNESOTA.

THIS PROJECT BUILDS UPON THE EXISTING OFFICIAL KINEVAL STENCIL PACKAGE FROM THE UNIVERSITY OF MICHIGAN - LINK: https://github.com/autorob/kineval-stencil
________________________________________________________________________________________________________________________________________________________

INPUT and OUTPUT:
-----------------
The environment contains two MR2 robots, operating in a set environment with known obstacles. The task involves two cubes, red and blue, placed randomly. The challenge is to guide both robots simultaneously to pick up their corresponding cubes and return to the starting point avoiding obstacles.

METHOD:
--------
We adopted the RRT connect path planning algorithm for planning two non-intersecting paths for the robots. The idea is to construct the path for the first robot and plan the second path using a spatial offset from the first path. For manipulation, both the robots use inverse kinematics.

OBJECTS/MAPS/ROBOTS:
--------------------
The environment is enclosed by a square boundary, with three sphere obstacles with defined radius and location. The environment includes two cubes (red and blue), and two MR2 robots.

EXPERIMENTS:
------------
Learning from trials: We tested our algorithm 100 times, achieving a success rate of 93 percent. The 7 percent failure occurred when limited space hindered the second robot’s path planning. 

SIMULATION:
-----------
To run the environment, run "python -m http.server" in the project directory. Then open "http://localhost:8000/home.html" on your local browser.

Navigate the toolbar on the top right side of the screen to view different functions that the robot can perform.

TO VIEW THE MULTI ROBOT NAVIGATION AND MANIPULATION SIMULATION:

run "python -m http.server" in the project directory

And,
run http://localhost:8000/home.html?world=worlds/world_final_project.js on your local browser to access the environment that we modified.

Check "persist_mobile_manipulate_traversal" under "Mobile Manipulate" tool in the toolbar.

Each time you refresh the window, the robots spawns in a random position, and performs the navigation and manipulation tasks simultaneously.

DEMO:
-------

https://github.com/NirshalNiru/Multi-Robot-Navigation-and-Manipulation/assets/157089936/7b52a4fa-b994-427b-9865-35942a2ae612

https://github.com/NirshalNiru/Multi-Robot-Navigation-and-Manipulation/assets/157089936/c2f4d52f-aa99-4072-9e7e-ad4949795297






