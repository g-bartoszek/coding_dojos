cmake_minimum_required(VERSION 2.6)
add_definitions(-Wall -pedantic -Werror -std=c++17)
project(valley)
include_directories(include)
add_executable(run src/main.cpp src/Solver.cpp)



enable_testing()
find_package(GTest REQUIRED)
include_directories(${GTEST_INCLUDE_DIRS})
add_executable(run_tests test/main.cpp src/Solver.cpp)
target_link_libraries(run_tests ${GTEST_BOTH_LIBRARIES})
