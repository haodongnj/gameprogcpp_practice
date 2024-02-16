cmake_minimum_required(VERSION 3.10)
project(gameprogcpp)

list(APPEND CMAKE_MODULE_PATH ${CMAKE_CURRENT_SOURCE_DIR}/cmake)


set(OpenGL_GL_PREFERENCE GLVND)
message(STATUS "Using OpenGL with ${OpenGL_GL_PREFERENCE}")

find_package(SDL2 REQUIRED)
find_package(SDL2_image REQUIRED)
find_package(OpenGL REQUIRED)
find_package(GLEW REQUIRED)

set(SOIL_LIBRARIES /usr/lib/libSOIL.so)


add_subdirectory(Chapter01)
add_subdirectory(Chapter02)
add_subdirectory(Chapter03)

add_subdirectory(Chapter05)
