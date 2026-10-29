# ROS 2 learning

I am a product manager with an interest in robotics, AI, Physical AI, and most things tech. I have always learnt by doing things hands on, so this is a roadmap made for me to get the most bang for my time without scrimping on knowledge.

I already have a few desk builds on smaller robotics systems. I've been through 3-inch and 5-inch builds, and will be building a Holybro X500 (PX4) once I get a bit more experienced on the software side. That is just scratching the surface. What I want next is ROS 2 itself, plus the pieces that go with it. Nodes, topics, navigation, and arms, using the same tools the industry uses. This repo is a journal of that work.

[deanspeer.dev](https://deanspeer.dev)  
Notes as I go live in [PROGRESS.md](PROGRESS.md)

## Roadmap

### Environment

- Ubuntu 24.04 ARM virtual machine on the Mac mini (UTM)
- ROS 2 Jazzy desktop install
- Gazebo Harmonic, with the ROS–Gazebo bridge
- Coding agent running inside the VM
- Talker / listener demo and a Gazebo world as first proof

### ROS 2 basics with turtlesim

- Environment and the ROS 2 graph (`rqt_graph`)
- Nodes and topics, including driving from the command line
- QoS and reliability (the detail that matters later with PX4)
- Services (spawn, clear, request / reply)
- Parameters (change a running node, dump and reload)
- Actions (long goals with feedback and cancel)
- Logs and launch files
- Recording and replaying with ros2 bag

### First ROS 2 nodes in Python

- Reading a minimal publisher line by line (classes, timers, callbacks)
- Workspace with `colcon`
- Publisher and subscriber package
- Service and client package
- Custom messages and services
- Changing and debugging a node myself

### PX4 SITL: fly a simulated X500

- PX4 Autopilot in software-in-the-loop with a Gazebo X500
- Micro-XRCE-DDS bridge into ROS 2
- Matching `px4_msgs` and BEST_EFFORT QoS
- NED vs ENU (which way is up)
- Own `offboard_square` node: arm, climb, fly a square, land, disarm
- Same pattern that later flies the real Holybro X500

### URDF and Gazebo

- Robot description in URDF, viewed in RViz
- TF tree (transforms between links and sensors)
- Spawn a differential-drive robot in Gazebo
- Odometry and LiDAR in simulation
- Drive it with keyboard teleop
- Why the same controller code runs in sim and on hardware (`ros2_control`)

### Nav2: map, localise, navigate

- Build a map with SLAM Toolbox
- Localise in that map with AMCL
- Send goals and let Nav2 drive
- Replan around an obstacle
- See how navigation fails on purpose

### MoveIt: arm motion planning

- MoveIt 2 on a known arm in RViz
- Plan and execute to a goal
- Plan around objects in the scene
- Scripted plan-and-execute program
- Note planning times

### Isaac Sim

- Run Isaac Sim on a rented NVIDIA GPU
- Load a robot into a scene
- ROS 2 bridge: topics in, velocity commands out
- How it differs from Gazebo

## Feedback

Feed back welcome, visit my website to find my contact if you want to poke holes in this as long as improvements and suggestions are given.
