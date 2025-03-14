# RM63BforReuleaux

This repo contains the packages for the simulation of the RML-63-B robot (of RealMan Robotics) used for the work on the repo Reuleaux_new (https://github.com/LucreziaPonti/Reuleaux_new)

Original repo: https://github.com/RealManRobot/rm_models/tree/main/RML63/urdf/rm_63_b_description


## Changes made
### Description package
- base_footprint added: to fix some minor issues with the solvers a dummy link (the frame base_footprint corresponds to the base_link frame of the robot) was added to the rm_63_b_description.urdf file;
- bummy mobile base: since the robot available in the lab was mounted on a mobile base, to simulate such situation, a new urdf has been created that contains the robot + a simple box fixed to the robot base (that fits the dimetions of a turtlebot3 Waffle). (the frame base_footprint in this case is at the base of the box);
- dummy gripper: consider the case of a gripper being applied to the robot a dummy gripper "link" was added
- fixed launches file: the launch file display.launch has been modified to make it simpler to choose which version to simulate (with or without the base) using the optional arg **base** (default=*true*)

### Moveit_config package

**to be done**
The package has been created using the MoveIt! Setup Assistant
