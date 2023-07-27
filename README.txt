
    
    DockerFile commit that launches Docker Container of ROS2 Humble
    and has install packages for SLAM algorithm and visualization in
    RVIZ.
    
    DockerFile references locally contained files (lidar_scan/) so
    build image in directory containing both

	EX: Current tree structure before I build my image. My working directory is /Athackst

Athackst
.
├── Dockerfile
├── lidar_scan
│   ├── launch
│   │   └── lidar.launch.py
│   ├── lidar_scan
│   │   ├── __init__.py
│   │   └── lidar_pub.py
│   ├── package.xml
│   ├── resource
│   │   └── lidar_scan
│   ├── rviz
│   │   └── wamv_config.rviz
│   ├── setup.cfg
│   ├── setup.py
│   └── test
│       ├── test_copyright.py
│       ├── test_flake8.py
│       └── test_pep257.py
├── README.txt
└── tahseen.rviz

6 directories, 14 files



Instructions for when in Docker Container

1. cd into home directory 
2. source /opt/ros/humble/setup.bash 
3. cd /ros2_ws
4. colcon build 
5. . install/setup.bash 
6. ros2 launch lidar_scan lidar.launch.py 
7. In a separate terminal, still within the docker container, run "ros2 launch slam_toolbox online_async_launch.py" 


