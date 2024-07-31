# Embedded System Design: Secure Handheld Messenger Device
## Overview
This project is an embedded systems design challenge focused on creating a secure communication scheme using the Adafruit Classic Playground. The goal is to build a handheld messenger device that can transmit one of ten predefined messages across a network of five nodes (representing five team members). Each message is encoded by a unique hand movement sequence, detected by the accelerometer on the device, and transmitted sequentially from Node 1 to Node 5. The challenge is to ensure that each node decodes and transmits the message correctly, even though the message enumeration differs between nodes.

## Objective
The primary objective is to design and implement a secure, simple communication protocol using the Adafruit Classic Playground. The device will:

- Encode a message as a specific hand movement sequence.
- Transmit the message from one node to the next using the encoded hand movement.
- Each node will decode the message and display it using one of the 10 NeoPixels.
- Successfully transmit the message from Node 1 to Node 5, with each node having a unique message enumeration.
## Project Structure
### Components Used
- Adafruit Classic Playground: The main microcontroller board used for this project. It comes with a built-in accelerometer, NeoPixels, and other sensors that will be used to detect hand movements and display messages.
- Accelerometer: Used to detect specific hand movements that correspond to each of the 10 predefined messages.
- NeoPixels: Used to visually indicate the decoded message at each node.

### Workflow
#### Message Selection:
- Node 1 selects a message (1-10) to transmit.
- The selected message is associated with a specific hand movement sequence.
#### Message Encoding and Transmission:
- Node 1 performs the hand movement sequence corresponding to the selected message.
- The accelerometer on Node 2’s device detects the movement, decodes the message, and lights up the corresponding LED on the NeoPixel ring.
#### Sequential Transmission:
- Node 2 picks up Node 3’s device and transmits the same message using the same hand movement sequence.
- This process continues until the message reaches Node 5.
#### Message Cross-Referencing:
- Each node has a unique cross-reference list for messages. For example, "I need an A" might be Message 5 for Node 1, Message 3 for Node 2, and so on.
- The hand movement for each message remains consistent across all nodes, but the enumeration of messages differs.
### Objective:
Successfully transmit the message from Node 1 to Node 5, with the correct LED lighting up on each node’s NeoPixel ring.
Implementation
### Implementation 
#### [Demonstration](https://youtu.be/1WiLkfjCwK0?si=eLJyImfDz9G9vf5Z)
#### [Gestures and Messages](https://drive.google.com/file/d/1-uJJ7Eq9zyjP7pJjNqWASnRE3qIeskAY/view?usp=sharing)
