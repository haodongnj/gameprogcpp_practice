project(Chapter02)

file(GLOB SOURCES "${CMAKE_CURRENT_SOURCE_DIR}/*.cpp")

add_executable(Chapter02
    ${SOURCES}
)

target_link_libraries(Chapter02
        SDL2
        ${SDL2_IMAGE_LIBRARIES}
)

add_custom_command(TARGET Chapter02 POST_BUILD
    COMMAND ${CMAKE_COMMAND} -E copy_directory
    ${CMAKE_CURRENT_SOURCE_DIR}/Assets
    $<TARGET_FILE_DIR:Chapter02>/Assets)