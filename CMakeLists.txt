cmake_minimum_required(VERSION 3.2)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -O3")

set(CMAKE_INSTALL_PREFIX ${CMAKE_BINARY_DIR})
include(GNUInstallDirs)

add_subdirectory(src)
add_subdirectory(test)


