cmake_minimum_required(VERSION 3.10)

project(Chapter01)

add_executable(Chapter01
        ${CMAKE_CURRENT_SOURCE_DIR}/Main.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/Game.cpp
)
target_link_libraries(Chapter01 SDL2)
