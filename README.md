WOZ_AI_Camera_Surveillance
==========================

### About

This project originated out of an idea from the course Human-AI-Interaction Design taught at Cornell University. 
We use motorized camera blockers to limit what surveillance cameras can capture. These camera blockers are visual to the person under monitoring and help to explain the surveillance status.
The first use and trial of the contextually switching blockers were during a Public Interest Fellowship from Cornell Tech with the YAI yetwork.

This repository holds the Node-Red flows that make individual components communicate. A few small code pieces, such as the manual servo control, were directly implemented in Node-Red.
The OpenCV program, written in python, does not directly communicate with the LEDs, motor with color sensor, and push notification server; instead it uses node-red to send and receive events through http requests and a Flask webserver to stream video images. 


|Description | Nodes | 
| :---            | :--        |  
|These nodes start the camera monitoring code, push notification server and http request module. |![image](https://user-images.githubusercontent.com/90477986/183556960-8ff077c8-9c6d-4bd0-81f7-fd01f98bb4f8.png)|
|These nodes provide the UI controls for calibrating the bed position, displaying the video stream, and opening the camera. |![image](https://user-images.githubusercontent.com/90477986/183558715-53ee31ba-375b-4ee8-82e2-7905ac019056.png)|
|These nodes control the motor which moves the camera lens shutters manually, or color calibrated, as well as control the LED lights. |![image](https://user-images.githubusercontent.com/90477986/183558946-d36d5e15-0e0b-489e-af5b-d3f03e30ead0.png)|
|These nodes make the camera lens shutter switch contexually. |![image](https://user-images.githubusercontent.com/90477986/183559014-a62ef0fa-fb6b-45af-9ec3-41037b6fb66a.png)|

The python code for the camera monitoring as well as motor and LED control can be found in: https://github.com/HaukeCornell/movenet_stream_privacy
