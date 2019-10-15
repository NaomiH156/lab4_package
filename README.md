### Naomi Hourihane, Modern Robot Programming Lab 4
## Tuesday 2:45 PM

# ROBOT DESCRIPTIONS

robot.urdf - a hand-made URDF file describing the robot.

robot_xacro.xacro - a XACRO file describing the robot. Includes the Hokuyo and Velocydyne sensor meshes.

urdf_from_xacro.urdf - a urdf file derived from robot_xacro.xacro

urdf_from_xacro.xacro - This one exists by mistake. I don't know how to remove it from the git repository. It's the same as the one above but with the wrong filetype. Oopsie!

urdf_from_xacro.txt - This one also exists by mistake. Same as the one above but also with the wrong filetype. Oopsie!


# RVIZ Stuff

config.rviz - The RVIZ session I was using to display the robot. Already set up to read /robot_description as a parameter.

#LAUNCHERS

launch.launch - launches RVIZ, with config.rviz, using robot.urdf as /robot_description. Also launches joint_state_publisher and robot_state_publisher nodes, with appropriate GUI.

launch_options.launch - launches RVIZ, with config.rviz. Capable of using either robot.urdf OR a URDF generated from robot_xacro.xacro as /robot_description. Also launches joint_state_publisher and robot_state_publisher nodes, with appropriate GUI.


# TO LAUNCH WITH robot.urdf

roslaunch lab4_package launch.launch

OR

roslaunch lab4_package launch_options.launch

OR

roslaunch lab4_package launch_options.launch use_xacro:=false

# TO LAUNCH WITH robot_xacro.xacro

roslaunch lab4_package launch_options.launch use_xacro:=true