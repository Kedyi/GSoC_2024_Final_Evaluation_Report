<p align="center">
  <img src="https://summerofcode.withgoogle.com/assets/media/logo.svg"/>
</p>

# Google Summer of Code 2024 with LibreCube - Open Source Space and Earth Exploration   
- Project: Rover Control
- Organization: LibreCube - Open Source Space and Earth Technologies
- Mentors: Artur Scholz, Husseinat Etti-Balogun
- Email: komaldubey561@gmail.com
- LinkedIn: https://www.linkedin.com/in/kedyi/
- GitLab: https://gitlab.com/Kedyi
- Repository: https://gitlab.com/librecube/prototypes/python-rover-control

## Project Description
### Title: Rover Control - A User-Friendly Platform for Rover Movements

The Rover Control project aims to provide a user-centric platform enabling easy control of rovers in both simulated and real-world environments. 
This project focuses on creating an integrated system for controlling a rover, featuring a range of components for visualization and control in both 2D and 3D environments. 
The project includes the development of multiple viewers and controllers, as well as a server for managing communication between them.

## Preface
Entering this project, the goal was to bridge simulation environments with real-world rover operations. Leveraging my programming background, 
I embraced the challenge, which has been immensely rewarding. The learning curve included managing diverse technologies such as Python, ROS2, FastAPI, Gazebo, and Webots, 
all while ensuring seamless communication between simulation and control interfaces. 
My passion for space exploration further motivated me to contribute to LibreCube, dedicated to making space technologies accessible.

## Components and Development Phases
 ### 1. Turtle Application (Viewer_2D A)
 - Description: Developed a 2D turtle graphics application to showcase rover movement in a simplified 2D space.
 - Purpose: To provide a basic simulation of rover movements and test control functionalities in a straightforward environment.
 - Achievements: Successfully demonstrated basic movement commands and interactions in 2D space.

## 2. Pygame Zero Viewer (Viewer_2D B)
Contributor: Artur Scholz
 - Description: Created an additional viewer using Pygame Zero, a simplified framework for creating games and graphical applications.
 - Purpose: To offer an alternative visualization of the rover’s movements, leveraging Pygame Zero’s easy-to-use interface for 2D graphics.
 - Achievements: Implemented a functional viewer with a user-friendly interface for demonstrating rover movements.

## 3. GUI Executor Controller (Controller A)
 - Description: Built an initial controller using GUI-Executor, where users select actions, input speeds, and run commands to control the rover’s movements.
 - Purpose: To provide a graphical interface for controlling the rover, though it resulted in slower interactions.
 - Challenges: The GUI-Executor approach introduced some delays in responsiveness, leading to a decision to develop an alternative controller.

## 4. Pygame Controller (Controller B)
 - Description: Developed a second controller using Pygame to address the performance issues with GUI-Executor. In this controller we used arrow key to control the rover and +/- to controller the speed.
This made the controller more easy to handle and faster while sending commands.
 - Purpose: To offer a more responsive and interactive control system for the rover.
 - Achievements: Created a more efficient controller with improved performance and real-time responsiveness for rover commands.

## 5. Server Simulation (Server Sim)
 - Description: Implemented a server to facilitate communication between the controllers (both 2D and 3D) and the viewers.
 - Purpose: To manage and route commands from the controllers to the appropriate viewer, ensuring seamless integration between components.
 - Achievements: Established a robust connection framework for handling interactions between different system components using FastAPI.

## 6. 3D Viewer Transition (Viewer 3D)
 - Description: Initially developed a 3D viewer using Gazebo but later transitioned to Webots for its lightweight and user-friendly controller capabilities.
 - Purpose: To provide an advanced simulation environment for rover movements in 3D.
 - Achievements: Successfully shifted to Webots, achieving a more efficient and manageable 3D simulation environment.

