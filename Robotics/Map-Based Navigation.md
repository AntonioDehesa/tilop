# Map-Based Navigation: Introduction
## Localization
Helps the robot know where it is. 

## Mapping
The robot needs a map of its environment to be able to recognize where it has been moving.

## Motion or path planning
To plan a path, the target position must be well-defined to the robot, which will require an appropiate addressing scheme. 


# Building a Map: Simultaneous Localization And Mapping (SLAM)

The process of building a map using a sensors such as:
* Laser Sensors
* 3D Sensors 
* Ultrasonic Sensors

## Sensor fusion: This process uses filtering techniques like Kalman filters or particle filters. 


### Source
ROS for Beginners II: Localization, Navigation and SLAM, by Anis Koubaa, in Udemy.  


# Running SLAM

This algorithm included in the turtlebot3 package will create a map using the laser sensors of the robot. This map will be saved as an *occupancy grid map*. 

## Gmapping

In this part of the course, we will be using gmapping for the SLAM method. Gmapping is a ROS wrapper for OpenSlam's Gmapping.  
There are other methods, such as Cartographer, and Hector_SLAM, but those will be covered later. 

### Occupancy Grid Map

* A map is a grid (matrix) of a cell.
* A cell can be either empty or occupied. 
* Depending on the resolution, cell size can be 5-50 cm. 
* Each cell holds a probability of occupancy of 0% to 100%.
* Unknown areas are marked as **-1**

In RVIZ we can see the live process of the mapping.  
![Here is a screenshot of the mapping process](https://github.com/AntonioDehesa/tilop/blob/main/Images/Robotics/Map%20Based%20Navigation/1%20-%20Gmapping.png)

The ran instructions, in different terminals, where: 
```bash
roslaunch turtlebot3_gazebo turtlebot3_house.launch
roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping
roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch model
rosrun map_server map_saver -f ~/tb3_house_map
```

Meaning of the colors: 
* White: Empty cell
* Gray: Unknown
* Black: Occupied
![Finished the process, only for the example. It is obviously not completed.](https://github.com/AntonioDehesa/tilop/blob/main/Images/Robotics/Map%20Based%20Navigation/2%20-%20After%20Moving%20the%20turtlebor.png)
## Reading Map Results
```yaml
image: /home/antonio/tb3_house_map.pgm
resolution: 0.050000
origin: [-10.000000, -10.000000, 0.000000]
negate: 0
occupied_thresh: 0.65
free_thresh: 0.196
```
![YML file and Resulting map](https://github.com/AntonioDehesa/tilop/blob/main/Images/Robotics/Map%20Based%20Navigation/3%20-%20Results%20of%20the%20mapping.png)
* Image: Location of the image of the map. It is in BGM format.
* Resolution: Resolution of the map. Expressed in meter/pixel. 
* Origin: [X,Y,Z] position of the origin of the map. 
* Occupied Threshold: Any pixel greater than this number, will be considered occupied. Remember, it is either occupied or not, so a true/false or binary threshold is used. 
* Free Threshold: Same, but with free cells. 


## Map Navigation
Once we have our map, we can begin with the navigation part. 
For this, the commands we used were: 
```bash
roslaunch turtlebot3_gazebo turtlebot3_house.launch
roslaunch turtlebot3_navigation turtlebot3_navigation.launch map_file:=/home/username/tb3map/tb3_house_map.yaml
```
My mistake was NOT including the username in the path. Pretty simple mistake, but still...

I am about to complete the ROS Course, so afterwards, I plan to do a project. 