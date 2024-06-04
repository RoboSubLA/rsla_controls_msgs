# rsla_controls_msgs

RSLA Control's interface package and communications specification.

## Adding the Package

Firstly, [source your ROS 2 installation](https://docs.ros.org/en/iron/Tutorials/Beginner-CLI-Tools/Configuring-ROS2-Environment.html).

```sh
source /opt/ros/iron/setup.bash
```

Include the rsla_controls_msgs package into `<ros2_ws_path>/src`.

```sh
cd <ros2_ws_path>/src
git clone <TODO>
```

From `<ros2_ws_path>` run.

```sh
cd <ros2_ws_path>
colcon build
```

```sh
# verify
source install/local_setup.bash
ros2 interface package rsla_controls_msgs
# ouptuts list of rsla_controls_msgs
```

## Usage (ROS 2 C++)

In order to use rsla_controls_msgs within a ROS 2 C++ package the following 
additions to the package must be made:

### package.xml

Add to `package.xml`

```xml
<depend>rsla_controls_msgs</depend>
```

### CMakeLists.txt

```cmake
#...
find_package(rsla_controls_msgs REQUIRED)

ament_target_dependencies(<executable_name> rclcpp rsla_controls_msgs)
```

### Include Header File

```cpp
// #include "rsla_controls_msgs/msg/<message_file>.hpp"
// e.g.

#include "rsla_controls_msgs/msg/setpoints.hpp"
```

## Messages 


```sh
# list messages
ros2 interface package rsla_controls_msgs
```

```sh
# show msg info
ros2 interface show rsla_controls_msgs/msg/<msg>.msg
```

## Communications Spec.

### Subscribers

TODO

### Publishers

TODO


## Resources
