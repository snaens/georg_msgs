# athome_msgs
> Message descriptions for Ohm @home robots

These Messages/Services/Actions are each implemented by the robot's subsystems.  
This robot utilizes a Functional approach to subsystems, decreasing operational overhead,  
and making it easier to use a central planning system + AI interaction.

## Example messages

### Enums
```msg
# Power supply status constants
uint8 POWER_SUPPLY_STATUS_UNKNOWN = 0
uint8 POWER_SUPPLY_STATUS_CHARGING = 1
uint8 POWER_SUPPLY_STATUS_DISCHARGING = 2
uint8 POWER_SUPPLY_STATUS_NOT_CHARGING = 3
uint8 POWER_SUPPLY_STATUS_FULL = 4

<...>

uint8   power_supply_status     # The charging status as reported. Values defined above
```

### Polling (no-request) service
```srv
---
bool is_calibrated
```

### Pinging (request-only) service
```action
trajectory_msgs/JointTrajectory trajectory
---
```

### Action with no return
```action
geometry_msgs/PointStamped target
geometry_msgs/Vector3 pointing_axis
string pointing_frame
builtin_interfaces/Duration min_duration
float64 max_velocity
---
---
float64 pointing_angle_error
```

## Resources
Many more example messages/services/actions can be found here:
- https://github.com/ros-controls/control_msgs/blob/master/control_msgs/
- https://github.com/ros2/common_interfaces/blob/jazzy/
# athome_msgs
