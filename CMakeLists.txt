cmake_minimum_required(VERSION 3.8)
project(actor_collision_plugin)

# if(CMAKE_COMPILER_IS_GNUCXX OR CMAKE_CXX_COMPILER_ID MATCHES "Clang")
#   add_compile_options(-Wall -Wextra -Wpedantic)
# endif()

# find dependencies
find_package(ament_cmake REQUIRED)
find_package(gazebo_ros REQUIRED)
# uncomment the following section in order to fill in
# further dependencies manually.
# find_package(<dependency> REQUIRED)

# Include directories
include_directories(
  include
  ${GAZEBO_INCLUDE_DIRS}
  ${rclcpp_INCLUDE_DIRS}
)

# Add the plugin library
add_library(ActorCollisionsPlugin SHARED
  src/ActorCollisionsPlugin.cc
)

# Link the plugin library with necessary dependencies
target_link_libraries(ActorCollisionsPlugin ${GAZEBO_LIBRARIES})

# Install the plugin library
install(TARGETS ActorCollisionsPlugin
  LIBRARY DESTINATION lib/${PROJECT_NAME}
)

# Install the header files
install(DIRECTORY include/
  DESTINATION include/${PROJECT_NAME}
)

# if(BUILD_TESTING)
#   find_package(ament_lint_auto REQUIRED)
#   # the following line skips the linter which checks for copyrights
#   # comment the line when a copyright and license is added to all source files
#   set(ament_cmake_copyright_FOUND TRUE)
#   # the following line skips cpplint (only works in a git repo)
#   # comment the line when this package is in a git repo and when
#   # a copyright and license is added to all source files
#   set(ament_cmake_cpplint_FOUND TRUE)
#   ament_lint_auto_find_test_dependencies()
# endif()

ament_package()
