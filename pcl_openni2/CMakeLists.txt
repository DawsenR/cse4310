cmake_minimum_required(VERSION 2.8 FATAL_ERROR)
project(pcl_openni2)

# set build type to release
set(CMAKE_BUILD_TYPE "Release")

# explicitly set c++11
set(CMAKE_CXX_STANDARD 11)

# configure PCL
find_package(PCL 1.8.0 REQUIRED)
include_directories(${PCL_INCLUDE_DIRS})
link_directories(${PCL_LIBRARY_DIRS})
add_definitions(${PCL_DEFINITIONS})

add_executable (openni2_snapper openni2_snapper.cpp)
target_link_libraries (openni2_snapper ${PCL_LIBRARIES})

