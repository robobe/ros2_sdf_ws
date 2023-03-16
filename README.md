
## LAB1
- build simple model with links and joints
  - three links same size 
  - one fixed joint
  - one revolute
  - control joints position and axes
- spawn model into gazebo
- add ros plugin for joint state and joint trajectory
- control joints

## reference
- [sdf specification](http://sdformat.org/spec)

## XXX

![](images/gazebo_with_model_lab1.png)

```bash
ros2 topic list
#
/clock
/joint_states
/parameter_events
/rosout
/set_joint_trajectory
```

```bash title="set_joint_trajectory"
ros2 topic pub -1 /set_joint_trajectory trajectory_msgs/msg/JointTrajectory '{header: {frame_id: world}, joint_names: [joint_child_fixed], points: [  {positions: {0.8}} ]}' 
```

![](images/gazebo_with_mode_after_trajectory.png)

!!! tip check gazebo view menu
    - show joints
    - show links frame
    - note joint axes rotation

!!! tip model develop
    Use gazebo **insert** TAB
     