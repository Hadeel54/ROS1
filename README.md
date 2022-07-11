# ROS1
This project is used to share the steps to install and practice ROS1 on Ubuntu


Step 1: 
Download and install VirtualBox

Step 2:
Download Ubuntu 20.04.4 LTS (Focal Fossa)
Link : https://releases.ubuntu.com/20.04.4/?_ga=2.133889290.525729052.1657570706-2012564934.1657297505

Step 3:
Run VirtualBox and install Ubuntu

Step 4: 
Start Ubuntu system and run the terminal
Execute below commands in sequenese to install ROS Noetic

  1. Setup your sources.list
  - Setup your computer to accept software from packages.ros.org.

  - command below:
  sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'

  2. Set up your keys

  - command below:
  sudo apt install curl # if you haven't already installed curl
  curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -

  3. Installation
  - First, make sure your Debian package index is up-to-date:

  - command below to update:
  sudo apt update

  - This command to install the ROS desktop version:
  sudo apt install ros-noetic-desktop-full
  
  4. Environment setup
  - You must source this script in every bash terminal you use ROS in.
  - Command below :
  source /opt/ros/noetic/setup.bash
  
  5. Add Dependencies for building packages
  - Up to now you have installed what you need to run the core ROS packages. To create and manage your own ROS workspaces, there are various tools and  requirements that are distributed separately. For example, rosinstall is a frequently used command-line tool that enables you to easily download many source trees for ROS packages with one command.

  - To install this tool and other dependencies for building ROS packages, run:

  sudo apt install python3-rosdep python3-rosinstall python3-rosinstall-generator python3-wstool build-essential
  Initialize rosdep

  - Before you can use many ROS tools, you will need to initialize rosdep. rosdep enables you to easily install system dependencies for source you want to compile and is required to run some core components in ROS. If you have not yet installed rosdep, do so as follows.

  sudo apt install python3-rosdep
  
  - With the following, you can initialize rosdep.

  sudo rosdep init
  rosdep update

Reference: https://wiki.ros.org/noetic/Installation/Ubuntu


