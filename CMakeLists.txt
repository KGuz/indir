cmake_minimum_required(VERSION 2.6)

project(indeer)

if(NOT CMAKE_BUILD_TYPE)
  set(CMAKE_BUILD_TYPE Release)
endif()

set(CMAKE_CXX_FLAGS "-Wall -Wextra")
set(CMAKE_CXX_FLAGS_DEBUG "-g")
set(CMAKE_CXX_FLAGS_RELEASE "-O3")

set(CMAKE_CXX_STANDARD 17)

set(EXECUTABLE_OUTPUT_PATH bin)

include_directories(include)

file(GLOB SOURCES "src/*.cpp")

add_executable(indeer ${SOURCES})

target_link_libraries(indeer pthread)
