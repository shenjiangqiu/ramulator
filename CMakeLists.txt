cmake_minimum_required(VERSION 3.10)
set(CMAKE_CXX_FLAGS "-Wall" )
aux_source_directory(src source)
add_library(ramulator ${source})
target_include_directories(ramulator PUBLIC src)

add_executable(ramulator_test main.cc)
target_link_libraries(ramulator_test PUBLIC ramulator)