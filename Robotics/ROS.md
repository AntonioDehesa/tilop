# ROS
ROS stands for Robot Operating System. It is a meta-OS which allows us to communicate our robots, program them, etc. 
It is one of the most used tools for robotics. I have had some experience with it, during college. 

## Launch file
It is an XML type of file, which allows us to call nodes and processes with different arguments, as well as run several processes at the same time.  
Instead of opening several terminals to execute several processes, we can simply use a .launch file to do so.  

### Arguments
```xml
<arg name="example" default="$(env VARIABLE)" doc="type [x, y, z]">
```
These are the arguments which we can use to launch the file. It includes a default value, in case we dont use parameters to call it. 
### IF and unless

If certain condition is met, then stuff inside group will happen. 
```xml
<group if="$(arg foo)">
<!-- Your stuff here-->
</group>
```
If certain condition is met, then stuff inside will not happen/be set. 
```xml
<param name="foo" value="bar" unless="$(arg foo)" />  <!-- This param won't be set when "unless" condition is met -->
```

### References to other launch files
```xml
<launch>
  <node name="talker" pkg="rospy_tutorials" type="talker" />
</launch>
```
With the previous instruction, we can launch another launch file. This way, we can include several launch files inside just one, and execute several nodes with just one instruction. 