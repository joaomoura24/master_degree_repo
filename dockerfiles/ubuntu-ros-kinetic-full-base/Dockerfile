FROM jakutenshi/ubuntu-dev

RUN sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list' \
    && apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80 --recv-key 421C365BD9FF1F717815A3895523BAEEB01FA116      \
    && apt-get update                                                                                                       \
    && apt-get install -y ros-kinetic-desktop-full                                                                          \
    && rosdep init                                                                                                          \
    && rosdep update                                                                                                        \
    && echo "source /opt/ros/kinetic/setup.bash" >> ~/.bashrc                                                               \
    && apt-get install -y python-rosinstall python-rosinstall-generator python-wstool
