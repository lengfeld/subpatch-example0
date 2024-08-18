cmake_minimum_required(VERSION 3.5)

project(libadd)

set(CMAKE_C_STANDARD 11)

add_library(add SHARED libadd.c)
target_include_directories(add SYSTEM PUBLIC include/)

add_executable(prog prog.c)
target_link_libraries(prog PRIVATE add)

# Tests
#add_subdirectory(external/googletest gtest)
#add_executable(test test.cc)
#target_link_libraries(test GTest::gtest_main add)
#include(GoogleTest)
#gtest_discover_tests(test)
