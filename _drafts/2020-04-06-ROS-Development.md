---
layout: post
title: Robotics--Ros Development
date: 2020-04-04 9:12:00 -0500
categories: [tutorial]
tags: [aws, robotics]
---

# Goals
1. Setup Cloud9 ROS IDE.
2. Import PhantomX CAD
3. Get PhantomX CAD to move with ROS.

# Cloud9 ROS IDE

1. Creating a [Cloud9 ROS *Integrated Development Environment*](https://docs.aws.amazon.com/robomaker/latest/dg/cloud9-create-ide.html) (IDE)

## Import AWS Hello World

1. From the [RoboMaker: Day 01]({% post_url 2020-04-04-Robomaker-D01 %}) blog post [video](https://youtu.be/eQYUAMFvpLg)
2. clone the [aws-robomaker-tutorial-helloworld](https://github.com/timrobotson/aws-robomaker-tutorial-helloworld) repository.
    1. `git clone git@github.com:timrobotson/aws-robomaker-tutorial-helloworld.git` if you are using ssh.
    2. Copied the simulation workspace (/simulation_ws) folder and the robot workspace (/robot_ws) from the hello world tutorial to [PhantomX tutorial](https://github.com/bstankie/PhantomX-Tutorial).

## Learning ROS
3. [ROS tutorial #2: Publishers and subscribers](https://youtu.be/bJB9tv4ThV4)
    1. **Nodes**: 'modules' that do one specific thing.
        * E.g., odometer, drive, path planning, etc.
    2. **Topics**: The independent *nodes* communicate with one another through *topics*. 
        * Topics can be thought of as 'named communication channels' that nodes can send data to other nodes.
    3. **Messages**: Data sent on the topics are called *messages*
    1. **Publish**: Sending a *message* to a topic.
        * Any *node* can *publish* a *message* to any *topic* as long as it knows the name of the topic.
    5. **Subscribe**: A *node* wants to see all of the *messages* that are *published* on a topic.
    6. *Many-to-Many* relationship between *nodes* and topics.
        * Multiple *nodes* can *publish* to the same topic.
        * Multiple *nodes* can *subscribe* to the same topic.
        * A *node* can *publish* to multiple topics.
        * A *node* can *subscribe* to multiple topics.
    7. Useful command-line tools.
        * `rosnode list`: List all of the *topics*.
        * `rosnode info /<someNode>`: List of all of the *topics* the node is *publishing* and *subscribed* to.
        * `rostopic list`: All of the *topics*.
        * `rostopic info /<someTopic>`: List of all of the nodes that are *publishing* and *subscribing* to in that topic.
        * `rostopic echo /<someTopic>`: Display the *messages* *published* on that topic.
    ROS works through *publishing* and *subscribing* to *topics*.
    8. ROS Master keeps track of all of the *topics* and which *nodes* are *publishing* and *subscribing* to which topics.
        * `roscore` or `roslaunch` to launch the Master node.
        * better to use `roscore` and leave it running.
4. [ROS tutorial #2: Writing some Code](https://youtu.be/bJB9tv4ThV4?t=550)


https://youtu.be/9U6GDonGFHw

## Importing a CAD model


## Bundling ROS *robot* and *simulation* packages.
1. Steps used to describe how to build are in the [Hello World Sample](https://github.com/aws-robotics/aws-robomaker-sample-application-helloworld) repository.

## [wiki.ros.org Tutorial](http://wiki.ros.org/ROS/Tutorials)
