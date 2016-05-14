# add_subdirectory( misc_examples )
# add_subdirectory( sdl_opengl_example )

if ( WIN32 )
    find_package( OpenGL REQUIRED )
    add_subdirectory( directx9_example )
    # [How to install the latest version of DirectX](https://support.microsoft.com/en-us/kb/179113) 
    # add_subdirectory( directx10_example )
    # add_subdirectory( directx11_example )

    # opengl
    set( GLFW_LIBRARY glfw3 )
    set( GLFW_INCLUDE_DIR ${CMAKE_CURRENT_SOURCE_DIR}/libs/glfw/include )
    set( GLFW_LINK_DIR ${CMAKE_CURRENT_SOURCE_DIR}/libs/glfw/lib-vc2010-64 )
    add_subdirectory( opengl_example )
    include_directories( ${GLFW_INCLUDE_DIR} )
    link_directories( ${GLFW_LINK_DIR} )

    # opengl3
    set( GL3W_INCLUDE_DIR ${CMAKE_CURRENT_SOURCE_DIR}/libs/gl3w )
    file( GLOB GL3W_SOURCES ${CMAKE_CURRENT_SOURCE_DIR}/libs/gl3w/*.c )
    # add_subdirectory( opengl3_example )

    # add_subdirectory( vulkan_example )
endif ( WIN32 )

add_subdirectory( raytrace_example )
