# ros_from_src

Build ros from source without using a PPA in a dockerfile (and later a github action).
Probably just copy what archlinux is doing.

    git clone git@github.com:lucasw/ros_from_src.git
    cd ros_from_src
    docker build .

To build with another ubuntu version:

    docker build --build-arg IMAGE=ubuntu:21.10 --build-arg PYTHON_MINOR_VERSION=9 . -t ros2110

Build with default version, but give it a tag:

    docker build --build-arg IMAGE=ubuntu:20.04 . -t ros2004
