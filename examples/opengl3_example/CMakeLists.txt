project( OpenGL3Example )
cmake_minimum_required( VERSION 2.6 )
file( GLOB SRCS *.c *.cpp *.cc *.h *.hpp )
include_directories( ${GL3W_INCLUDE_DIR} )
include_directories( ${GLFW_INCLUDE_DIR} )
link_directories( ${GLFW_LINK_DIR} )
add_executable( ${PROJECT_NAME} ${SRCS} ${GL3W_SOURCES} )
target_link_libraries( ${PROJECT_NAME}
    ImGui 
    ${OPENGL_gl_LIBRARY}
    ${OPENGL_glu_LIBRARY}
    ${GLFW_LIBRARY} )
