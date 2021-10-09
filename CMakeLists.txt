cmake_minimum_required(VERSION 3.20)
project(MAZE LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 20)

add_library(MAZE library.cpp)

if (CMAKE_COMPILER_IS_GNUCXX AND CMAKE_CXX_COMPILER_VERSION VERSION_LESS 9.0)
    message(FATAL_ERROR "MAZE requires at least g++-9")
endif()
