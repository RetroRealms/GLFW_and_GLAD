cmake_minimum_required(VERSION 3.29)
project(GLAD_GLFW_Project VERSION 1.0.0)

# Set C++ standard
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Add the include directories
include_directories(include)

# Add the GLAD source file
add_library(glad src/glad.c)

# Add the GLFW library
add_subdirectory(glfw)

# Add the executable
add_executable(GLAD_GLFW_Project main.cpp)

# Link the libraries
target_link_libraries(GLAD_GLFW_Project glad glfw ${GLFW_LIBRARIES})
