# AI-week2_tasks

## TASK 1 : 
The installation steps of Ubuntu and ROS 
1-Download Ubuntu 20.04.4 LTS Desktop Image from this URL: https://releases.ubuntu.com/20.04/ubuntu-20.04.4-desktop-amd64.iso

2-Download and install VirtualBox.

3-After installing VirtualBox, click New to make a new virtual machine.

4-Type Ubuntu in the field Name.

5-Set the type to Linux, and version to Ubuntu (64-bit) then click Next.

6-Set the Memory size to the end of the green bar and click Next.

7-Click Next and then click Create.

8-After creating the virtual machine we should connect Ubuntu image that we downloaded in step number 1, we do that by double clicking on the virtual machine.

9-After launching the virtual machine, click browse and choose the Ubuntu image then click Start.

10-Click Install Ubuntu then continue and wait until the installation is finished.

## TASK 2 :

Install ROS on jetson nano

1-	Open a new terminal

2-	Set up the Jetson Nano to accept software from packages.ros.org : 

    $ sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'

3-	Add a new apt key: 

    $ sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654

4-	Update the Debian packages index:

    $ sudo apt update

5-	Install the ROS Desktop package :

    $ sudo apt install ros-melodic-desktop

6-	load the ROS environment variables automatically when you execute a new shell session

    $ echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc
    $ source ~/.bashrc
    
7-	Install and initialize rosdep :

    $ sudo apt install python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential
    $ sudo rosdep init
    $ rosdep update

Now the Jetson Nano is ready to execute ROS packages


