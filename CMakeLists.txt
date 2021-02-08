# 
# study the pnp method using 2d and 3d points  
#

project(epnp)
cmake_minimum_required(VERSION 2.8.3)

set(CMAKE_CXX_FLAGS "-ggdb -g -O3 -w -std=c++11 -fpermissive") # -fPIC -fpermissive


include_directories("/opt/homebrew/Cellar/eigen/3.3.9/include")
set(EIGEN3_INCLUDE_DIR "/opt/homebrew/Cellar/eigen/3.3.9/include/")
include_directories("/opt/homebrew/Cellar/eigen/3.3.9/include/eigen3")

add_library(epnp_eigen SHARED epnp_eigen epnp_eigen_debug_tool)

add_executable(main  main.cpp)
target_link_libraries(main epnp_eigen)