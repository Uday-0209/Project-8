# Contour-Following-Based-Glueing-Cobot
The main object of this project is to automate the gluing process in manufacturing industry. Here the cobot with the help vision technology and glue dispensor, Glue the contour of the object.

The things required for the project;
1) Cobot.
2) Python knowledge, OpenCV, Pointcloud, Meshing.
3) RoboDk software.
4) Knowledge of cobot controller.
5) Glue dispensor, TOF intel camera.

The complete working methodology:
![cobot work model](https://github.com/user-attachments/assets/7bc34b63-3c7e-423a-a623-2fc59e5a00b7)

The picture of the cobot setup:
![cobot](https://github.com/user-attachments/assets/ad4a4902-ccfd-42e4-8a5c-8e772a730776)

The point cloud data of the 3D model:
![contour](https://github.com/user-attachments/assets/cef72dcc-de78-41bc-a1fa-43aac07f14de)

The Simulation of the cobot in RoboDk:
![robodk](https://github.com/user-attachments/assets/c3615214-0e32-45e1-8ae3-3590399612e9)

The methodology followed to achieve the project:

1) The Intel RealSense camera is used to acquire the point cloud data of the model.
2) The images need to be processed to acquire the contour data. The depth data of the contour is separated from the point cloud data.
3) The 3D coordinates are converted to joint coordinates using inverse kinematics.
4) The glue dispenser is triggered once the joint coordinates are sent to the robot via RoboDK.
5) RoboDK is used to simulate the robot movement and ensure smooth connectivity with the cobot.
6) RoboDK acts as a bridge between the program, the cobot, and the glue dispenser.
7) Once the program is triggered, the contour point cloud is collected, and the 3D coordinates are converted to joint coordinates. These are then sent to the cobot, and once the cobot is triggered, the glue dispenser is enabled and starts dispensing. Once the path is covered, the dispenser is disabled.
