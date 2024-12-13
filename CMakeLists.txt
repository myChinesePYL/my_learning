cmake_minimum_required(VERSION 3.10)

project(
  ml
  CXX
)

if (CMAKE_BUILD_TYPE STREQUAL "")
  set(CMAKE_BUILD_TYPE Debug)
endif()

message(STATUS "Build\ type\ is: ${CMAKE_BUILD_TYPE}")

add_subdirectory(src)
