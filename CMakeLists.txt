# @file CMakeLists.txt
# 
# CMake file for RAIIDataMembers

cmake_minimum_required(VERSION 3.28 FATAL_ERROR)

project(RAIIDataMembers)

# RAIIDataMembers
add_executable(RAIIDataMembers)
target_sources(RAIIDataMembers PRIVATE RAIIDataMembers.cpp)
target_compile_features(RAIIDataMembers PRIVATE cxx_std_17)
target_compile_options(RAIIDataMembers PRIVATE
    $<$<CXX_COMPILER_ID:MSVC>:/Wall>
    $<$<CXX_COMPILER_ID:GNU,Clang,AppleClang>:-Wall>
)
