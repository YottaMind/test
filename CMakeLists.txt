cmake_minimum_required(VERSION 3.20)

project(
srt-test
C
CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)

find_package(srt REQUIRED CONFIG)

target_compile_options(srt-test PRIVATE -Wall -Wextra -pedantic)
add_executable(srt-test main.cpp)

target_link_libraries(srt-test srt)
