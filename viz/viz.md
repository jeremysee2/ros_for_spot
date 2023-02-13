# Visualization in RViz

In order to test the robot in simulation, we make use of the [MoveIt controller by estherRay](https://github.com/estherRay/Spot-Arm) for the robot arm, and the tutorial on how to run RViz in Docker from [nebohq](https://github.com/nebohq/mac-ros).

## Setting up Docker container for RViz

Importantly, find the correct ROS_MASTER_URI linking to the Docker container containing the running `roscore`. This involves some networking setup with Docker.

1. In ros.env, change ROS_MASTER_URI=[YOUR ROS MASTER]
2. `docker-compose up --build`
3. In a separate terminal, `docker-compose exec ros bash`
4. Build the ROS project, `cd ~/catkin_ws && catkin_make && source devel/setup.bash`
5. Run RViz, `rosrun rviz rviz`
6. On your computer, open a browser and go to `localhost:8080/vnc.html`