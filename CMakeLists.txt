cmake_minimum_required(VERSION 3.0)

project(PR3)

EXECUTE_PROCESS(COMMAND python "preparing.py" WORKING_DIRECTORY A)
#set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -Wall")

set(SOURCES C/main.cpp A/preparing.py)


include_directories(${PROJECT_SOURCE_DIR})
add_executable(PR3 ${SOURCES})

add_subdirectory(B)
target_link_libraries(PR3 B)
