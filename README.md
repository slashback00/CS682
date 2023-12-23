
# TEAM 2 – Autonomous Drone
**Project Statement**: Develop the Autonomous Navigation Features of a Pixhawk Powered Drone. Utilize The Jetson Nano, ZED 2 Stereoscopic Camera, and 2d LiDAR to sufficiently travel a path in a supervised, heuristic environment. This repo provides waypoint-seeking drone heuristics tested on AirSim, and ready to deploy on a Pixhawk drone!

### Full Documentation [here!](https://slashback00.github.io/CS682_Autonomous_Drone/index.html)
## Hardware and Features

### Zed Camera
The ZED 2 Camera is a stereo depth camera that provides advanced depth sensing and environmental understanding capabilities. It is designed for a wide range of applications, including robotics, augmented reality, and spatial mapping. The ZED SDK provides APIs for depth sensing, spatial mapping, object detection, and more. This project uses the ZED 2 functionalities to detect waypoints, read distance and position, and pass those variables to the drone.
![image](https://github.com/slashback00/CS682_Autonomous_Drone/assets/69451310/0d4920f2-630b-4772-a035-44f4b59a34fb)

### QGroundcontrol
QGroundControl (QGC) is an intuitive and powerful ground control station (GCS) for UAVs. The primary goal of QGC is ease of use for both first time and professional users. It provides full flight control and mission planning for any MAVLink enabled drone, and vehicle setup for both PX4 and ArduPilot powered UAVs.
<img width="1680" alt="Screenshot_2023-10-25_at_16 22 09" src="https://github.com/slashback00/CS682_Autonomous_Drone/assets/69451310/e214fdb3-8b76-4063-8405-e3cb3547a823">


### 2d LiDAR
The 2D LiDAR system is an advanced sensor that uses laser light to measure distances and create a two-dimensional representation of the surrounding environment. It is widely used in robotics, autonomous vehicles, environmental monitoring, and other applications requiring accurate distance measurements and environmental mapping.

![Screenshot 2023-12-23 175919](https://github.com/slashback00/CS682_Autonomous_Drone/assets/69451310/d147c7f7-58e0-4dc4-ae2c-2c942b229a87)



### AirSim – Our UAV Simulator of Choice
AirSim is an open source vehicle simulator built on Unreal Engine. The simulator provides realistic drone physics and comes with ready-made compatibility with our drone hardware. AirSim comes with a Pixhawk flight control wrapper, which is the brand of flight controller we use for our drone, thus providing functionality for all simulated flights in the hardware. AirSim also comes with a ROS wrapper.

Follow these instructions to download AirSim here[installation_guide.html](https://slashback00.github.io/CS682_Autonomous_Drone/installation_guide.html)

## Demo the waypoint travel

1. **Before Running the code, activate a conda environment with environment.yml**

    ```bash
    conda env create -f environment.yml
    conda activate drone_env
    ```

2. Deploy the AirSimMap in Unreal Engine and hit play.

3. Point your Zed 2 camera at the designated waypoint (default humans, see follow_person_airsim documentation to change waypoint-designated objects. Optional: enter the yaw rotations needed for each waypoint as described in docs for multi-waypoint travel).

4. **Run the code and watch the drone move!**

    ```bash
    python follow_object_airsim.py
    ```
