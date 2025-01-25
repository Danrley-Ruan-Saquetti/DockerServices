cmake_minimum_required(VERSION 2.8.12)

project(GameEngine)

set(CMAKE_CXX_STANDARD 17)
set(Sample_VERSION_MAJOR 0)
set(Sample_VERSION_MINOR 0)
set(Sample_VERSION_PATCH 1)

configure_file(
  "${PROJECT_SOURCE_DIR}/config.h.in"
  "${PROJECT_BINARY_DIR}/config.h"
)

file(GLOB_RECURSE SOURCES "src/*.cpp")

include_directories("${PROJECT_BINARY_DIR}")

add_executable(program src/main.cpp)