# Recordings

ROS 2 recordings (bags) from the turtlesim work.

- `turtle_drive/` is a 37 second drive, recording `/turtle1/cmd_vel` and `/turtle1/pose`. With turtlesim running, `ros2 bag play bag_files/turtle_drive` replays it.
- `turtle_drive_info.txt` is its summary from `ros2 bag info`, 12 commands and 2,302 position messages.
