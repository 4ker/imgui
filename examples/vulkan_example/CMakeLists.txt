cmake_minimum_required(VERSION 2.8)
project(ImGuiGLFWVulkanExample C CXX)

if(NOT CMAKE_BUILD_TYPE)
  set(CMAKE_BUILD_TYPE Debug CACHE STRING "" FORCE)
endif()

set (CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -DVK_PROTOTYPES")
set (CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -DVK_PROTOTYPES")

# Libraries
find_library(VULKAN_LIBRARY
  NAMES vulkan vulkan-1)
set(LIBRARIES "glfw;${VULKAN_LIBRARY}")

# Use vulkan headers from glfw:
include_directories(${GLFW_DIR}/deps)

file(GLOB sources *.cpp)

add_executable(vulkan_example ${sources} )
target_link_libraries(vulkan_example ${LIBRARIES} ImGui ${GLFW_LIBRARY} )
