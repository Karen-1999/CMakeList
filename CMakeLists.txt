cmake_minimum_required(VERSION 3.0)

project(PR3)

#set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -Wall")

set(SOURCES C/main.cpp A/preparing.py A/index.cpp)

include_directories("A/" "B/" "C/")

add_executable(PR3 ${SOURCES})

add_subdirectory(B)

target_link_libraries(PR3 B)