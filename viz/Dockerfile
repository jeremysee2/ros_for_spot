FROM osrf/ros:noetic-desktop-full

RUN apt install ros-noetic-joint-state-publisher-gui 
# ros-noetic-moveit

RUN mkdir -p /root/catkin_ws/src
WORKDIR /root/catkin_ws
RUN /bin/bash -c "source /opt/ros/noetic/setup.bash"
RUN echo "source /opt/ros/noetic/setup.sh" >> /root/.bashrc
RUN echo "source /root/catkin_ws/devel/setup.bash" >> /root/.bashrc
WORKDIR /root/catkin_ws/src