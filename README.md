# ros-bridge-docker-demo

Demo showing how to connect ROS and ROS 2 over ROS 1 bridge using Docker Compose - just a basic ROS1-talker and ROS2-listener.

## running

```bash
docker-compose up
```

## output log example

```bash
Recreating ros-bridge-docker-demo_ros-master_1 ... done
Recreating ros-bridge-docker-demo_ros2_1       ... done
Recreating ros-bridge-docker-demo_ros1_1       ... done
Recreating ros-bridge-docker-demo_bridge_1     ... done
Attaching to ros-bridge-docker-demo_ros-master_1, ros-bridge-docker-demo_ros2_1, ros-bridge-docker-demo_ros1_1, ros-bridge-docker-demo_bridge_1
ros-master_1  | ... logging to /root/.ros/log/e2525d1e-de74-11eb-91d0-0242ac190002/roslaunch-c7a52d6acee7-1.log
ros-master_1  | Checking log directory for disk usage. This may take a while.
ros-master_1  | Press Ctrl-C to interrupt
ros-master_1  | Done checking log file disk usage. Usage is <1GB.
ros-master_1  | 
ros-master_1  | started roslaunch server http://c7a52d6acee7:46809/
ros-master_1  | ros_comm version 1.15.11
ros-master_1  | 
ros-master_1  | 
ros-master_1  | SUMMARY
ros-master_1  | ========
ros-master_1  | 
ros-master_1  | PARAMETERS
ros-master_1  |  * /rosdistro: noetic
ros-master_1  |  * /rosversion: 1.15.11
ros-master_1  | 
ros-master_1  | NODES
ros-master_1  | 
ros-master_1  | auto-starting new master
ros-master_1  | process[master]: started with pid [33]
ros-master_1  | ROS_MASTER_URI=http://c7a52d6acee7:11311/
ros-master_1  | 
ros-master_1  | setting /run_id to e2525d1e-de74-11eb-91d0-0242ac190002
ros-master_1  | process[rosout-1]: started with pid [44]
ros-master_1  | started core service [/rosout]
ros1_1        | [INFO] [1625587916.723012]: hello world 1625587916.7229428
ros1_1        | [INFO] [1625587916.823246]: hello world 1625587916.8231428
ros1_1        | [INFO] [1625587916.923463]: hello world 1625587916.9233472
ros1_1        | [INFO] [1625587917.023426]: hello world 1625587917.0232832
ros1_1        | [INFO] [1625587917.123590]: hello world 1625587917.1232712
ros1_1        | [INFO] [1625587917.223647]: hello world 1625587917.2233222
ros1_1        | [INFO] [1625587917.323894]: hello world 1625587917.323564
ros1_1        | [INFO] [1625587917.424103]: hello world 1625587917.4237773
ros1_1        | [INFO] [1625587917.523645]: hello world 1625587917.5233216
ros1_1        | [INFO] [1625587917.623652]: hello world 1625587917.6233299
ros1_1        | [INFO] [1625587917.723644]: hello world 1625587917.72332
ros1_1        | [INFO] [1625587917.823873]: hello world 1625587917.8235059
ros1_1        | [INFO] [1625587917.923647]: hello world 1625587917.9233246
ros1_1        | [INFO] [1625587918.023836]: hello world 1625587918.0234787
ros1_1        | [INFO] [1625587918.123686]: hello world 1625587918.1233351
ros1_1        | [INFO] [1625587918.223897]: hello world 1625587918.2235441
ros1_1        | [INFO] [1625587918.323907]: hello world 1625587918.3235562
ros1_1        | [INFO] [1625587918.423692]: hello world 1625587918.4233441
ros1_1        | [INFO] [1625587918.523712]: hello world 1625587918.5233612
ros1_1        | [INFO] [1625587918.623702]: hello world 1625587918.6233523
bridge_1      | [INFO] [1625587918.628248974] [ros_bridge]: Passing message from ROS 1 std_msgs/String to ROS 2 std_msgs/msg/String (showing msg only once per type)
bridge_1      | [INFO] [1625587918.628902132] [ros_bridge]: Passing message from ROS 2 rcl_interfaces/msg/Log to ROS 1 rosgraph_msgs/Log (showing msg only once per type)
ros2_1        | [INFO] [1625587918.629136974] [listener]: I heard: [hello world 1625587918.6233523]
ros1_1        | [INFO] [1625587918.723527]: hello world 1625587918.723327
ros2_1        | [INFO] [1625587918.726381213] [listener]: I heard: [hello world 1625587918.723327]
ros1_1        | [INFO] [1625587918.823877]: hello world 1625587918.823526
ros2_1        | [INFO] [1625587918.829197105] [listener]: I heard: [hello world 1625587918.823526]
ros1_1        | [INFO] [1625587918.923574]: hello world 1625587918.9233294
ros2_1        | [INFO] [1625587918.927553797] [listener]: I heard: [hello world 1625587918.9233294]
ros1_1        | [INFO] [1625587919.023484]: hello world 1625587919.023349
ros2_1        | [INFO] [1625587919.025555661] [listener]: I heard: [hello world 1625587919.023349]
ros1_1        | [INFO] [1625587919.123634]: hello world 1625587919.1232822
ros2_1        | [INFO] [1625587919.128652739] [listener]: I heard: [hello world 1625587919.1232822]
ros1_1        | [INFO] [1625587919.223555]: hello world 1625587919.2233195
ros2_1        | [INFO] [1625587919.227244130] [listener]: I heard: [hello world 1625587919.2233195]
ros1_1        | [INFO] [1625587919.323825]: hello world 1625587919.323476
ros2_1        | [INFO] [1625587919.328713292] [listener]: I heard: [hello world 1625587919.323476]
ros1_1        | [INFO] [1625587919.423416]: hello world 1625587919.4232185
ros2_1        | [INFO] [1625587919.426110540] [listener]: I heard: [hello world 1625587919.4232185]
ros1_1        | [INFO] [1625587919.523648]: hello world 1625587919.5232947
ros2_1        | [INFO] [1625587919.528764606] [listener]: I heard: [hello world 1625587919.5232947]
```
