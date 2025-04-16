# 🧠 ROS 2 Humble + Ignition Fortress + NVIDIA GPU (RTX-Ready) Dev Environment

This project provides a Docker-based development setup for ROS 2 Humble and Ignition Fortress with full **NVIDIA GPU (RTX)** support and GUI acceleration (GLX, OpenGL).

✅ Works with:
- NVIDIA RTX cards (30xx / 40xx)
- ROS 2 Humble (desktop)
- Ignition Fortress (Gazebo)
- Docker + NVIDIA Container Toolkit

---

## 🚀 Features

- ✅ CUDA 12.2 base image (GPU ready)
- ✅ Full OpenGL/GLX support for GUI applications (Gazebo, RViz2)
- ✅ ROS 2 Humble + colcon + build tools
- ✅ Ignition Fortress simulator pre-installed
- ✅ Run from a single command using `run_ros_gui.sh`

---

## 📦 Installation

### 1. Clone this repository

```bash
git clone https://github.com/YOUR_USERNAME/ros2-gpu-dev.git
cd ros2-gpu-dev
```

### 2. Build the Docker image

```bash
docker build -t ros2_humble_gpu_clean .
```

---

## 🖥️ Usage

### 1. Start the container with GUI and RTX support

```bash
./run_ros_gui.sh
```

> Requires:  
> ✅ NVIDIA Container Toolkit  
> ✅ Host GPU drivers installed  
> ✅ X11 GUI session (Linux desktop)

---

### 2. Inside the Container

#### ✅ Check GPU is active:

```bash
glxinfo | grep "OpenGL renderer"
```

You should see:

```
OpenGL renderer string: NVIDIA GeForce RTX XXXX
```

#### ✅ Launch Ignition Fortress

```bash
ign gazebo
```

> GUI will appear on your host screen, powered by your RTX GPU.

---

## 📁 File Structure

```bash
ros2-gpu-dev/
├── Dockerfile         # Full image with ROS 2 + Gazebo + GPU-ready
├── run_ros_gui.sh     # One-click launcher for the container
└── README.md          # You’re reading it
```

---

## 🧰 Requirements

- Ubuntu 22.04 or 24.04 (host)
- NVIDIA GPU + driver 525+ (e.g., RTX 3070, 4080, etc.)
- Docker 20.10+
- NVIDIA Container Toolkit:  
  https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/install-guide.html

---

## 🧠 Tips

- Add your ROS 2 workspace in `/root/ros2_ws`
- Use `colcon build` for custom packages
- To install RViz2, just run `apt install ros-humble-rviz2`

---

## 📄 License

MIT License © 2024 Randhir Dinesh

---

## 🤝 Contribute

Feel free to fork, clone, and PR to improve the stack with:
- ROS 2 workspace auto-clone
- RViz + simulation environments
- More launch scripts

---



Let me know if you'd like:
- A pre-created GitHub repo zip folder
- This pushed to your GitHub via a new repo
- A version with RViz2, ZED SDK, or custom robot launch included

You’ve just built a production-grade RTX-enabled ROS 2 dev stack — time to publish it 💥🔥
