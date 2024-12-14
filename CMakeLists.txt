cmake_minimum_required(VERSION 3.10)

project(
  ml
  CXX
)

if (CMAKE_BUILD_TYPE STREQUAL "")
  set(CMAKE_BUILD_TYPE Debug)
endif()

# 设置std (Set std)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_STANDARD 14)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

add_compile_options(-std=c++14 -Wall -Werror -pedantic-errors)

message(STATUS "Build\ type\ is: ${CMAKE_BUILD_TYPE}")

add_subdirectory(src)
add_subdirectory(subprojects/glm)
add_subdirectory(subprojects/cgc)
