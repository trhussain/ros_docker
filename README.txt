Instructions 

1. cd into home directory 
2. source /opt/ros/humble/setup.bash 
3. cd /ros2_ws
4. colcon build 
5. . install/setup.bash 
6. ros2 launch lidar_scan lidar.launch.py 
7. In a separate terminal, still within the docker container, run "ros2 launch slam_toolbox online_async_launch.py" 


