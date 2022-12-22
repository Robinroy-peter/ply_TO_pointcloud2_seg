# ply_TO_pointcloud2_seg
.ply to pointcloud2  convert and import into ros, plane seg , dynamic ops publish

Compile the workspace in ur local system
Follow below steps

sudo apt-get install ros-noetic-costmap-converter*

roscore

rosrun tf static_transform_publisher 0 0 0 0 0 0 map base_link 50

roslaunch ply_ros_publisher ply_ros_publisher.launch

rosrun rviz rviz
open config and load .rviz from pcl_seg .rviz

roslaunch pcl_seg pcl_seg.launch

for lanuching dynamic obs pub

rosrun obs_pub dynamic_obs_pub.py
rosrun obs_pub groundtruth_obs_pub.py
rosrun obs_pub simple_obs_pub.py


