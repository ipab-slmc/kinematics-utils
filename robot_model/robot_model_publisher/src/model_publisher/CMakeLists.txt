################
add_executable(robot_model_publisher robot_model_publisher.cpp)
pods_use_pkg_config_packages(robot_model_publisher 
                             urdf lcm 
                             lcmtypes_robot_model_publisher model-client)

add_executable(robot_model_listener robot_model_listener.cpp)
pods_use_pkg_config_packages(robot_model_listener urdf lcm 
                             lcmtypes_robot_model_publisher)

# make exeutables public
pods_install_executables(robot_model_publisher robot_model_listener)



