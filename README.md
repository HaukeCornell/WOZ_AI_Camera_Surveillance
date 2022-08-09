WOZ_AI_Camera_Surveillance
==========================

### About

This project originated out of an idea from the course Human-AI-Interaction Design taught at Cornell University. 
We use motorized camera blockers to limit what surveillance cameras can capture. These camera blockers are visual to the person under monitoring and help to explain the surveillance status.
The first use and trial of the contextually switching blockers were during a Public Interest Fellowship from Cornell Tech with the YAI yetwork.

This repository holds the Node-Red flows that make individual components communicate. A few small code pieces, such as the manual servo control, were directly implemented in Node-Red.
The OpenCV program, written in python, does not directly communicate with the LEDs, motor with color sensor, and push notification server; instead it uses node-red to send and receive events through http requests and a Flask webserver to stream video images. 