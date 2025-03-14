# RM63BforReuleaux

This repo contains the packages for the simulation of the RML-63-B robot (of RealMan Robotics) used for the work on the repo Reuleaux_new (https://github.com/LucreziaPonti/Reuleaux_new)

Original repo: https://github.com/RealManRobot/rm_models/tree/main/RML63/urdf/rm_63_b_description


## Changes made
### Description package
- base_footprint added: to fix some minor issues with the solvers a dummy link (the frame base_footprint corresponds to the base_link frame of the robot) was added to the rm_63_b.urdf file;
- bummy mobile base: since the robot available in the lab was mounted on a mobile base, to simulate such situation, a new urdf has been created that contains the robot + a simple box fixed to the robot base (that fits the dimetions of a turtlebot3 Waffle). (the frame base_footprint in this case is at the base of the box);
- dummy gripper: consider the case of a gripper being applied to the robot a dummy gripper "link" was added
- fixed launches file: the launch file display.launch has been modified to make it simpler to choose which version to simulate (with or without the base) using the optional arg **dummy_base** (default=*true*)

### Moveit_config package

The package has been created using the MoveIt! Setup Assistant.

It contains the URDF and SRDF files of both the manipulator on its own (*rm_63_b*) or the manipulator mounted on the dummy base (*rm_63_b_dummy_base*). To choose between the two at launch (for demo.launch mainly) there is an optional argument *dummy_base* that when set to true loasd the robot with the base, by default it is set to true.

**issues** : the gazebo.launch still gives some issues in the ws I'm working on so I'm not sure it works ok. - will look into it if possible