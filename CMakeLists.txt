cmake_minimum_required(VERSION 3.19)

set(PROJECTNAME "FILLMEIN")

project(${PROJECTNAME})

set(CMAKE_CXX_STANDARD 20)

set(BUILD_SHARED_LIBS TRUE)

add_subdirectory(libs/sfml)

add_executable(${PROJECTNAME} main.cpp)
target_include_directories(${PROJECTNAME} PUBLIC libs/sfml/include)
target_link_libraries(${PROJECTNAME} sfml-system sfml-window sfml-graphics)

