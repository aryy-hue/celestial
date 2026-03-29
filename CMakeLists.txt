cmake_minimum_required(VERSION 3.10)
project(Celestial)

set(CMAKE_CXX_STANDARD 17)

find_package(OpenGL REQUIRED)
find_package(glfw3 REQUIRED)
find_package(assimp REQUIRED)

set(SOURCES src/main.cpp src/glad.c)
add_executable(Celestial ${SOURCES})

target_include_directories(Celestial PRIVATE include)
target_link_libraries(Celestial PRIVATE OpenGL::GL glfw assimp dl)