# Mir_custom_navigation_package

# Agenda

- [Prerequisites](#prerequisite)
    - [Workspace Setup](#workspace-setup)
    
- [Navigation Running](#navigation-running)

## **Prerequisites**

> Note: If you have already done prerequisite, you may move to [Navigation step](#navigation-running).

### **Workspace setup**

> Note: I have named the workspace as `mir_ws`, you can change name as per your requirement.

- create or change the directory to the workspace directory.

    `mkdir -p mir_ws/src`

    or

    `cd mir_ws/src`

- git clone the mir robot package.

    `git clone -b noetic https://github.com/DFKI-NI/mir_robot.git`

    &

    `https://github.com/pondinesh006/Mir_custom_navigation_package.git`

- change the directory to the workspace directory.

    `cd mir_ws`

- Install the requirement packages using

    `sudo apt-get update`
    
    `sudo apt-get -y upgrade`
    
    ``` Install dependencies
    sudo apt-get -y install ros-noetic-costmap-queue \
    ros-noetic-dwb-critics \
    ros-noetic-rospy-message-converter \
    ros-noetic-sbpl-lattice-planner \
    ros-noetic-dwb-plugins \
    ros-noetic-move-base \
    ros-noetic-amcl \
    ros-noetic-teb-local-planner \
    ros-noetic-map-server \
    ros-noetic-fake-localization \
    ros-noetic-robot-localization
    ```

## **Navigation Running**

- change the directory to the workspace directory.

    `cd Home/mir_ws`

- source the workspace directory.

    `source devel/setup.bash`

- launch the navigation file along with simulation file.

    `roslaunch mir_navigation_customized mir_navigation_customized.launch`

    > Note: Now, I have used fake localization for the navigation. We can able to change the localization to the amcl localization through uncomment amcl on the `mir_navigation_customized.launch` file and comment out fake localization.

- Now, you can give the `2d Nav goal` for the autonmous navigation.

- For closing `ctrl + c` on the terminal.

**_--The end--_**
