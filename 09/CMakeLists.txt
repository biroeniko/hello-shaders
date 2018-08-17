# Project definition
cmake_minimum_required(VERSION 2.8)
project(camera_walkaround_lookaround)

# Source files
set(SRC_DIR "${CMAKE_CURRENT_SOURCE_DIR}/src")
set(SHADER_DIR "${CMAKE_CURRENT_SOURCE_DIR}/src/shaders")
set(INCLUDE_DIR "${CMAKE_CURRENT_SOURCE_DIR}/includes")
set(SOURCES "${SRC_DIR}/main.cpp")

find_package(glfw3 REQUIRED)
find_package(OpenGL REQUIRED)
find_package(GLUT REQUIRED)

include_directories(${OPENGL_INCLUDE_DIRS}  ${GLUT_INCLUDE_DIRS} ${INCLUDE_DIR})

# Executable definition and properties
add_executable(${PROJECT_NAME} ${SOURCES})
target_include_directories(${PROJECT_NAME} PRIVATE "${SRC_DIR}")
set_property(TARGET ${PROJECT_NAME} PROPERTY CXX_STANDARD 11)

# pkg-config --static --libs glfw3 -> OUTPUT
target_link_libraries(${PROJECT_NAME} glfw3 GL GLU rt m dl Xrandr Xinerama Xxf86vm Xext Xcursor Xrender Xfixes X11 pthread xcb Xau Xdmcp)

# glad
set(GLAD_DIR "${INCLUDE_DIR}/glad")
add_library("glad" "${GLAD_DIR}/src/glad.c")
target_include_directories("glad" PRIVATE "${GLAD_DIR}/include")
target_include_directories(${PROJECT_NAME} PRIVATE "${GLAD_DIR}/include")
target_link_libraries(${PROJECT_NAME} "glad" "${CMAKE_DL_LIBS}")
