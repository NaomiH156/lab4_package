### Naomi Hourihane, Modern Robot Programming Lab 4
## Sunday 1:45 PM




# View the robot in RVIZ with or without GUI, using either URDF or XACRO:

roslaunch lab4_package launch_options.launch use_xacro:=true use_gui:=true

launch_options.launch is what has the options for displaying the robot using either "robot.urdf" or "robot_xacro.xacro"

I have been checking rosrun_xacro.xacro with:

rosrun xacro xacro robot_xacro.xacro > urdf_from_xacro.urdf

and then checking that urdf_from_xacro is set up properly.

#View the robot using URDF only, with no GUI

roslaunch lab4_package launch.launch

This launcher uses robot.urdf only. It runs the correct robot_state_publisher and joint_state_publisher, but it does not include a GUI.

# Problems I am still having

In my robot_xacro.xacro file, I keep getting the following error:

unknown macro name: xacro:hokuyo

To double check that robot_xacro.xacro is set up properly, I have been doing the following command:

rosrun xacro xacro > urdf_from_xacro

However, once I added the Hokuyo and velocidyne stuff, I kept getting the error about the unknown macro name.

Additionally, this tells me that I am doing something wrong when I added the Hokuyo stuff to my XACRO file.

Everything else works okay.