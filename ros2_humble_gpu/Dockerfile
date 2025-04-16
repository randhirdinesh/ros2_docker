FROM osrf/ros:humble-desktop

# Setup environment
ENV DEBIAN_FRONTEND=noninteractive
ENV LANG=C.UTF-8
ENV LC_ALL=C.UTF-8

# Install common tools and GPU support libs
RUN apt update && apt install -y \
    python3-colcon-common-extensions \
    python3-pip \
    curl \
    git \
    vim \
    build-essential \
    ros-humble-rviz2 \
    ros-humble-gazebo-ros \
    nvidia-cuda-toolkit \
    && rm -rf /var/lib/apt/lists/*

# Optional: Install PyTorch with CUDA (example)
RUN pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121

# Source ROS 2 in every shell
RUN echo "source /opt/ros/humble/setup.bash" >> ~/.bashrc

