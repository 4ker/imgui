project( ImGUI )
cmake_minimum_required( VERSION 2.8.3 )

include_directories( ${CMAKE_SOURCE_DIR}/)
include_directories( ${CMAKE_BINARY_DIR}/)
include_directories( ${CMAKE_SOURCE_DIR}/src )
include_directories( ${CMAKE_BINARY_DIR}/src )
include_directories( ${CMAKE_SOURCE_DIR}/src/ImGui )
include_directories( ${CMAKE_BINARY_DIR}/src/ImGui )

configure_file( 
    "${PROJECT_SOURCE_DIR}/Configs.h.in"
    "${PROJECT_BINARY_DIR}/Configs.h" )

add_subdirectory( src )
add_subdirectory( examples )
