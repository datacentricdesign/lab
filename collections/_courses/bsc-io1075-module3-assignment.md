---
layout: minimal
title: "Network Communication"
permalink: /courses/bsc-io1075/module3/assignment
description: "Software-Based Product - Assignment 3"
assignment-id: 3
assignment-of: io1075-3
---

**Goal**:  In this assignment, you will connect to the world! You will develop a connected doorbell, establishing a connection between a button and a speaker, and back with a button and an opening mechanism. 
      
* Programming environment: environment (IDE, Jupyter), code execution
* Design: state diagrams, class diagrams
* Code management: - comments, functions
* Computational concepts: variables, types, boolean expression, objects, control flow

# Task 1:

## Step 1.1:


Assignment 3: Network communication (Week topic: Network Technology)
Goal: 

Programming environment: dependencies, debugging
Design: component and sequence diagrams
Code management: exceptions
Computational concepts:  communication models, protocols, data format (encoding, JSON)

Task 1: Checking the Doorbell Status
In this task you will learn how to establish a TCP connection and receive data from a doorbell. You will also build a basic server to explore the differences between client and server.

Task 1.1: Reading the doorbell status (Socket client)
Task 1.2: Listening for input (Socket server)
Task 1.3: Ping
Task 1.4: Debuging and managing exceptions
Task 2: Streaming the doorbell camera
In this task you will learn how to receive a live video stream from the doorbell camera with UDP. It will emphasise the difference between TCP and UDP.

Task 2.1: Receive raw doorbell camera feed via UDP
Task 2.2: Install openCV
Task 2.3: Show stream on the screen
Task 3: Listening to Doorbell Events
In this task you will learn a different model of communication, publish/subscribe, as opposed to a request/response model. This time, you will listen to events from the doorbell instead of checking its status.

Task 3.1: Connect and subscribe
Task 3.2: Decoding information
Task 3.3: Triggering action by publishing
Task 4: Integrating Network into the Lighting System

Task 4.1: Make a class DoorbellButton which receive data from the network
Task 4.2: Make the LightBulb send data to the network
Task 5: Sequence and Component Diagram
As your program is now connecting several components through a network, it is the appropriate moment to learn how to draw a sequence and component diagram.

Task 5.1: Component diagram
Task 5.2: Sequence diagram
