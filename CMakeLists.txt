cmake_minimum_required(VERSION 3.10)

project(OpenGLHelloWindow)

set(CMAKE_CXX_STANDARD 11)

# Include directories
include_directories(glad/include)

# Add source files
add_executable(OpenGLHelloWindow main.cpp glad/src/glad.c)

# Link GLFW
find_package(glfw3 3.3 REQUIRED)
target_link_libraries(OpenGLHelloWindow glfw)
