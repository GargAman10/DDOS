Project Title: Configuration Manual For SDN Based DDoS Attack Simulation Platform

Overview
This project is a research initiative focused on the detection and mitigation of Distributed Denial of Service (DDoS) attacks within a Software Defined Networking (SDN) environment. The simulation platform utilizes various tools and protocols to effectively manage network traffic and implement machine learning techniques for attack detection.

Key Features
SDN Implementation: Utilizes OpenFlow protocol and OpenVSwitch for managing network traffic.
Traffic Generation: Employs Hping3 and Iperf for generating normal and attack traffic.
Machine Learning: Implements statistical and machine learning methods using Python to analyze network traffic and detect attacks.
Simulation Environment: Built on Mininet to create a virtual network topology for testing.

Tools and Technologies
OpenFlow Protocol: Standard protocol for SDN.
OpenVSwitch: A virtual switch designed to enable network automation.
Ryu Controller: A Python-based open-source SDN controller for defining rules and logic.
Mininet: A network emulator that creates a virtual network topology.
Hping3: A packet generator for TCP/IP traffic, used for network security testing.
Iperf: A tool for network performance measurement and traffic generation.
Python Libraries: Includes NumPy and Scikit-learn for machine learning tasks.

Installation Instructions

System Requirements: Ensure you are using Ubuntu 20.04.1 LTS or a compatible Linux distribution.
Update and Upgrade Packages:

sudo apt-get update
sudo apt-get upgrade

Install Python and Required Libraries:

sudo apt install python2
sudo apt install python3
sudo apt install python3-pip
sudo pip3 install ryu numpy sklearn

Install Required Tools:

sudo apt-get install openvswitch-switch
sudo apt-get install mininet
sudo apt-get install iperf
sudo apt-get install hping3

Simulation Setup
Traffic Data Collection:

Modify controller.py to set APP TYPE=0 and TEST TYPE=0 for normal traffic data collection.
Use topo.py to set TEST TYPE=normal and run the simulation.
Attack Traffic Simulation:

Change TEST TYPE=attack in topo.py and run the simulation to generate attack traffic.
DDoS Attack Detection:

Set APP TYPE=1 in controller.py to enable attack detection.
Monitor the controller's response and mitigation actions through the terminal.

Results and Evaluation
The system is evaluated based on its accuracy and detection rate in identifying DDoS attacks. The results can be analyzed using the provided Python scripts for accuracy and detection rate calculations.

Limitations
The current implementation may not effectively handle attacks from trusted sources that are included in the training dataset, necessitating further research and enhancements.