## Controllers and Viewers:
   |Controllers and Viewers|Images|
   |--------------------------- | ------|
   |GUI Executor Controller (Controller A)|![Screenshot 2024-08-26 085315](https://github.com/user-attachments/assets/390c0c09-f33f-4732-9294-e0b140365830)|
   |Pygame Controller (Controller B) |![conr](https://github.com/user-attachments/assets/909ae670-ce89-4d05-945c-699c362c9635)|
   |Server Simulation (Server Sim)|![Screenshot 2024-08-26 085426](https://github.com/user-attachments/assets/d7c07d8b-e7b3-4e24-970d-a116fbe32137)|
   |Turtle Application (Viewer_2D A)|![viewer_A](https://github.com/user-attachments/assets/28a9169d-9dfe-4f21-a4df-0d6f971c054b)|
   |Pygame Zero Viewer (Viewer_2D B)|![Screenshot 2024-08-26 085652](https://github.com/user-attachments/assets/85efc3e8-b773-4834-803e-f1ba07570446)|
   |3D Viewer Transition (Viewer 3D)|![Screenshot (2416)](https://github.com/user-attachments/assets/45abb414-1d2e-447f-829b-4abf57713b71)|
   

## Detailed Overview
### Viewers:
The project features three main viewers: The Turtle Graphics Viewer provides a basic 2D representation using geometric shapes to visualize rover movements.
The Pygame Zero Viewer builds upon this with a more polished and interactive 2D interface, offering enhanced control and visual feedback. 
For 3D visualization, we initially used Gazebo but transitioned to Webots for its lightweight performance and user-friendly controller. 
The Webots 3D Viewer incorporates Mars terrain, emulating the rugged Martian landscape for realistic rover simulation. This terrain adaptation, inspired by the Sojourner project, 
adds depth and realism to the 3D environment.
### Controllers:
The project includes two distinct controllers designed for managing rover movements. 
The first controller, built using GUI-Executor, allows users to select actions, set speeds, and execute commands. 
While functional, its interface was somewhat sluggish due to its reliance on sequential command inputs. 
To address this, a second controller was developed using Pygame. This controller features a more responsive and interactive GUI, 
where users can easily send commands such as forward, backward, and turn left or right. 
The Pygame controller displays real-time feedback, including visual indicators for command status, and includes speed adjustment controls with a more intuitive user experience.
### Server:
The server plays a crucial role in our project by acting as the intermediary between the various components—controllers and viewers. 
Its primary function is to handle communication and synchronization between these components, ensuring that commands from the controllers are accurately 
transmitted and reflected in the viewers. This setup allows for a modular and scalable architecture, where the server manages the data flow and coordination, 
enabling seamless integration of different viewers (2D and 3D) and controllers. By using a server, we can maintain a clear separation of concerns, 
allowing each component to focus on its specific tasks while the server ensures that all parts of the system work together harmoniously.

## Future Scope
In the future, we will focus on refining the interface of controller_b to make it more suitable for real-world rover control via the PUS protocol. 
This will involve enhancing its user experience and ensuring it meets the necessary standards for real-time control. 
Additionally, we will work on aligning our code with industry standards to improve maintainability, performance, and reliability.

## Conclusion
This project successfully developed a comprehensive rover control system, starting with a 2D turtle application and expanding to 3D visualization with Webots. 
We created multiple controllers, initially using gui-executor and later switching to Pygame for better performance. 
The server facilitated seamless communication between controllers and viewers. The use of Mars terrain in Webots enhanced the simulation realism. 
Future efforts will focus on refining controller_b for real-world rover control using the PUS protocol and aligning the code with industry standards. 
This journey has significantly advanced my technical skills and highlighted the value of adaptability in system development.

## Acknowledgements
I would like to express my gratitude to Google and the LibreCube organization for the incredible opportunity to work on this innovative and challenging project. 
Special thanks to my mentors, Artur and Husseinat, for their invaluable guidance and support throughout this journey. 
A heartfelt shoutout to Artur for his consistently timely feedback, even during late hours. 
I also appreciate the community events organized by LibreCube, which allowed me to connect with other developers through engaging icebreakers and online games. 
This experience has deepened my respect for open-source technologies, and 
I look forward to continuing my involvement with both the LibreCube and Google Developer communities.
