cmake_minimum_required(VERSION 3.10)
project(gameprogcpp)

list(APPEND CMAKE_MODULE_PATH ${CMAKE_CURRENT_SOURCE_DIR}/cmake)

find_package(SDL2 REQUIRED)
find_package(SDL2_image REQUIRED)

add_subdirectory(Chapter01)
add_subdirectory(Chapter02)