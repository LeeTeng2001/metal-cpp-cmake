cmake_minimum_required(VERSION 3.21)
set(CMAKE_CXX_STANDARD 17)
project(metal_cpp_try)

option(METAL_CPP_BUILD_EXAMPLES "Build examples" ON)

add_subdirectory(metal-cmake)  # Library definition

if(METAL_CPP_BUILD_EXAMPLES)
	add_subdirectory(src)  # Add targets
endif(METAL_CPP_BUILD_EXAMPLES)

