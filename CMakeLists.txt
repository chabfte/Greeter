cmake_minimum_required(VERSION 3.16)

# set the project name
project(Greeter)

# Pass information to the source code
configure_file(greeter_config.h.in greeter_config.h)

# add the executable target named HelloWorld
add_executable(greet greet.cpp)

# add binary tree to the list of paths to search includes 
target_include_directories(greet PUBLIC "${PROJECT_BINARY_DIR}")