cmake_minimum_required(VERSION 3.9)

set(CMAKE_CXX_COMPILER "clang++")
project(sonar_scanner_example)

# Add compile flags to instrument the binaries for coverage
set(CMAKE_CXX_FLAGS " ${CMAKE_CXX_FLAGS} -fprofile-instr-generate -fcoverage-mapping -O0 -g")
set(CMAKE_CXX_STANDARD 17)

add_executable(coverage_test1 src/lib.cpp src/test1.cpp)
add_executable(coverage_test2 src/lib.cpp src/test2.cpp)

