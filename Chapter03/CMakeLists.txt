project(Chapter03)

file(GLOB SOURCES "${CMAKE_CURRENT_SOURCE_DIR}/*.cpp")

add_executable(Chapter03
    ${SOURCES}
)

target_link_libraries(Chapter03
        SDL2
        ${SDL2_IMAGE_LIBRARIES}
)

add_compile_options(-fsanitize=address -fno-omit-frame-pointer)
add_link_options(-fsanitize=address)

add_custom_command(TARGET Chapter03 POST_BUILD
    COMMAND ${CMAKE_COMMAND} -E copy_directory
    ${CMAKE_CURRENT_SOURCE_DIR}/Assets
    $<TARGET_FILE_DIR:Chapter03>/Assets)