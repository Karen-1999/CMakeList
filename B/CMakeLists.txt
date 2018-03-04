cmake_minimum_required(VERSION 3.0)
project(B)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -Wall")
set(SOURCES lib.cpp)

add_library(B ${SOURCES})