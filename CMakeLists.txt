cmake_minimum_required(VERSION 3.5 FATAL_ERROR)

project(rabbit)

find_package(PCL 1.12.0 REQUIRED)

include_directories(${PCL_INCLUDE_DIRS})
link_directories(${PCL_LIBRARY_DIRS})
add_definitions(${PCL_DEFINITIONS})

add_executable (rabbit rabbit.cpp)
target_link_libraries (rabbit ${PCL_LIBRARIES})

