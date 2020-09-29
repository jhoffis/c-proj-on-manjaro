cmake_minimum_required(VERSION 3.17)
project(untitled1)

set(CMAKE_CXX_STANDARD 20)

add_executable(untitled1 main.cpp)

find_package(Vulkan REQUIRED)
target_include_directories(${PROJECT_NAME} PUBLIC ${Vulkan_INCLUDE_DIRS})
target_link_libraries(${PROJECT_NAME} Vulkan::Vulkan)

find_package(glm REQUIRED)
target_include_directories(${PROJECT_NAME} PUBLIC /usr/include/glm)
target_link_libraries(${PROJECT_NAME} glm)

find_package(glfw3 REQUIRED)
target_include_directories(${PROJECT_NAME} PUBLIC /usr/include/GLFW)
target_link_libraries(${PROJECT_NAME} glfw)
#include_directories(/usr/include/glm [${CMAKE_HOME_DIRECTORY}])
