# Google Summer of Code 2018 Ideas

23 Jan 2018

## General information on applications

This is the list of ideas for the Google Summer of Code 2018, if you are interested in any of the ideas listed below or you think you can propose something interesting to improve RoboComp we encourage you to apply. 

* It is important to first familiarize with the software ([https://github.com/robocomp/robocomp](https://github.com/robocomp/robocomp)). 
* You can go through the available tutorials and direct your questions to the mailing list or gitter chat (listed below, also see contact section). 
* Please read all the information posted in this page before applying. 
* Make sure you are familiar with the required skills for the idea. 
* Since several of the mentioned RoboComp tools and components are not explained here to keep this list short, we encourage everyone to check the RoboComp documentation linked below. 
* Mentors and backup mentors are listed right after the idea explanation. All mentors contact info is at the end of the page. Contact them directly for specific questions on the idea.

Robocomp installation and tutorials: [https://robocomp.readthedocs.io/en/highlyunstable/](https://robocomp.readthedocs.io/en/highlyunstable/)

**Where can I start and what to include on my application?**

You are encouraged to go through these steps for a better understanding and follow-up of your application:

1.  Download and install RoboComp: [https://github.com/robocomp/robocomp/blob/master/README.md](https://github.com/robocomp/robocomp/blob/master/README.md).
2.  Follow the tutorials: https://github.com/robocomp/robocomp/blob/master/doc/README.md.
3.  Once you are familiar with RoboComp and the components and tools involved in the particular idea you want to contribute to, try to understand how these components/tools work and, if possible, their design.
4.  Participate in the mailing list asking any question you might have.
5.  Create a schedule with the milestones you plan to follow during the GSoC 2017 program.
6.  **Send the schedule and any code you might have written along with your CV and other application materials to the mentor of your idea and the backup mentor.**

For general questions about RoboComp please use: The [developers list](https://groups.google.com/forum/?hl=es#!forum/robocomp-dev) and the [gitter chat](https://gitter.im/robocomp/home).

NOTE:  If you send this by email make sure to also submit your application through the official GSoC website otherwise you will not be considered for the programme.

## IDEAS LIST for GSoC 2018

### 1\. RCManager extended functionalities: a tool to deploy and monitor large sets of components. 

 
Currently RoboComp has a tool to deploy components that is being improved through several GSoC editions. It’s name is RCManager and is used on a daily basis by all the people that use RoboComp to program robots. Since this tool is crucial to the software development process and since robot software is all the time increasing its complexity as a large-scale distributed system, we need to improve this tool as much as we can. 
* The first extension is to make the tool access remote RoboComp installations to create a list of potential components to be added to the deployment set.
* The second extension tackles the need to group sets of components into higher order entities, so visualization is simplified.
* A third extension is to include the capability to probe the edges in the graph of components so a pop-up window would show in real time the traffic moving through it. When connections between components use publish/subscribe modality the probing is easy, but when communication is done using the pull/request modality things get more complicated.

Where to start and what to include in my application for this idea?

1. Run a test with the RCManager tool and understand how it works
2. Have a look at the tool’s code and check for how to make modifications so a deployment file can be automatically generated in a painless way through the tool
3. Provide some example of a small modification or improvement in the tool.


Technologies involved: Qt5, C++, Python, Zeroc ICE  
Mentor: Esteban Martinena, Pablo Bustos  
Backup mentor: Luis J. Manso  

### 2\. RCIS: improving RoboComp simulator with contact physics

RCIS is RoboComp’s robot simulator and a very  valuable tool that has been developed for the last years to suit our needs. However, as robots get more and more complex more advanced functions are needed in RCIS. This project’s goal is the extension of RCIS with a new set of functionalities dealing with contact physics. Without incurring in a full fledged physics engine in this work, the student will use the existing FCL collision detection library already included in RCIS to program different ways to control the behavior of simulated objects, robots and humans. The skill needed for this project include C++, OpenSceneGraph and knowledge of basic physics.

RCIS is RoboComp’s robot simulator and a very  valuable tool that has been developed for the last years to suit our needs. However, as robots get more and more complex more advanced functions are needed in RCIS. This project’s goal is the extension of RCIS with a new set of functionalities dealing with contact physics. Without incurring in a full fledged physics engine in this work, the student will use the existing FCL collision detection library already included in RCIS to program different ways to control the behavior of simulated objects, robots and humans. The skill needed for this project include C++, OpenSceneGraph and knowledge of basic physics.

Technologies involved:  C++, Python, Qt, OPenSceneGraph  
Mentors: Pablo Bustos, Marco A. Gutiérrez  
Backup mentor: Ramon Cintas  

### 3\. RCIS: improving RoboComp simulator with transmission delays

RCIS is RoboComp’s robotics simulator. It is built using the OpenSceneGraph 3D engine as the visual renderer. Over the years we have tuned RCIS to suit or needs for robot software development. Despite the mature state of the software we need to add more functionalities to cope with the increasing complexity of our social robots. One of these new functions is the simulation of different kind of transmission delays that occur when the real robot is running. Ignoring these delay may even cause that a nice simulated result is almost useless in a real-world execution. The goal of this project is to design, model and include a set of realistic delay into RCIS so simulations get closer to real-world results. These delays will include transmission, hardware and computational factors.

Technologies involved: C++, Python, Qt5  
Mentors: Luis Manso, Pilar Bachiller  
Backup mentor: Pablo Bustos  

### 4\. Emotion recognition component for Learnbot 

Learnbot is a small low-cost robot designed to develop computational thinking in kids of age 10 and above. Learnbot is programmed using a block language specifically designed for it. Through this language, kids program robot behaviors in an easy way by specificating what the robot has to to do whenever a given situation occurs. The last version of Learnbot has been equipped with a display that provides it with the possibility to show “emotions”. This way, kids can program not only motor behaviors, but also emotional reactions. To improve the HRI functions in Learnbot and extend the situations that make it to exhibit different emotional behaviours, we want to add new skills in the robot that allow it to recognize emotions in people such as happy, sad, angry, scared, … These new skills will be developed as a Robocomp component in charge of detecting people faces, recognizing basic emotions on them and providing its results to other components demanding this kind of information.

For your info here is a talk about the first version of the learnbot: [https://www.youtube.com/watch?v=3IRNXUDAXns](https://www.youtube.com/watch?v=3IRNXUDAXns)

Technologies involved: C++, Python, Qt5, OpenCV3  
Mentors: Pilar Bachiller, Iván Barbecho  
Backup mentor: Marco A. Gutiérrez  

### 5\. Improving the Human-centered Robot Navigation Agent

Currently, RoboComp provides robots with the capability to behave in a socially acceptable manner. Particularly, the strategy followed in our Social Navigation Agent is based on the definition of regions where navigation is either discouraged or forbidden (personal spaces). These regions are related with the Proxemics, which defines spaces that humans mutually respects during an interaction. The navigation architecture combines the Probabilistic Road Map and the Rapidly-exploring Random Tree path planners and an adaptation of the elastic band algorithm to include the social behaviour. All of them are part of different RoboComp components. Considering the complexity of this task, the use of the current version of the social navigation agent is restricted, since it does not analyse, for instance, the human intentions during the robot navigation (do the human want to interact with the robot?) or the size of  personal space depending of context (personal space should be different in a corridor than in a big room). 

The task at hand here would be to integrate improvements in the existing RoboComp Social Navigation Agent. In a future version of this agent, more complex situations will be taking into account, such a s human intention analysis and/or adaptive personal spaces. A typical case of use would be that of a group of humans walking in different environments while the robot performs a task. All these simulations would be made using RCIS (RoboComp InnerModel Simulator)

Technologies involved: C++, Python, Qt5  
Mentors: Pedro Nuñez, Luis Manso  
Backup mentor: Pablo Bustos  

### 6\. Generation of new use cases, tutorials and reference information for RoboComp

During several years of RoboComp diffusion we have realized that it takes too much time for new users to understand the internals of the framework and its workflows. Creating tutorials of small use cases for RoboComp can help everyone to better understand all the tools involved and to facilitate the collaboration with our project in a much faster way. The student selected for this idea will have to acquire a fairly deep knowledge of the tool to select and create a set of key use cases that will help to explain and disseminate all the features available in RoboComp. These use cases must be documented and integrated in the RoboComp website and in the manual, so they are available to everyone and even to future GSoC students!

Technologies involved: C++, Python, Qt5, Jekyll (for static web generation) and other online generation tools.  
Mentors: Marco A. Gutiérrez, Esteban Martinena  
Backup mentor: Luis J. Manso  

### 7\. Gazebo-RoboComp connection

RoboComp currently has its own simulation tool RCIS (RoboComp Innermodel Simulator), however it does not incorporate physics simulation. Sometimes robot models are already available under Gazebo, which is a more common simulation environment. Having gazebo as an option for simulations with RoboComp will help grow the possibilities our framework can offer to developers. The idea is to connect RoboComp and Gazebo in a similar way ROS is. This way any simulation with RoboComp can be tested on both simulators (Gazebo or RCIS).

Where to start and what to include in my application?

1. Download robocomp: https://github.com/robocomp/robocomp
2. Get familiarized with the framework through the docs: https://github.com/robocomp/robocomp/tree/master/doc
3. Run a test with the RCIS tool and understand how it works
4. Download and run Gazebo: http://gazebosim.org/
5. Run it and find ways to connect Gazebo to robocomp components through the ros interface.

Technologies involved: Gazebo, C++, Robotics simulation, ROS  
Mentors: Marco A. Gutiérrez, Ramón Cintas  
Backup mentor: Luis J. Manso  

### 8\. Javascript support in RoboComp component model

An interesting diversion from current robotics technologies based on C++ and Python is the use of Javascript as the language to code some highly concurrent components. NodeJS component code generation was added during GSoC 2017. This was an innovative task as Zeroc ICE (the main supported middleware in RoboComp) just added support for javascript interfaces. Although components development was achieved some effort is still needed to stabilize the code and fully integrate this solution into the RoboComp component model. The RoboComp component generator will be extended to include Javascript running in a server as a new target language for components. 

Technologies involved: Javascript, ZeroC ICE, Python, Cog(python module)  
Mentor: Marco A. Gutiérrez, Nicolás González  
Backup mentor: Pablo Bustos  

### 9\. Learnbot Simulation with RCIS

Learnbot is the new open robot supported by robocomp designed for learning. Although it is already in its second (or more) design iteration there is no support for this robot in the official robocomp simulation tool (RCIS). This is a key feature for the robot as it helps people test their algorithm in a simulated environment prior to real world testing while also giving the opportunity to developers to play with the robot without the need of the possessing the hardware. 

In this idea the RCIS tool will be extended and different interfaces will be created so the LearnBot can be simulated. The behavior and shape should mimic the real hardware. Documentation and tutorials with different use case scenarios would be produced for future users and developers.

For your info here is a talk about the first version of the learnbot: [https://www.youtube.com/watch?v=3IRNXUDAXns](https://www.youtube.com/watch?v=3IRNXUDAXns)

Technologies involved: C++, 3D design, Zeroc ICE  
Mentor: Marco A. Gutiérrez, Pilar Bachiller  
Backup mentor: Iván Barecho  

### 10\. Learnblock (Learnbot programming language) extension for collaborative robotics

LearnBlock is the programing tool designed for easy usage of the Learnbot robot. It is meant to be used by students and to help them learn new concepts by the usage of robotics programming. This idea involves the extension of the Learnblock programming tool to manage collaborative robotics between learnbots. The student will have to develop a system that enables Learnbot to communicate between and offer this option through the learnblock tool to the end user. Finally a use case example of these collaborative robotics tool will have to be developed and tutorials produced for future users and developers of the platform.

For more info about learnblock check: [https://github.com/ibarbech/learnbot/blob/master/doc/learnblock.md](https://github.com/ibarbech/learnbot/blob/master/doc/learnblock.md), regarding larnbot you can have a look at our talk about the first version of the learnbot: [https://www.youtube.com/watch?v=3IRNXUDAXns](https://www.youtube.com/watch?v=3IRNXUDAXns).

Technologies involved: C++, Python, Qt5  
Mentor: Marco A. Gutiérrez, Iván Barbecho  
Backup mentor: Pilar Bachiller  

### 11\. Adding locomotion skills to a human avatar

Real-time control of three-dimensional avatars is an important problem in the context of robotics.  Currently, RoboComp provides a basic avatar which is used not only for simulations in RCIS (RoboComp Innermodel Simulator), but also for different navigation and human-robot interaction algorithms (fakehumanComp). RoboComp Human avatar  implements basic locomotion skills, it moves from a keyboard and a joystick, but it doesn’t generate realistic walking motions.  The task at hand here would be to integrate improvements in the existing RoboComp human avatar. In a future version of this avatar, more complex and realistic walking motions should be provide. Besides, social skills should be also taken into account in the final version of the component. All these simulations would be made using RCIS (RoboComp InnerModel Simulator)

Technologies involved: C++, Python  
Mentors: Pedro Núñez, Pablo Bustos  
Backup mentor: Luis J. Manso  

### 12\. Integrating MORSE Human-robot interaction simulator with RoboComp

MORSE is a generic simulator for academic robotics (see [https://www.openrobots.org/morse/doc/stable/what_is_morse.html](https://www.openrobots.org/morse/doc/stable/what_is_morse.html)). Currently simulations in RoboComp are made using RCIS (RoboComp InnerModel Simulator), which has several limitations related to Human-Robot interactions. MORSE does not make any assumption on the external architecture using it, thus, the idea is to integrate this simulator as an additional tool for RoboComp. As MORSE authors say in their webpage, “it is developed using python and also supports a simple socket-based protocol for easy integration in other languages/toolbox”, features that will facilitate the proposed integration. Besides, MORSE developers provide complete bindings for Python which make it a natural way to integrate with RoboComp’s Python code generation tool.

Technologies involved: C++, Python  
Mentor: Pablo Bustos, Luis J. Manso  
Backup Mentor: Pedro Núñez  

### 13\. Improvements in Robocomp code generator: robocompdsl

RoboComp’s code generator, robocompdsl, is one of the core elements of RoboComp. It is used to generate and automatically modify the software components that users develop. The code generated using robocompdsl is separated in two kinds of files: ‘specific’ and ‘generic’ files. The names of those files which are supposed to be written by the user end with ‘specific’, whereas those responsible aren’t end with ‘generic’. This separation allows modifying the specification of components and re-generate their code without overwriting user’s code. Over the years, it has been endowed with plenty of features: support for ROS, AGM, Qt4/Qt5, hierarchical state machines and much more. Despite it was initially developed using Java/Xtext, now it’s implemented using PyParsing/Cog (two Python modules). The tool is under constant evolution and we have multiple tasks to be done:

* Create special specific files for AGM and ROS, to help users structure their code.
* Update the documentation of the tool
* Update code generation to replace Qt with c++11 features
* Add support for Python 3

Needed skills: Python, Cog (python module)  
Mentor: Pablo Bustos, Luis J. Manso  
Backup mentor: Marco A. Gutiérrez  

### 14\. Graphical, automatic, real-time animation of RoboComp state-machines.

A very important tool of RoboComp is the state-machine code generator. The design and implementation of complex robot behaviour demands specific tools to create and debug highly structured programs that can be debugged during real-time execution. This project proposes the extension of RoboCom’s state-machine code generator to include new derived classes that will bring real-time animation of the program flow. The student will need skills in C++, Qt and Python to create code that will display the state-machine as an animated structure in a transparent way for the user of the tool. This graphic feature will be optional and non intrusive for the logic counterpart.

Needed skills: C++, Python, Qt5.  
Mentor: Iván Barbecho, Pablo Bustos  
Backup mentor: Ramón Cintas  

## Mentors:

### Marco A. Gutiérrez

marcogATunexDOTes  
Robocomp Developer  

### Pablo Bustos

pbustosATunexDOTes  
Professor, RoboLab,  
University of Extremadura  

### Luis J. Manso

lmansoATunexDOTes  
Postdoc Researcher, RoboLab,  
University of Extremadura  

### Ramon Cintas

rcintasATunexDOTes  
Researcher, Robolab,  
University of Extremadura  

### Esteban Martinena

martinenaDOTestebanATgmailDOTcom  
Robocomp Developer  

### Pedro Núñez

pnuntruATunexDOTes  
Professor, RoboLab,  
University of Extremadura  

### Pilar Bachiller

pilarbATunexDOTes  
Professor, RoboLab,  
University of Extremadura  

### Ivan Barbecho

ibarbechATalumnosDOTunexDOTes   
Researcher, Robolab,  
University of Extremadura  

### Nicolás González

nicolasATunexDOTes  
Developer, Robolab,  
University of Extremadura  
